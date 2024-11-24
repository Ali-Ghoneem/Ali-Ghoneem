<!DOCTYPE html>
<html>
<head>
    <title>Calculator 
Made by Ali Ghoneem</title>
    <style>
        /* Add your CSS styles here */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        
        input[type="text"] {
            width: 200px;
            padding: 10px;
            margin: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        
        input[type="button"] {
            width: 50px;
            padding: 10px;
            margin: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #f0f0f0;
        }
    </style>
</head>
<body>
    <h1>Simple Calculator
Made By Ali Ghoneem</h1>
    <input type="text" id="result" readonly>
    <br>
    <input type="button" value="1" onclick="display('1')">
    <input type="button" value="2" onclick="display('2')">
    <input type="button" value="3" onclick="display('3')">
    <input type="button" value="+" onclick="display('+')">
    <br>
    <input type="button" value="4" onclick="display('4')">
    <input type="button" value="5" onclick="display('5')">
    <input type="button" value="6" onclick="display('6')">
    <input type="button" value="-" onclick="display('-')">
    <br>
    <input type="button" value="7" onclick="display('7')">
    <input type="button" value="8" onclick="display('8')">
    <input type="button" value="9" onclick="display('9')">
    <input type="button" value="*" onclick="display('*')">
    <br>
    <input type="button" value="0" onclick="display('0')">
    <input type="button" value="C" onclick="clearResult()">
    <input type="button" value="=" onclick="calculate()">
    <input type="button" value="/" onclick="display('/')">
    
    <script>
        function display(value) {
            document.getElementById("result").value += value;
        }

        function clearResult() {
            document.getElementById("result").value = "";
        }

        function calculate() {
            let expression = document.getElementById("result").value;
            let result = eval(expression);
            document.getElementById("result").value = result;
        }
    </script>
</body>
</html>
