# youcine-gratis-web
youcine feito para pc, notebook, celulares e tvs smarts
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>FreeCine</title>
<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #000;
  color: white;
}
header {
  background: #111;
  padding: 15px;
  font-size: 22px;
  color: red;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
  gap: 15px;
  padding: 20px;
}
.card {
  background: #222;
  border-radius: 10px;
  overflow: hidden;
  cursor: pointer;
}
.card img {
  width: 100%;
}
.card p {
  padding: 10px;
  text-align: center;
}
video {
  width: 100%;
  max-height: 80vh;
}
</style>
</head>
<body>

<header>🎬 FreeCine</header>

<div class="grid">
  <div class="card" onclick="playVideo('https://archive.org/download/BigBuckBunny_328/BigBuckBunny_512kb.mp4')">
    <img src="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg">
    <p>Big Buck Bunny</p>
  </div>
</div>

<video id="player" controls></video>

<script>
function playVideo(url) {
  const player = document.getElementById("player");
  player.src = url;
  player.play();
  window.scrollTo(0, document.body.scrollHeight);
}
</script>

</body>
</html>
