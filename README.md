<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Letters for Aya</title>

  <!-- Handwritten font -->
  <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@400;600&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      background: radial-gradient(circle at top, #2b1055, #0b0614);
      font-family: 'Caveat', cursive;
      color: #eadcff;
      overflow-x: hidden;
    }

    /* Twinkling stars */
    .stars {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }

    .star {
      position: absolute;
      width: 2px;
      height: 2px;
      background: white;
      border-radius: 50%;
      opacity: 0.8;
      animation: twinkle 3s infinite alternate;
    }

    @keyframes twinkle {
      0% { opacity: 0.2; }
      50% { opacity: 0.8; }
      100% { opacity: 0.2; }
    }

    .container {
      max-width: 720px;
      margin: 60px auto;
      padding: 0 20px;
    }

    h1 {
      text-align: center;
      color: #d9b8ff;
      text-shadow: 0 0 12px rgba(200, 140, 255, 0.6);
      margin-bottom: 10px;
      letter-spacing: 2px;
    }

    .description {
      text-align: center;
      opacity: 0.7;
      margin-bottom: 50px;
      font-size: 18px;
      line-height: 1.5;
    }

    .letter-box {
      background: rgba(30, 12, 55, 0.85);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 40px;
      margin-bottom: 50px;
      box-shadow: 0 8px 25px rgba(160, 90, 255, 0.25);
      transition: transform 0.2s, box-shadow 0.2s;
      border-top: 1px solid rgba(255,255,255,0.1);
      border-bottom: 1px solid rgba(255,255,255,0.1);
    }

    .letter-box:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 35px rgba(200, 120, 255, 0.35);
    }

    .date {
      font-size: 16px;
      opacity: 0.7;
      margin-bottom: 20px;
    }

    iframe {
      margin: 20px 0;
      border-radius: 12px;
    }

    .letter {
      font-size: 22px;
      line-height: 1.9;
      white-space: pre-line;
    }

    .signature {
      margin-top: 30px;
      text-align: right;
      color: #cfa8ff;
      font-size: 20px;
    }

    @media (max-width: 600px) {
      .letter {
        font-size: 20px;
      }
      .letter-box {
        padding: 30px;
      }
    }
  </style>
</head>
<body>

<!-- Stars -->
<div class="stars" id="stars"></div>

<div class="container">
  <h1>Letters for Aya</h1>
  <p class="description">
    A collection of letters and songs for Aya. Soft thoughts, quiet nights, and music that sits beside the words.
  </p>

  <!-- ===== LETTER TEMPLATE ===== -->
  <!-- Copy this block to add a new letter -->
  <div class="letter-box">
    <div class="date">DATE HERE</div>

    <iframe src="SPOTIFY_LINK_HERE"
      width="100%" height="80" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>

    <div class="letter">
YOUR LETTER TEXT HERE
    </div>

    <div class="signature">— Nic</div>
  </div>
  <!-- ===== END LETTER TEMPLATE ===== -->

  <!-- Example Letters -->
  <div class="letter-box">
    <div class="date">September 27, 2025</div>

    <iframe src="https://open.spotify.com/embed/track/PUT_SPOTIFY_LINK_1"
      width="100%" height="80" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>

    <div class="letter">
Dear Aya,

I wanted this song to sit quietly beside these words.
No pressure.
No expectations.
Just a place you can rest for a while.
    </div>

    <div class="signature">— Nic</div>
  </div>

  <div class="letter-box">
    <div class="date">October 1, 2025</div>

    <iframe src="https://open.spotify.com/embed/track/PUT_SPOTIFY_LINK_2"
      width="100%" height="80" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>

    <div class="letter">
Dear Aya,

Purple nights always feel softer.
So I left this letter here,
glowing quietly,
waiting for you.
    </div>

    <div class="signature">— Nic</div>
  </div>

</div>

<script>
  // Create 100 twinkling stars
  const starsContainer = document.getElementById('stars');
  for (let i = 0; i < 100; i++) {
    const star = document.createElement('div');
    star.classList.add('star');
    star.style.top = Math.random() * 100 + '%';
    star.style.left = Math.random() * 100 + '%';
    star.style.width = (Math.random() * 2 + 1) + 'px';
    star.style.height = star.style.width;
    star.style.animationDuration = (Math.random() * 3 + 2) + 's';
    starsContainer.appendChild(star);
  }
</script>

</body>
</html>
