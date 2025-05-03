<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>آلة حاسبة - رحاب محمد</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f7f7f7;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    .header {
      padding: 30px 0 10px 0;
      background-color: #ffffff;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
      margin-bottom: 20px;
    }

    .header h1 {
      margin: 0;
      font-size: 24px;
      color: #333;
    }

    .header p {
      margin: 5px 0 0 0;
      font-size: 18px;
      color: #555;
    }

    .calculator {
      background-color: #ffffff;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      display: inline-block;
      padding: 20px;
    }

    #display {
      width: 100%;
      height: 40px;
      font-size: 20px;
      text-align: right;
      padding-right: 10px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .row {
      display: flex;
      justify-content: center;
      margin-bottom: 5px;
    }

    .row .left, .row .right {
      display: flex;
      flex-direction: column;
    }

    .left button, .right button {
      width: 60px;
      height: 40px;
      margin: 3px;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      background-color: #e0e0e0;
      cursor: pointer;
    }

    .right button {
      background-color: #d0d0d0;
    }

    .left button:hover, .right button:hover {
      background-color: #c0c0c0;
    }

    .watermark {
      position: fixed;
      bottom: 10px;
      right: 10px;
      opacity: 0.3;
      font-size: 14px;
      font-family: 'Courier New', Courier, monospace;
    }
  </style>
</head>
<body>

  <div class="header">
    <h1>رحاب محمد</h1>
    <p>20232267</p>
  </div>

  <div class="calculator">
    <input type="text" id="display" disabled>

    <div class="row">
      <div class="left">
        <button onclick="press('7')">7</button>
        <button onclick="press('4')">4</button>
        <button onclick="press('1')">1</button>
        <button onclick="press('0')">0</button>
      </div>
      <div class="left">
        <button onclick="press('8')">8</button>
        <button onclick="press('5')">5</button>
        <button onclick="press('2')">2</button>
        <button onclick="clearDisplay()">C</button>
      </div>
      <div class="left">
        <button onclick="press('9')">9</button>
        <button onclick="press('6')">6</button>
        <button onclick="press('3')">3</button>
        <button onclick="calculate()">=</button>
      </div>
      <div class="right">
        <button onclick="press('/')">÷</button>
        <button onclick="press('*')">×</button>
        <button onclick="press('-')">−</button>
        <button onclick="press('+')">+</button>
      </div>
    </div>
  </div>

  <div class="watermark">Rehab</div>

  <script>
    function press(val) {
      document.getElementById('display').value += val;
    }

    function clearDisplay() {
      document.getElementById('display').value = '';
    }

    function calculate() {
      try {
        document.getElementById('display').value = eval(document.getElementById('display').value);
      } catch {
        document.getElementById('display').value = 'Error';
      }
    }
  </script>

</body>
</html>
