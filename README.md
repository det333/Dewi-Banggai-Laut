# Dewi-Banggai-Laut
Destinasi Wisata Banggai Laut
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <title>VR 360 Pantai Lambangan Pauno</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no"/>
  <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
  <style>
    body { margin:0; background:#000; }
  </style>
</head>
<body>
  <a-scene>
    <a-assets>
      <!-- Video panorama 360 -->
      <video id="paunoVid" src="assets/lambangan_pauno.mp4"
             autoplay loop muted playsinline crossorigin="anonymous"></video>
    </a-assets>

    <!-- Sphere tempat video 360 diproyeksikan -->
    <a-videosphere src="#paunoVid" rotation="0 -90 0"></a-videosphere>

    <!-- Camera & cursor -->
    <a-entity camera look-controls>
      <a-cursor></a-cursor>
    </a-entity>
  </a-scene>
</body>
</html>
