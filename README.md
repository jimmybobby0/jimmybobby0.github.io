<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Windows 98</title>

  <!-- 98.css -->
  <link rel="stylesheet" href="https://unpkg.com/98.css">

  <style>
    /* ============================
       CUSTOM WINDOWS 98 CURSORS
       ============================ */

    /* Normal pointer */
    body {
      cursor: url('arrow.cur'), auto;
    }

    /* Hover cursor */
    a:hover,
    .icon:hover,
    button:hover {
      cursor: url('cursor_15.cur'), auto;
    }

    /* Text cursor */
    input,
    textarea,
    [type="text"] {
      cursor: url('beam.cur'), auto;
    }

    /* Loading cursor */
    .wait,
    .loading,
    body.waiting {
      cursor: url('cursor_3.cur'), auto;
    }


    /* ============================
       WINDOWS 98 DESKTOP STYLES
       ============================ */

    body {
      margin: 0;
      height: 100vh;
      overflow: hidden;
      background: #008080;
      background-size: cover;
      font-family: "MS Sans Serif", Arial;
    }

    .icon {
      width: 90px;
      text-align: center;
      color: white;
      font-size: 14px;
      margin: 20px;
      cursor: default;
      user-select: none;
    }

    .icon img {
      width: 64px;
      height: 64px;
      image-rendering: pixelated;
    }

    .taskbar {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 40px;
      background: #c0c0c0;
      border-top: 2px solid white;
      display: flex;
      align-items: center;
      padding: 4px;
    }

    .start-button {
      margin-left: 4px;
    }

    .taskbar-clock {
      margin-left: auto;
      margin-right: 10px;
      background: white;
      padding: 4px 8px;
      border: 2px inset #808080;
      font-size: 14px;
    }

    .desktop {
      display: flex;
      flex-direction: column;
      padding: 10px;
    }
  </style>
</head>

<body>

  <!-- Desktop icons -->
  <div class="desktop">

    <div class="icon">
      <img src="oldpcwin98.webp">
      <div>My Computer</div>
    </div>

    <div class="icon">
      <img src="olddocwin98.webp">
      <div>Documents</div>
    </div>

    <div class="icon">
      <img src="oldbrowwin98.webp">
      <div>Browser</div>
    </div>

    <div class="icon">
      <img src="oldnotewin98.webp">
      <div>Notes</div>
    </div>

  </div>

  <!-- Taskbar -->
  <div class="taskbar">
    <button class="start-button">Start</button>
    <div class="taskbar-clock" id="clock">00:00</div>
  </div>

  <script>
    // Windows 98 clock
    function updateClock() {
      const now = new Date();
      let h = now.getHours();
      let m = now.getMinutes();
      if (m < 10) m = "0" + m;
      document.getElementById("clock").textContent = h + ":" + m;
    }
    setInterval(updateClock, 1000);
    updateClock();
  </script>

</body>
</html>
