# Giddy511.github.io
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>MAPOLY GPS</title>
  <meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">
  <script src="https://api.mapbox.com/mapbox-gl-js/v2.16.1/mapbox-gl.js"></script>
  <link href="https://api.mapbox.com/mapbox-gl-js/v2.16.1/mapbox-gl.css" rel="stylesheet" />
  <style>
    body { margin:0; padding:0; }
    #map { position:absolute; top:0; bottom:0; width:100%; }
  </style>
</head>
<body>
<div id="map"></div>
<script>
mapboxgl.accessToken = 'YOUR_MAPBOX_ACCESS_TOKEN';
const map = new mapboxgl.Map({
  container: 'map',
  style: 'mapbox://styles/mapbox/streets-v12',
  center: [3.3267, 7.1543], // Default center (MAPOLY library area)
  zoom: 16
});

// Add marker example
new mapboxgl.Marker().setLngLat([3.3267, 7.1543]).setPopup(new mapboxgl.Popup().setText("Library")).addTo(map);
</script>
</body>
</html>
