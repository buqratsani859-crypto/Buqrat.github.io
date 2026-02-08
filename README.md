<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Propose Day ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #fff;
      overflow: hidden;
    }
    .card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      padding: 40px 30px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      max-width: 420px;
      position: relative;
    }
    h1 {
      font-size: 2.2rem;
      margin-bottom: 10px;
    }
    .names {
      font-size: 1.1rem;
      margin-bottom: 10px;
      opacity: 0.95;
    }
    p {
      font-size: 1.05rem;
      margin-bottom: 25px;
      line-height: 1.6;
    }
    .heart {
      font-size: 3rem;
      animation: beat 1s infinite;
    }
    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    .buttons {
      display: flex;
      gap: 15px;
      justify-content: center;
      margin-top: 10px;
      position: relative;
    }
    button {
      background: #ff4b5c;
      border: none;
      padding: 12px 22px;
      font-size: 1rem;
      color: white;
      border-radius: 25px;
      cursor: pointer;
      transition: transform 0.2s, background 0.3s;
      position: relative;
    }
    button:hover {
      background: #ff2e44;
    }
    #noBtn {
      background: #ffffff;
      color: #ff4b5c;
    }
    #noBtn:hover {
      background: #ffe6ea;
    }
    .hint {
      font-size: 0.85rem;
      opacity: 0.85;
      margin-top: 8px;
    }
    audio {
      margin-top: 18px;
      width: 100%;
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="heart">❤️</div>
    <h1>Happy Propose Day</h1>
    <div class="names">Buqqi ➜ Arfa</div>
    <p>
      Arfa, tum meri zindagi ka sab se khoobsurat hissa ho.<br />
      Aaj dil se pooch raha hoon —<br /><br />
      Kya tum meri banogi?<br />
      Aaj, kal aur hamesha 💗
    </p><div class="buttons">
  <button id="yesBtn">Yes 💞</button>
  <button id="noBtn">No 🙈</button>
</div>
<div class="hint">(Hint: No pakarna mushkil hai 😅)</div>

<audio id="bgMusic" controls>
  <!-- Place the song file in the SAME folder as this HTML -->
  <!-- File name expected: meri_zindagi_hai_tu.mp3 -->
  <source src="meri_zindagi_hai_tu.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

  </div>  <script>
    const noBtn = document.getElementById('noBtn');
    const yesBtn = document.getElementById('yesBtn');
    const music = document.getElementById('bgMusic');

    // Move NO button randomly to tease
    noBtn.addEventListener('mouseenter', moveNo);
    noBtn.addEventListener('click', moveNo);

    function moveNo() {
      const x = Math.random() * (window.innerWidth - 120);
      const y = Math.random() * (window.innerHeight - 120);
      noBtn.style.position = 'fixed';
      noBtn.style.left = x + 'px';
      noBtn.style.top = y + 'px';
    }

    // YES button celebration
    yesBtn.addEventListener('click', () => {
      alert('She said YES! 💍❤️\nBuqqi & Arfa');
      // Try to play music on user interaction (allowed by browsers)
      music.play().catch(() => {});
    });
  </script></body>
</html>
