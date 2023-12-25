# ODD23-24-WT-JavaScript
## Ex-09(a)
 # AIM
Create a form with java script code to calculate electricity bill.

# DESIGN STEPS: 9(a)

# Step 1:
Input Units Consumed: Prompt the user to enter the number of units consumed. This can be done using a Scanner object in Java.

# Step 2:
Set Rate Per Unit: Define a variable for the rate per unit of electricity. This will be a constant value that you can set according to the electricity rates in your area.

# Step 3:
Calculate Bill: Multiply the number of units consumed by the rate per unit to calculate the total bill.

# Step 4:
Display Bill: Print the calculated bill to the console.

# CODE (9a):
```
<html>
<head>
<script type="text/javascript">
function calc()
{
var prev,curr,units,amt;
prev=Number(document.getElementById("t1").value);
curr=Number(document.getElementById("t2").value);
units=curr-prev;
if(units<=100)
	amt=100;
else if(units>100&&units<=300)
	amt=100+(units-100)*3;
else
	amt=100+600+(units-300)*5;
document.getElementById("t3").value=amt;
}
</script>
</head>
<body>
<h2>Electricity Bill</h2>
<form>
Enter Previous Reading :
<input type="text" id="t1">
<br>
<br>

Enter Current Reading:
<input type="text" id="t2">
<br>
<br>

<input type="button"  onclick="calc()" value="Generate Bill">
<input type="text" id="t3">
</form>
</body>
</html>

```
# OUTPUT (9a):

![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/fcff9d0a-5d10-4f59-bce5-cfcf980d3d4a)


# Ex-09(b) :

# AIM
Develop a JavaScript program to compute the factorial of a given number without recursion.

# DESIGN STEPS: 9(b)

# Step 1:
Initialize a variable result to 1. This will hold the final factorial value.

# Step 2:
Start a loop from 2 to the given number n.

# Step 3:
In each iteration of the loop, multiply the current number i with result and update result.

# Step 4:
After the loop ends, result will hold the factorial of n. Return result.

# CODE(9b) :

```
<html>
<head>
<script type="text/javascript">
function show()
{
var i, n, fact;
fact=1;
n=Number(document.getElementById("num").value);
for(i=1; i<=n; i++)  
{
fact= fact*i;
}  
document.getElementById("answer").value= fact;
}
</script>
</head>
<body>
<form>
Enter Factorial Number
<br>
<br>
Enter Number: <input type="text" id="num">
<br>
<br>
<button onclick="show()">Factorial</button>
<input type="text" id="answer">
</form>
</body>
</html>

```
## OUTPUT (9b): 

![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/8b969f12-ff4a-488b-8bbd-f4ccff6e9a2a)


# Ex-09(c)
# AIM
Construct a JavaScript code to generate ‘N’ prime numbers.

# DESIGN STEPS: 9(c)

# Step 1:
Initialize a count variable to keep track of the number of prime numbers generated.

# Step 2:
Start from the number 2 (the first prime number), and for each number, check if it is prime.

# Step 3:
If the number is prime, increment the count and print the number.

# Step 4:
Repeat steps 2 and 3 until ‘N’ prime numbers have been generated.

# CODE(9c):

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prime Number Generator</title>
  <script>
    function generatePrimes(N) {
      const primes = [];
      let num = 2;

      while (primes.length < N) {
        if (isPrime(num)) {
          primes.push(num);
        }
        num++;
      }

      return primes;
    }

    function isPrime(num) {
      for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) {
          return false;
        }
      }
      return num > 1;
    }

    function displayPrimes() {
      const N = document.getElementById('inputN').value;
      const primeNumbers = generatePrimes(N);

      const resultContainer = document.getElementById('result');
      resultContainer.textContent = `The first ${N} prime numbers are: ${primeNumbers.join(', ')}`;
    }
  </script>
</head>
<body>
  <h1>Prime Number Generator</h1>
  
  <label for="inputN">Enter the value of N:</label>
  <input type="number" id="inputN" min="1" value="10">
  <button onclick="displayPrimes()">Generate Primes</button>

  <p id="result"></p>
</body>
</html>
```

## OUTPUT (9c):

![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/64348327-aa21-46b5-bdfa-89826ead3ca3)


# DESIGN STEPS: 9(d)

# Step 1:
Define a function for each operation (addition, subtraction, multiplication, division) that takes two numbers as input and returns the result of the operation.

# Step 2:
Define a function calculate that takes three parameters: two numbers and an operator.operation function based on the operator provided.

# Step 3:
Call the calculate function with the numbers and operator as arguments to perform a calculation.

# Step 4:
Print the result of the calculation.

# CODE(9d):
```
<!DOCTYPE html>
<html>
<body>

<h2>Simple Calculator</h2>

<input id="num1" type="number" placeholder="Number 1">
<input id="num2" type="number" placeholder="Number 2">

<button onclick="add()">Add</button>
<button onclick="subtract()">Subtract</button>
<button onclick="multiply()">Multiply</button>
<button onclick="divide()">Divide</button>

<p id="result"></p>

<script>
function add() {
    var num1 = document.getElementById("num1").value;
    var num2 = document.getElementById("num2").value;
    var result = Number(num1) + Number(num2);
    document.getElementById("result").innerHTML = "Addition Result: " + result;
}
function subtract() {
    var num1 = document.getElementById("num1").value;
    var num2 = document.getElementById("num2").value;
    var result = num1 - num2;
    document.getElementById("result").innerHTML = "Subtraction Result: " + result;
}

function multiply() {
    var num1 = document.getElementById("num1").value;
    var num2 = document.getElementById("num2").value;
    var result = num1 * num2;
    document.getElementById("result").innerHTML = "Multiplication Result: " + result;
}

function divide() {
    var num1 = document.getElementById("num1").value;
    var num2 = document.getElementById("num2").value;
    if (num2 != 0) {
        var result = num1 / num2;
        document.getElementById("result").innerHTML = "Division Result: " + result;
    } else {
        document.getElementById("result").innerHTML = "Cannot divide by zero";
    }
}
</script>

</body>
</html>
```

## OUTPUT (9d):

![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/16455d27-6300-4d2a-8ae8-e999609f9aed)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/2c80df17-cdc6-413b-bfb4-4357a0a877b8)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/d9ca5c45-e59f-4f00-a9d7-869044052d9d)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/18aedd17-edc9-4f25-a3e1-20ae6b388c14)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/cc21275c-b697-43e1-96a0-16225bf642ab)


# Ex-09(e):

# AIM
Design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

# DESIGN STEPS: 9(e)

# Step 1:
User enters the text in the text area.

# Step 2:
User clicks on one of the buttons to perform an operation (capitalize, lowercase, reverse).

# Step 3:
The JavaScript function corresponding to the operation is executed. This function gets the text from the text area, performs the operation, and updates the result paragraph with the new text.

# Step 4:
The result is displayed on the webpage. The user can perform more operations or enter new text. The process repeats from Step 2.

# CODE(9e):

```
<html>
<head>
<script type="text/javascript">
function f1()
{
document.getElementById("num").style.fontWeight="bold";
}
function f2()
{
document.getElementById("num").style.fontStyle="italic";
}
function f3()
{
document.getElementById("num").style.textTransform="uppercase";
}
function f4()
{
document.getElementById("num").style.textTransform="lowercase";
}
function f5()
{
document.getElementById("num").style.textTransform="capitalize";
}
function f6()
{
document.getElementById("num").style.textAlign="right";
}
function f7()
{
document.getElementById("num").style.textAlign="left";
}
function f8()
{
    document.getElementById("num").style.textAlign="center";
}
function f9()
{
document.getElementById("num").style.fontWeight = "normal";
document.getElementById("num").style.textAlign = "left";
document.getElementById("num").style.fontStyle = "normal";
}
</script>
</head>
<body>
    <textarea rows="10" cols="90" id="num">
         This is an javascript text area
        </textarea>
        <br>

<form>
    <br>
<input type="button" onclick="f1()"  value="Bold">
<input type="button" onclick="f2()"  value="Italics">
<input type="button" onclick="f3()"  value="All Caps">
<input type="button" onclick="f4()"  value="Small Caps">
<input type="button" onclick="f5()"  value="Title Case">
<input type="button" onclick="f6()"  value="Align Right">
<input type="button" onclick="f7()"  value="Align Left">
<input type="button" onclick="f8()"  value="Align Center">
<input type="button" onclick="f9()"  value="Clear Formatting">

</form>
</body>
</html>

```
## OUTPUT (9e):

![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/9e77961a-5362-4dc7-acc3-d1a6cc2647df)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/1197c798-c3eb-44cd-b004-97fc10cac0b5)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/704746b1-af60-4e57-b335-1a7716322202)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/b3f6ed23-a4ad-4cf7-9290-1dca20ed879e)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/adc4b8a8-2cec-4d3f-b3b1-db411558d333)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/0a3b0d61-e792-49cd-a3fb-2abcf18de45d)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/da26a713-c0eb-43da-b319-59a1c0f4685c)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/87414485-a02c-435e-9bd9-e2bdf24b72ad)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/3f7de93e-d913-47d6-8157-640697d5c68c)
![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/0b6ea8f2-06c9-43ac-aa65-b783f25ebf1e)


# Ex-09(f):

# AIM
Design a JavaScript program which displays error messages when a field in form is entered incorrectly.

# DESIGN STEPS: 9(f)
# Step 1:
User fills out the form and clicks the “Submit” button.

# Step 2:
The validateForm function is executed. This function gets the values of the name and email fields.

# Step 3:
The function checks if the name and email fields are filled out and if the email is a valid email address. If a field is entered incorrectly, it sets the corresponding error message.

# Step 4:
The function updates the corresponding error message spans with the error messages. If a field is entered incorrectly, the error message is displayed on the webpage. The user can correct the errors and submit the form again. The process repeats from Step 2.

# CODE(9f):
```
<!DOCTYPE html>
<html>
<body>

<h2>Form Validation</h2>

<form id="myForm">
  <label for="name">Name:</label><br>
  <input type="text" id="name" name="name"><br>
  <span id="nameError" style="color:red"></span><br>
  <label for="email">Email:</label><br>
  <input type="text" id="email" name="email"><br>
  <span id="emailError" style="color:red"></span><br>
  <input type="button" value="Submit" onclick="validateForm()">
</form>

<script>
function validateForm() {
    var name = document.getElementById("name").value;
    var email = document.getElementById("email").value;
    var nameError = "";
    var emailError = "";

    if (name == "") {
        nameError = "Name must be filled out";
    }

    if (email == "") {
        emailError = "Email must be filled out";
    } else if (!email.includes("@")) {
        emailError = "Email must be a valid email address";
    }
    document.getElementById("nameError").innerHTML = nameError;
    document.getElementById("emailError").innerHTML = emailError;
}
</script>

</body>
</html>
```

## OUTPUT (9f):

 ![image](https://github.com/23008344/ODD23-24-WT-JavaScript/assets/145742655/0eaf28ce-3869-44f3-ad73-232a7eddb503)


