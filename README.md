* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;

  background: #0d160d;
  color: #dfffdf;

  font-family: Georgia, serif;
}

.container {
  width: min(95%, 650px);
  text-align: center;
}

h1 {
  font-size: 38px;
  margin-bottom: 25px;
  color: #9acd32;
}

.wheel-area {
  position: relative;
  width: 500px;
  max-width: 90vw;
  aspect-ratio: 1;
  margin: auto;
}

#wheel {
  width: 100%;
  height: 100%;
  border-radius: 50%;

  box-shadow:
    0 0 0 8px #1d351d,
    0 0 30px rgba(154, 205, 50, 0.35);
}

.pointer {
  position: absolute;
  z-index: 5;

  left: 50%;
  top: -18px;

  transform: translateX(-50%);

  font-size: 42px;
  color: #9acd32;

  text-shadow: 0 0 10px #000;
}

button {
  margin-top: 25px;

  padding: 13px 30px;

  border: 2px solid #9acd32;
  border-radius: 12px;

  background: #162516;
  color: #dfffdf;

  font-family: Georgia, serif;
  font-size: 18px;
  font-weight: bold;

  cursor: pointer;

  transition: 0.2s;
}

button:hover {
  background: #9acd32;
  color: #0d160d;
  transform: scale(1.05);
}

button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  transform: none;
}

#result {
  min-height: 30px;
  margin: 20px 0;

  font-size: 23px;
  color: #9acd32;
}

.choices {
  margin-top: 30px;
}

.choices h2 {
  color: #9acd32;
}

textarea {
  width: 90%;
  height: 120px;

  padding: 12px;

  resize: vertical;

  border: 2px solid #315431;
  border-radius: 10px;

  background: #111d11;
  color: #dfffdf;

  font-family: Georgia, serif;
  font-size: 16px;
}

textarea:focus {
  outline: none;
  border-color: #9acd32;
}

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Wheel Spinner 🎡</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>

  <div class="container">

    <h1>🎡 Wheel Spinner</h1>

    <div class="wheel-area">

      <div class="pointer">▼</div>

      <canvas id="wheel" width="500" height="500"></canvas>

    </div>

    <button id="spinButton">SPIN ✨</button>

    <p id="result">Click the button to spin!</p>

    <div class="choices">
      <h2>Choices</h2>

      <textarea id="choicesInput">Green
Pink
Purple
Blue
Yellow
Orange</textarea>

      <button id="updateButton">Update Wheel</button>
    </div>

  </div>

  <script src="script.js"></script>

</body>
</html>
