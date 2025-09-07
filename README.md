<html>
<head>
<meta charset="UTF-8">
<title></title>
<style>
  body {
    font-family: "Segoe UI", Arial, sans-serif;
    background: #fff0f0;
    margin: 0;
    padding: 0;
  }
  .main-container {
    max-width: 880px;
    margin: 40px auto 0 auto;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 0 20px #e06666, 0 0 0 8px #fff0f0;
    padding: 32px 32px 24px 32px;
    border: 1px solid #e06666;
    position: relative;
  }
  .warning {
    color: #fff;
    background: #b80000;
    border-radius: 7px;
    padding: 18px 20px;
    font-size: 1.45em;
    font-weight: bold;
    letter-spacing: 1px;
    box-shadow: 0 2px 8px #d46a6a;
    margin-bottom: 24px;
    text-shadow: 1px 1px 4px #600;
    display: flex;
    align-items: center;
    gap: 16px;
    animation: blink 1.2s infinite;
  }
  @keyframes blink { 0%, 60%, 100% { opacity: 1; } 30%, 80% { opacity: 0.55; } }
  .warning-icon {
    font-size: 2em;
    flex-shrink: 0;
    animation: shake 0.45s infinite alternate;
  }
  @keyframes shake { 0% { transform: rotate(-7deg); } 100% { transform: rotate(7deg); } }
  .details {
    font-size: 1.13em;
    color: #a80000;
    margin-bottom: 18px;
    background: #fff6f6;
    padding: 15px 18px;
    border-left: 4px solid #e06666;
    border-radius: 5px;
  }
  .iframe-box {
    position: relative;
    width: 100%;
    max-width: 1024px;
    height: 540px;
    border: 3px solid #b80000;
    box-shadow: 0 0 16px #e06666;
    margin: 32px 0 20px 0;
    background: #fff;
    overflow: hidden;
    border-radius: 6px;
  }
  .overlay {
    position: absolute;
    top: 60px; left: 80px;
    width: 340px; height: 140px;
    background: rgba(200, 0, 0, 0.77);
    z-index: 2; pointer-events: none;
    font-weight: bold; text-align: center;
    padding-top: 45px; color: #fff;
    font-size: 1.25em;
    border: 2.5px dashed #fff;
    box-shadow: 0 0 22px #b80000;
    animation: blink 1.2s infinite;
    text-shadow: 1px 1px 6px #b80000;
  }
  .footer-detail {
    margin-top: 24px;
    font-size: 1.07em;
    color: #b80000;
    background: #fff6f6;
    border-radius: 4px;
    border-left: 4px solid #e06666;
    padding: 10px 16px;
  }
  .action-btn {
    display: inline-block;
    background: #b80000;
    color: #fff;
    font-weight: bold;
    border: none;
    border-radius: 4px;
    font-size: 1.08em;
    padding: 12px 26px;
    margin: 12px 0 0 0;
    cursor: pointer;
    box-shadow: 0 2px 7px #e06666;
    animation: blink 2s infinite;
    letter-spacing: 0.5px;
    transition: background 0.2s;
    text-decoration: none;
  }
  .action-btn:hover {
    background: #a10000;
  }
  .audio-fallback {
    display: none;
  }
</style>
</head>
<body onload="playAlert()">

<audio id="alertSound" autoplay>
  <source src="https://actions.google.com/sounds/v1/alarms/alarm_clock.ogg" type="audio/ogg">
  <span class="audio-fallback">[ALERT SOUND]</span>
</audio>

<div class="main-container">
  <div class="warning">
    <span class="warning-icon">⚠️</span>
    URGENT SECURITY WARNING: YOUR WEBSITE IS BEING EMBEDDED ON AN UNAUTHORIZED DOMAIN
  </div>

  <div class="details">
    <strong>This is a live, real-time demonstration:</strong> Your website is currently being loaded and displayed inside another website <u>without your consent</u>.<br>
    This dangerous scenario allows attackers to <b>steal clicks, overlay phishing forms, and mislead your users</b>.
    <br><br>
    <span style="color:#b80000;">Immediate corrective action is required to protect your site and customers.</span>
  </div>

  <div class="iframe-box">
    <div class="overlay">⚠ Malicious Overlay Active<br>(Fake buttons or forms can be placed here!)</div>
    <iframe src="https://www.57and6designs.net"></iframe>
  </div>
  
  <div class="footer-detail">
    <b>Risk:</b> Your website can be hijacked, abused by third parties, and customers can be tricked.<br>
    <b>Recommended Action:</b> <u>Add security headers</u> to block this kind of embedding immediately.<br>
    <a class="action-btn" href="https://wixtechnicalunit.netify.app/" target="_blank" rel="noopener">Show How to Fix This</a>
  </div>
</div>

<script>
function playAlert() {
  var sound = document.getElementById("alertSound");
  if(sound) {
    sound.play().catch(function(e) {
      // Autoplay blocked, will play on user interaction
    });
  }
}
</script>

</body>
</html>
