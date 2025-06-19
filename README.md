<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MacroDroid Ultimate Web Controller</title>
  <meta name="description" content="Control your MacroDroid-connected Android device remotely without IP access.">
  <meta name="author" content="rareaddy3307abhi">
  <style>
    body {
      background: linear-gradient(to bottom right, #c471ed, #f7797d);
      font-family: Arial, sans-serif;
      text-align: center;
      color: white;
      padding: 20px;
    }
    .box {
      background-color: #1e1e1e;
      padding: 15px;
      margin: 10px auto;
      width: 340px;
      border-radius: 10px;
      box-shadow: 0 0 10px #00000088;
    }
    input, button, select {
      margin: 8px 0;
      padding: 10px;
      width: 90%;
      border-radius: 6px;
      border: none;
    }
    button {
      background-color: #ff0040;
      color: white;
      cursor: pointer;
    }
    .btn-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 20px;
    }
    .btn-grid button {
      width: 140px;
    }
    footer {
      margin-top: 40px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <h2>📲 MacroDroid Ultimate Web Controller</h2>

  <!-- All control boxes remain the same -->

  <!-- Your existing boxes and controls code -->

  <!-- Action Buttons Grid -->
  <div class="btn-grid">
    <!-- Buttons like Recent, Home, Wifi On, etc. -->
    <!-- ... existing buttons ... -->
  </div>

  <footer>
    <p>Note: Share this link to control devices without IP address. Make sure MacroDroid macro "Control Device Remotely" is running.</p>
    <p>Developed with ❤️ by rareaddy3307abhi</p>
  </footer>

  <script>
    function showAlert(type) {
      let message = '';
      switch(type) {
        case 'toast': message = document.getElementById('toastInput').value; break;
        case 'notification': message = `Title: ${document.getElementById('notiTitle').value}\nDesc: ${document.getElementById('notiDesc').value}`; break;
        case 'speak': message = document.getElementById('speakText').value; break;
        case 'floating': message = document.getElementById('floatingText').value; break;
        case 'paste': message = document.getElementById('pasteText').value; break;
        case 'dim': message = `Dim: ${document.getElementById('dimVal').value}`; break;
        case 'brightness': message = `Brightness: ${document.getElementById('brightnessVal').value}`; break;
        case 'variable': message = `Set ${document.getElementById('varName').value} = ${document.getElementById('varValue').value}`; break;
        case 'launchApp': message = `Launching: ${document.getElementById('appPackage').value}`; break;
        case 'openUrl': message = `Opening: ${document.getElementById('openUrl').value}`; break;
      }
      alert(`${type.toUpperCase()}\n${message}`);
    }

    function quickAction(actionName) {
      alert(`Triggering: ${actionName}`);
    }
  </script>

</body>
</html>
