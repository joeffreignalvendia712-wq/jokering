<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>hi-core — Reenvezx</title>
<style>
  body {
    background-color: #0b1120;
    color: #fff;
    font-family: 'Poppins', sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    text-align: center;
  }
  .card {
    background: #10182f;
    border-radius: 16px;
    padding: 30px;
    width: 320px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.5);
  }
  h2 {
    margin-bottom: 10px;
  }
  p {
    opacity: 0.8;
  }
  button {
    border: none;
    outline: none;
    padding: 12px 24px;
    border-radius: 10px;
    font-size: 16px;
    margin: 10px;
    cursor: pointer;
    font-weight: 600;
    transition: 0.2s;
  }
  .yes {
    background-color: #00c853;
    color: #fff;
  }
  .yes:hover {
    background-color: #00e676;
  }
  .no {
    background-color: #d32f2f;
    color: #fff;
  }
  .no:hover {
    background-color: #f44336;
  }
  .result {
    margin-top: 20px;
    font-size: 18px;
  }
</style>
</head>
<body>
  <div class="card">
    <h2 id="greet"></h2>
    <p>Could you please send me a picture to use as my profile picture in ML? 🥺</p>
    <div>
      <button class="yes" onclick="answer(true)">Yes ✅</button>
      <button class="no" onclick="answer(false)">No ❌</button>
    </div>
    <div class="result" id="result"></div>
  </div>

  <script>
    const greet = document.getElementById("greet");
    const hour = new Date().getHours();
    if (hour < 12) greet.innerText = "Good morning 🌅";
    else if (hour < 18) greet.innerText = "Good afternoon 🌞";
    else greet.innerText = "Good evening 🌙";

    function answer(isYes) {
      const result = document.getElementById("result");
      if (isYes) {
        result.innerHTML = "Yay! You said YES — Salamat! 🥰🎉";
      } else {
        result.innerHTML = "Aww 😢 You said NO — maybe next time.";
      }
    }
  </script>
</body>
</html>
