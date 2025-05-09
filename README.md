<!DOCTYPE html>
<html>
<head>
  <title>CHUNGTHIENSON</title>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <style>
    #map {
      height: 500px;
    }
  </style>
</head>
<body>
  <h3>Bản đồ: Tượng đài Cà Mau</h3>
  <div id="map"></div>

  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
  <script>
  
    var tuongDaiCoords = [9.176222, 105.150861];

    var map = L.map('map').setView(tuongDaiCoords, 17);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© OpenStreetMap contributors'
    }).addTo(map);

    
    var circle = L.circle(tuongDaiCoords, {
      color: 'red',           
      fillColor: 'green',     
      fillOpacity: 0.3,       
      radius: 60      
    }).addTo(map);

    var marker = L.marker(tuongDaiCoords).addTo(map);
    marker.bindPopup("<b>Tượng đài Cà Mau</b>").openPopup();

 
    circle.bindPopup("<b>Tượng đài Cà Mau</b>");
  </script>
</body>
</html>
