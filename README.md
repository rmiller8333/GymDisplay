<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Gym Dashboard</title>
  <style>
    body {
      margin: 0;
      background: #111;
      color: #fff;
      font-family: Arial, sans-serif;
      text-align: center;
    }
    #clock {
      font-size: 5em;
      margin-top: 40px;
    }
    img {
      margin-top: 30px;
      max-width: 80%;
      border-radius: 10px;
    }
    iframe {
      margin-top: 30px;
      border: none;
    }
  </style>
</head>
<body>
  <div id="clock"></div>

  <img src="https://via.placeholder.com/600x400?text=Workout+Plan" alt="Workout Plan">

  <iframe src="https://forecast7.com/en/38d96n94d38/greenwood/" width="300" height="250"></iframe>

  <script>
    function updateClock() {
      const now = new Date();
      document.getElementById('clock').innerText = now.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
    }
    setInterval(updateClock, 1000);
    updateClock();
  </script>
</body>
</html>
