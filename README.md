<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Fathima ❤️ Sulaim | Love Calculator</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 50%, #fbc2eb 100%);
      padding: 20px;
      overflow-x: hidden;
    }

    .box {
      background: rgba(255, 255, 255, 0.95);
      padding: 35px 25px;
      border-radius: 25px;
      width: 100%;
      max-width: 360px;
      text-align: center;
      box-shadow: 0 15px 40px rgba(255, 75, 110, 0.3);
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      color: #ff4b6e;
      font-size: 24px;
      margin-bottom: 6px;
    }

    .subtitle {
      color: #888;
      font-size: 13px;
      margin-bottom: 20px;
    }

    .names {
      font-size: 17px;
      color: #333;
      margin-bottom: 20px;
      font-weight: 600;
    }

    .names span {
      color: #ff4b6e;
    }

    input {
      padding: 12px;
      margin: 7px 0;
      width: 100%;
      border-radius: 12px;
      border: 2px solid #ffd6de;
      font-size: 15px;
      outline: none;
      transition: 0.3s;
    }

    input:focus {
      border-color: #ff4b6e;
      box-shadow: 0 0 8px rgba(255, 75, 110, 0.3);
    }

    button {
      background: linear-gradient(135deg, #ff4b6e, #ff7a9c);
      color: white;
      padding: 13px 25px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      font-size: 16px;
      font-weight: 600;
      width: 100%;
      margin-top: 12px;
      transition: 0.3s;
      box-shadow: 0 5px 15px rgba(255, 75, 110, 0.4);
    }

    button:active {
      transform: scale(0.97);
    }

    #result {
      margin-top: 22px;
      font-size: 18px;
      color: #333;
      font-weight: 600;
      line-height: 1.6;
      min-height: 50px;
    }

    .score {
      font-size: 42px;
      color: #ff4b6e;
      font-weight: 800;
      display: block;
      margin: 5px 0;
    }

    .hearts {
      font-size: 22px;
      margin-top: 10px;
      animation: pulse 1.2s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.15); }
    }

    .footer {
      margin-top: 20px;
      font-size: 12px;
      color: #aaa;
    }

    .footer strong {
      color: #ff4b6e;
    }
  </style>
</head>
<body>
  <div class="box">
    <h1>💖 Love Calculator 💖</h1>
    <p class="subtitle">Happy 2nd Monthsary!</p>

    <p class="names">
      <span>Fathima Sharafa</span> &nbsp;❤️&nbsp; <span>Sulaim Ahamed</span>
    </p>

    <input type="text" id="name1" placeholder="Your Name (Fathima)" />
    <input type="text" id="name2" placeholder="Husband Name (Sulaim)" />

    <button onclick="calculate()">Calculate Love 💘</button>

    <div id="result"></div>

    <div class="footer">
      Made with ❤️ by <strong>Fathima</strong> for <strong>Sulaim</strong><br />
      18.09.2026 — Our Special Day
    </div>
  </div>

  <script>
    function calculate() {
      let n1 = document.getElementById("name1").value.trim().toLowerCase();
      let n2 = document.getElementById("name2").value.trim().toLowerCase();

      if (n1 === "" || n2 === "") {
        document.getElementById("result").innerHTML =
          "Please enter both names 😅";
        return;
      }

      // Always show 100% for the special couple 💕
      let score = 100;

      let msg = "";
      if (score === 100) {
        msg = "Perfect Match! Soulmates Forever 💞";
      } else if (score >= 95) {
        msg = "Made for each other 💖";
      } else if (score >= 85) {
        msg = "Strong love growing 💕";
      } else {
        msg = "Love is in the air 💗";
      }

      document.getElementById("result").innerHTML =
        "<span class='score'>" + score + "%</span>" +
        msg +
        "<div class='hearts'>❤️ 💖 💕 💘 ❤️</div>" +
        "<div style='font-size:14px;color:#888;margin-top:10px;'>" +
        "Happy 2nd Monthsary, My Love! <br>18.09.2026 🎉" +
        "</div>";
    }
  </script>
</body>
</html>