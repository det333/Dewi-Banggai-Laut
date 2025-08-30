<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <title>Wisata VR 360 - Pantai Lambangan Pauno</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- A-Frame -->
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
    }
    .overlay {
      position: absolute;
      top: 20px;
      left: 20px;
      background: rgba(0,0,0,0.5);
      padding: 15px 20px;
      border-radius: 12px;
      color: white;
      max-width: 350px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.4);
      animation: fadeIn 2s ease-in-out;
    }
    .overlay h1 {
      font-size: 22px;
      margin: 0 0 10px 0;
      color: #ffdd57;
    }
    .overlay p {
      margin: 0;
      font-size: 14px;
      line-height: 1.4;
    }
    .footer {
      position: absolute;
      bottom: 15px;
      right: 20px;
      font-size: 12px;
      color: white;
      background: rgba(0,0,0,0.4);
      padding: 6px 12px;
      border-radius: 8px;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <!-- Overlay Informasi -->
  <div class="overlay">
    <h1>🌊 Pantai Lambangan Pauno</h1>
    <p>
      Selamat datang di Pantai Lambangan Pauno, surga tersembunyi di Luwuk Banggai 🌴.  
      Pantai ini menawarkan air laut jernih, pasir putih yang lembut,  
      serta panorama alam yang menenangkan jiwa.  
      Cocok untuk wisata bahari, snorkeling, atau sekadar menikmati sunset.
    </p>
  </div>

  <!-- Footer Kecil -->
  <div class="footer">📍 Luwuk Banggai, Sulawesi Tengah</div>

  <!-- VR Scene -->
  <a-scene>
    <!-- Video 360 -->
    <video id="paunoVideo" src="LPauno.mp4" autoplay loop="true" crossorigin="anonymous" playsinline webkit-playsinline></video>

    <!-- Sphere background pakai video -->
    <a-videosphere src="#paunoVideo"></a-videosphere>

    <!-- Kamera -->
    <a-entity camera look-controls></a-entity>
  </a-scene>
</body>
</html>
