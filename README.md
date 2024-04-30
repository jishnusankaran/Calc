# Ex.08 Design of a Standard Calculator
## Date:25-4-24

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

## calc.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>
        <center><h1>JISHNUPRIYAN S(212223240061)</h1></center>
    </div>
  <div class="calculator">
    <input type="text" id="display" readonly>
    <div class="keys">
      <button onclick="appendNumber('7')">7</button>
      <button onclick="appendNumber('8')">8</button>
      <button onclick="appendNumber('9')">9</button>
      <button onclick="appendOperator('+')">+</button>
      <button onclick="appendNumber('4')">4</button>
      <button onclick="appendNumber('5')">5</button>
      <button onclick="appendNumber('6')">6</button>
      <button onclick="appendOperator('-')">-</button>
      <button onclick="appendNumber('1')">1</button>
      <button onclick="appendNumber('2')">2</button>
      <button onclick="appendNumber('3')">3</button>
      <button onclick="appendOperator('*')">*</button>
      <button onclick="appendNumber('0')">0</button>
      <button onclick="clearDisplay()">C</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendOperator('/')">/</button>
       <button onclick="appendOperator('%')">%</button>
    </div>
  </div>
  <script src="index.js"></script>
</body>
</html>
```

## style.css
```
.calculator {
    width: 220px;
    margin: 50px auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 3px;
    text-align: center;
    background-color: #DE3163; /* Adding background color */
  }
  
  #display {
    width: 100%;
    margin-bottom: 10px;
    padding: 5px;
  }
  
  .keys {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
  }
  
  button {
    padding: 10px;
    font-size: 18px;
    background-color: #f0f0f0;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #ccc;
  }  
```

## index.js
```
let expression = '';

function appendNumber(num) {
  expression += num;
  updateDisplay();
}

function appendOperator(op) {
  expression += op;
  updateDisplay();
}

function clearDisplay() {
  expression = '';
  updateDisplay();
}

function calculate() {
  try {
    const result = eval(expression);
    document.getElementById('display').value = result;
    expression = result.toString();
  } catch (error) {
    document.getElementById('display').value = 'Error';
    expression = '';
  }
}

function updateDisplay() {
  document.getElementById('display').value = expression;
}
```

## OUTPUT:
![alt text](<Screenshot 2024-04-30 085520.png>)

![alt text](<Screenshot 2024-04-30 085536.png>)
## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
