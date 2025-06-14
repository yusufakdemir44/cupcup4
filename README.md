<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sana Özel</title>
  <style>
    body {
      font-family: sans-serif;
      background: linear-gradient(135deg, #fff0f5, #ffe4e1);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      height: 100vh;
      margin: 0;
      padding: 20px;
    }

    h1 {
      font-size: 24px;
      margin-bottom: 30px;
      color: #444;
    }

    .buttons {
      display: flex;
      gap: 20px;
      margin-bottom: 25px;
    }

    button {
      padding: 12px 24px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      color: white;
    }

    .play {
      background-color: #ff5e78;
    }

    .pause {
      background-color: #888;
    }

    .link {
      text-decoration: none;
      color: white;
      background-color: #1db954;
      padding: 12px 20px;
      border-radius: 10px;
      font-size: 16px;
    }

    .youtube {
      background-color: #ff0000;
    }

    .spotify {
      background-color: #1db954;
    }
  </style>
</head>
<body>
  <h1>Bu buton sadece sana özel</h1>

  <div class="buttons">
    <button class="play" onclick="playSong()">Başlat</button>
    <button class="pause" onclick="pauseSong()">Durdur</button>
  </div>

  <audio id="song" src="Kenan Doğulu - Ara Beni Lütfen (Official Video) #Festival.mp3"></audio>

  <a class="link youtube" href="https://www.youtube.com/watch?v=2QaBwvR6G3A" target="_blank">
    YouTube'da Dinle
  </a>
  <br /><br />
  <a class="link spotify" href="https://open.spotify.com/track/2ytdiXcGQggDltO7t5jqx4" target="_blank">
    Spotify'da Dinle
  </a>

  <script>
    const audio = document.getElementById("song");

    function playSong() {
      audio.play().catch(err => {
        alert("Ses oynatılamadı. Tarayıcı engelliyor olabilir.");
        console.error(err);
      });
    }

    function pauseSong() {
      audio.pause();
    }
  </script>
</body>
</html>
