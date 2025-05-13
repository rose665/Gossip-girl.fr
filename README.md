<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Bienvenue</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      font-family: Arial, sans-serif;
    }

    .hero {
      position: relative;
      height: 100vh;
      overflow: hidden;
    }

    .hero iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      pointer-events: none;
      z-index: 0;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.5);
      z-index: 1;
    }

    .hero-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      text-align: center;
      z-index: 2;
      background: rgba(0, 0, 0, 0.6);
      padding: 30px;
      border-radius: 15px;
      backdrop-filter: blur(10px);
      cursor: pointer;
    }

    .hero-text h1 {
      font-size: 32px;
      margin-bottom: 15px;
    }

    .hero-text p {
      font-size: 18px;
    }

    .content {
      height: 100vh;
      background: white;
      padding: 50px;
    }
  </style>
</head>
<body>

  <div class="hero" onclick="scrollToContent()">
    <iframe 
      src="https://www.youtube.com/embed/NUuRX3JYCHY?autoplay=1&mute=0&controls=0&modestbranding=1&rel=0&showinfo=0&loop=1&playlist=NUuRX3JYCHY" 
      title="Intro Video" 
      frameborder="0" 
      allow="autoplay; encrypted-media" 
      allowfullscreen>
    </iframe>

    <div class="overlay"></div>

    <div class="hero-text">
      <h1>Le savoir est une arme</h1>
      <p>Encore faut-il savoir s’en servir</p>
    </div>
  </div>

  <div id="main-content" class="content">
    <h2>Bienvenue sur mon site</h2>
    <p>Contenu à venir (boutique, présentation, contact...)</p>
  </div>

  <script>
    function scrollToContent() {
      document.getElementById('main-content').scrollIntoView({ behavior: 'smooth' });
    }
  </script>

</body>
</html>
