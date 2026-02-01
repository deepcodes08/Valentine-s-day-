<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Valentine’s Day 💖</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
  }
  .card {
    background: white;
    padding: 40px 50px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 20px 40px rgba(0,0,0,0.25);
  }
  h1 {
    margin-bottom: 30px;
    color: #ff4d6d;
  }
  button {
    font-size: 18px;
    padding: 12px 30px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    margin: 10px;
    transition: 0.3s;
  }
  #yes {
    background: #ff4d6d;
    color: white;
  }
  #yes:hover {
    transform: scale(1.1);
  }
  #no {
    background: #ddd;
    position: absolute;
  }
</style>
</head>

<body>

<div class="card">
  <h1>Happy Valentine’s Day 💕<br>Will you be my Valentine?</h1>
  <button id="yes" onclick="yesClick()">Yes 💖</button>
  <button id="no" onmouseover="moveNo()">No 🙃</button>
</div>

<script>
function yesClick() {
  document.body.innerHTML = `
    <div style="
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      background:linear-gradient(135deg,#ff758c,#ff7eb3);
      color:white;
      font-size:32px;
      font-family:Poppins;
      text-align:center;
    ">
      💖 Yay! You made my Valentine special 😍
    </div>
  `;
}

function moveNo() {
  const btn = document.getElementById("no");
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  btn.style.left = x + "px";
  btn.style.top = y + "px";
}
</script>

</body>
</html>
