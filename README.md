# Ex.08 Design of a Standard Calculator
## Date:23.12.2023

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
```
<!DOCTYPE html>
<html>
<head>
  <title>Advanced Calculator</title>
  <style>


 

    .calculator {
  width: 8cm; 
  margin: 50px auto;
  border: 2px solid black;
  padding: 10px;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  font-family: Arial, sans-serif;
}

#display {
  width: calc(100% - 20px);
  margin-bottom: 20px;
  padding: 10px;
  font-size: 20px;
  border: 1px solid black;
  border-radius: 5px;
  height: 4cm;
  background-color: #fadbd5;
  
}


.keys {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 5px;
 
}

.keys button {
  width: 100%;
  height: 50px;
  font-size: 18px;
  border:none;
  
  border-radius: 3px;
  cursor: pointer;
  background-color: #f4e1d2;
  transition: background-color 0.3s ease;
}

.keys button:hover {
  background-color: #e0bab3;
}
 


.calculator button:nth-child(1),
.calculator button:nth-child(2),
.calculator button:nth-child(3) {
  background-color: #bc5a45;
}
                                                                   

.calculator button:nth-child(4),
.calculator button:nth-child(8),
.calculator button:nth-child(12),
.calculator button:nth-child(16),
.calculator button:nth-child(20) {
 background-color: #f18973;
}
.calculator button {
  background-color: #ffaaa5;
}
.bottomdiv{
            	    color:black;
            	    text-align: center;
                    position:relative;
           }
 body {
                background-color:#ebd5d5;
            }


  </style>
</head>
<body>
  <div class="bottomdiv">
    <h1> ATCHAYA CALCULATOR</h1>
    <h1>Register no: 212223220011</h1>
  </div>
  
  <div class="calculator">
    <input type="text" id="display" readonly>
    <div class="keys">
      <button onclick="clearDisplay()">C</button>
      <button onclick="appendToDisplay('log')">log</button>
      <button onclick="backspace()">&larr;</button>
      <button onclick="appendToDisplay('sqrt')">&radic;</button>
      <button onclick="appendToDisplay('7')">7</button>
      <button onclick="appendToDisplay('8')">8</button>
      <button onclick="appendToDisplay('9')">9</button>
      <button onclick="appendToDisplay('/')">/</button>
      <button onclick="appendToDisplay('4')">4</button>
      <button onclick="appendToDisplay('5')">5</button>
      <button onclick="appendToDisplay('6')">6</button>
      <button onclick="appendToDisplay('*')">*</button>
      <button onclick="appendToDisplay('1')">1</button>
      <button onclick="appendToDisplay('2')">2</button>
      <button onclick="appendToDisplay('3')">3</button>
      <button onclick="appendToDisplay('-')">-</button>
      <button onclick="appendToDisplay('.')">.</button>
      <button onclick="appendToDisplay('0')">0</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendToDisplay('+')">+</button>
    </div>
  </div>

  <script>
    let display = document.getElementById('display');

      function appendToDisplay(value) {
      display.value += value;
    }
    

    function clearDisplay() {
      display.value = '';
    }

    function backspace() {
      display.value = display.value.slice(0, -1);
    }

    function calculate() {
      try {
        let expression = display.value.replace(/log/g, 'Math.log');
        display.value = new Function('return ' + expression)();
      } catch (error) {
        display.value = 'Error';
      }
    }
  </script>
</body>
</html>
```

## OUTPUT:
![Alt text](<Screenshot (43).png>)
![Alt text](<Screenshot (44).png>)



## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
