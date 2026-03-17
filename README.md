# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
## Calculator.js
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {

    const [input, setInput] = useState("");

    const handleClick = (value) => {
        setInput(input + value);
    };

    const clearDisplay = () => {
        setInput("");
    };

    const calculate = () => {
        try {
            setInput(eval(input).toString());
        } catch {
            setInput("Error");
        }
    };

    return (
        <div className="calculator">
            <h2>Simple Calculator</h2>

            <input
                type="text"
                value={input}
                readOnly
                className="display"
            />

            <div className="buttons">

                <button onClick={() => handleClick("7")}>7</button>
                <button onClick={() => handleClick("8")}>8</button>
                <button onClick={() => handleClick("9")}>9</button>
                <button onClick={() => handleClick("/")}>/</button>

                <button onClick={() => handleClick("4")}>4</button>
                <button onClick={() => handleClick("5")}>5</button>
                <button onClick={() => handleClick("6")}>6</button>
                <button onClick={() => handleClick("*")}>*</button>

                <button onClick={() => handleClick("1")}>1</button>
                <button onClick={() => handleClick("2")}>2</button>
                <button onClick={() => handleClick("3")}>3</button>
                <button onClick={() => handleClick("-")}>-</button>

                <button onClick={() => handleClick("0")}>0</button>
                <button onClick={clearDisplay}>C</button>
                <button onClick={calculate}>=</button>
                <button onClick={() => handleClick("+")}>+</button>

            </div>
        </div>
    );
}

export default Calculator;
```
## Calculator.css
```
body {
    background: linear-gradient(135deg, #667eea, #764ba2);
    font-family: Arial;
}

.calculator {
    width: 320px;
    margin: 100px auto;
    padding: 20px;
    background: white;
    border-radius: 10px;
    text-align: center;
}

.display {
    width: 100%;
    height: 50px;
    font-size: 20px;
    margin-bottom: 15px;
    text-align: right;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 10px;
}

button {
    padding: 15px;
    font-size: 18px;
    border: none;
    background: #667eea;
    color: white;
    border-radius: 5px;
}

button:hover {
    background: #764ba2;
}
```
## OUTPUT
<img width="542" height="640" alt="Screenshot 2026-03-16 161029" src="https://github.com/user-attachments/assets/60a599d9-7829-4e36-a5f9-ff6a5ba1acc1" />

<img width="661" height="733" alt="image" src="https://github.com/user-attachments/assets/6e21440a-e08f-48c1-8dc5-50db320b4fbe" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
