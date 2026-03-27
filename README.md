<!DOCTYPE html>
<html lang="en">
<head>
    <title> Javasciprt Button Example </title>
    <style>
     .note {
        color : green; 
        font-style: italic;
     }
    </style>
</head>
<body>
    <h1> All Javascript Button Samples</h1>

<div> 
    <button onclick="alert('Hello')"> Click Me For Alert </button>
</div>

<div> 
    <button onclick="sayHello()"> Click Me For Function </button>
</div>

<div> 
    <button onclick="changeText()"> Click to change text </button>
</div>

<div> 
    <button onclick="IncrementCounter()"> Click To Increase</button>
</div>

<div>
    <input type="text" id="nameInput" placeholder="Your Name here">
    <button onclick="greetUser()">Greet Me</button>
</div>

<div>
    <input type="number" id="ageInput" placeholder="Enter Age">
    <button onclick="checkAge()">Check Age</button>
</div>

<div>
    <input type="number" id="num1" placeholder="First Number">
    <input type="number" id="num2" placeholder="Second Number">

    <button onclick="addNumbers()">Add</button>
    <button onclick="subtractNumbers()">Subtract</button>
    <button onclick="multiplyNumbers()">Multiply</button>
    <button onclick="divideNumbers()">Divide</button>

    <div class="output" id="sumResult">Result: 0</div>
</div>
            <div id="light" style="background-color: gray; padding: 20px; text-align: center; border-radius: 5px; margin-bottom: 10px;">
                Light is OFF
            </div>
            <button onclick="toggleLight()">Toggle Light</button>
        </div>
</div>

<p id="output"></p>
<p id="demo"></p>
<p id="countDisplay"></p>
<p id="result"></p>
<p id="ageResult"></p>


<script>
    //Sample 2
    function sayHello(){
        let messege = "Hello from the Function";
        alert(messege);
        document.getElementById("output").innerHTML = messege;
        console.log("Sample 2: Button was Clicked");

    }

    // Sample 3
    function changeText(){
        document.getElementById("demo").innerHTML = 
           "The Text Has Changed! Button was Clicked at" + new Date().toLocaleString();
        console.log("Sample 3: Text Changed Succesfully");

    }

    //Sample 4
    let count = 0;
    
    function IncrementCounter() {
       count++;
       document.getElementById("countDisplay").innerHTML = count;
       console.log("Sample 4: Count =" + count);   

    }

    //Sample 5
    function greetUser() {
        let name = document.getElementById("nameInput").value;

        if (name === "") {
            name = "Guest";
        }
 
       let message = "Hello, " + name + "!";
       document.getElementById("result").innerHTML = message;
       console.log("Sample 5:" + message );
    }

    //Sample 6
    function checkAge() {
        let age = document.getElementById("ageInput").value;
        let result;

        if (age >= 18) {
            result = "You Are older than 18! (Age: " + age + ")";
            console.log("Sample 6: Adult - " + age);
        } 
        else {
            result = "You Are Younger than 18! (Age: "+ age +")";
            console.log("Sample 6: Minor - " + age);
        }
        
        document.getElementById("ageResult").innerHTML = result;
    }

    //Sample 7 
    function addNumbers() {
        let a = Number(document.getElementById("num1").value);
        let b = Number(document.getElementById("num2").value);
        let result = a + b;
        document.getElementById("sumResult").innerHTML = "Result: " + result;
        console.log("Add: " + result);
    }

    function subtractNumbers() {
        let a = Number(document.getElementById("num1").value);
        let b = Number(document.getElementById("num2").value);
        let result = a - b;
        document.getElementById("sumResult").innerHTML = "Result: " + result;
        console.log("Subtract: " + result);
    }

    function multiplyNumbers() {
        let a = Number(document.getElementById("num1").value);
        let b = Number(document.getElementById("num2").value);
        let result = a * b;
        document.getElementById("sumResult").innerHTML = "Result: " + result;
        console.log("Multiply: " + result);
    }

    function divideNumbers() {
        let a = Number(document.getElementById("num1").value);
        let b = Number(document.getElementById("num2").value);
        if (b === 0) {
            document.getElementById("sumResult").innerHTML = "Error: Cannot divide by zero";
            console.log("Divide: Error - division by zero");
        } else {
            let result = a / b;
            document.getElementById("sumResult").innerHTML = "Result: " + result;
            console.log("Divide: " + result);
        }
        let isLightOn = false;
            function toggleLight() {
                isLightOn = !isLightOn;

                let light = document.getElementById("light");

                if(isLightOn) {
                    light.innerHTML = "Light is On";
                    light.style.backgroundColor = "red";
                    light.style.color = "black";
                } else {
                    light.innerHTML = "Light is OFF";
                    light.style.backgroundColor = "gray";
                    light.style.color = "white";
                }

    }
    }

</script>

</body>
</html>
