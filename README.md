<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Proposal Box</title>
  <style>
    body {
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #ffe6eb;
      font-family: Arial, sans-serif;
    }

    .box {
      background: white;
      padding: 30px 40px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      position: relative;
    }

    h2 {
      margin-bottom: 25px;
      color: #e6005c;
    }

    button {
      padding: 10px 25px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin: 10px;
    }

    #yes {
      background: #ff4d88;
      color: white;
    }

    #no {
      background: #999;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="box" id="box">
    <h2>Do you love me? ❤️</h2>
    <button id="yes">Yes</button>
    <button id="no">No</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const box = document.getElementById("box");

    function moveNoButton() {
      const boxRect = box.getBoundingClientRect();

      const x = Math.random() * (boxRect.width - 80);
      const y = Math.random() * (boxRect.height - 40);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    // Move on hover (desktop)
    noBtn.addEventListener("mouseover", moveNoButton);

    // Move on touch (mobile)
    noBtn.addEventListener("touchstart", moveNoButton);

    document.getElementById("yes").addEventListener("click", () => {
      alert("Aww! ❤️");
    });
  </script>

</body>
</html>
