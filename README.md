<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>MAPOLY MAP</title>
  <meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no" />
  
  <!-- Mapbox GL JS CSS -->
  <link href="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.css" rel="stylesheet" />
  
  <!-- Mapbox Directions CSS -->
  <link href="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.1/mapbox-gl-directions.css" rel="stylesheet" />

  <style>
    body { margin: 0; padding: 0; }
    #map { position: absolute; top: 0; bottom: 0; width: 100%; }
  </style>
</head>
<body>

<div id="map"></div>

<!-- Mapbox GL JS -->
<script src="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.js"></script>

<!-- Mapbox Directions plugin -->
<script src="https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-directions/v4.1.1/mapbox-gl-directions.js"></script>

<script>
  // Replace this with your actual Mapbox token
  mapboxgl.accessToken = 'pk.eyJ1IjoiZ2lkZHk1IiwiYSI6ImNtZjczNDRldTBuMGQyanFzdnl4YWFmeWgifQ.FB1TNdmdlBsMNI21m9lijg';

  // Initialize the map
  const map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/streets-v11',
    center: [3.3666, 7.1570], // Example: MAPOLY coordinates (you can adjust)
    zoom: 15
  });

  // Add navigation directions
  const directions = new MapboxDirections({
    accessToken: mapboxgl.accessToken,
    unit: 'metric',
    profile: 'mapbox/walking'
  });

  map.addControl(directions, 'top-left');
</script>

</body>
</html>
