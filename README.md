# Geolocalizacion!

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Mi ubicación GPS</title>
  </head>
  <body>
    <h1 id="location">Cargando ubicación...</h1>
    <script>
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position) {
          var latitude = position.coords.latitude;
          var longitude = position.coords.longitude;
          document.getElementById("location").innerHTML =
            "Latitud: " + latitude + "<br>Longitud: " + longitude;
        });
      } else {
        document.getElementById("location").innerHTML =
          "Lo siento, tu navegador no soporta la ubicación GPS.";
      }
    </script>
  </body>
</html>

![image](https://user-images.githubusercontent.com/57690542/218569617-36e7f680-2f7d-482e-b246-cf9b056e7f45.png)
