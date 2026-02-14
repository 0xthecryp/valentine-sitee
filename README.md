# valentine-sitee
<!DOCTYPE html>
<html>
<head>
  <title>Be My Val? ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg,#ff4d6d,#ff8fa3);
      overflow: hidden;
    }

    .container {
      text-align: center;
      color: white;
    }

    h1 {
      font-size: 38px;
    }

    .buttons {
      margin-top: 20px;
      position: relative;
    }

    button {
      padding: 15px 25px;
      font-size: 18px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      margin: 10px;
      transition: 0.2s;
    }

    #yes {
      background: #28a745;
      color: white;
      font-size: 18px;
    }

    #no {
      background: #333;
      color: white;
      position: absolute;
    }
  </style>
</head>

<body>

<div class="container">
  <h1>Happiness ❤️</h1>
  <h1>Will you be my Val? 💖</h1>

  <div class="buttons">
    <button id="yes" onclick="yesClicked()">Yes 💕</button>
    <button id="no" onmouseover="moveNo()">No 😢</button>
  </div>
</div>

<script>
let yesSize = 18;

function moveNo() {
  const noBtn = document.getElementById("no");

  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 100);

  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";

  yesSize += 6;
  document.getElementById("yes").style.fontSize = yesSize + "px";
}

function yesClicked() {
  document.body.innerHTML = `
    <div style="
      display:flex;
      justify-content:center;
      align-items:center;
      height:100vh;
      background:linear-gradient(135deg,#ff4d6d,#ff8fa3);
      color:white;
      font-family:Arial;
      text-align:center;
      flex-direction:column;
    ">
      <h1>YAY Happiness!!! 💕</h1>
      <h2>You just made me the happiest 😍</h2>
      <h3>Happy Valentine’s Day ❤️</h3>
    </div>
  `;
}
</script>

</body>
</html>
