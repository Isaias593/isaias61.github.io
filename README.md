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
![image](https://user-images.githubusercontent.com/58237470/218566736-10c82398-ef78-419b-8ba0-1c4c1cfec809.png)
