<!DOCTYPE html>
<html>
<head>
  <title>Do You Love Me?</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      padding-top: 100px;
      color: #fff;
    }

    h1 {
      font-size: 40px;
      text-shadow: 2px 2px 4px #000;
    }

    .btn {
      margin: 20px;
      padding: 15px 30px;
      font-size: 20px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    .yes {
      background-color: #28a745;
      color: white;
    }

    .no {
      background-color: #dc3545;
      color: white;
      position: absolute;
    }

    #loveGif {
      display: none;
      margin-top: 50px;
    }
  </style>
</head>
<body>
  <h1>Do you love me?</h1>
  <button class="btn yes" onclick="showLove()">Yes</button>
  <button class="btn no" id="noBtn" onclick="askAgain()">No</button>

  <div id="loveGif">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbWh1bzFqZjFseTVpY3dyajYzOWM5czlvdnI5c2liOXV4MmxxZ2Z2ZCZlcD12MV9naWZzX3NlYXJjaCZjdD1n/MQVp7b87KwWsQ/giphy.gif" width="200">
    <h2>I knew it... You love me!</h2>
  </div>

  <script>
    let noBtn = document.getElementById("noBtn");
    let noClicked = 0;

    function askAgain() {
      noClicked++;
      if (noClicked === 1) {
        document.querySelector("h1").innerText = "Ek baar aur soch lo...";
      } else {
        let x = Math.random() * (window.innerWidth - 100);
        let y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
      }
    }

    function showLove() {
      document.querySelector("h1").style.display = "none";
      document.querySelector(".yes").style.display = "none";
      noBtn.style.display = "none";
      document.getElementById("loveGif").style.display = "block";
    }
  </script>
</body>
</html>
