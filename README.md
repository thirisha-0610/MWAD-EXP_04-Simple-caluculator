# MWAD-EXP_04-Simple-caluculator
## Date:30/4/25
# Name: Thirisha A
# Reg no: 212223040228

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
```
import React, { useState } from "react";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleDelete = () => {
    setInput(input.slice(0, -1));
  };

  const handleCalculate = () => {
    try {
      const result = Function(`return ${input}`)();
      setInput(result.toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div>
      <h1>Simple Calculator</h1>
    <div>
      <h1></h1>
    </div>
    <div style={styles.page}>
      <div className="calculator" style={styles.calculator}>
        <input
          type="text"
          value={input}
          readOnly
          style={styles.display}
          placeholder="0"
        />
        <div style={styles.buttons}>
          <button onClick={handleClear} style={styles.button}>C</button>
          <button onClick={handleDelete} style={styles.button}>DEL</button>
          <button onClick={() => handleClick("/")} style={styles.button}>/</button>
          <button onClick={() => handleClick("*")} style={styles.button}>*</button>

          <button onClick={() => handleClick("7")} style={styles.button}>7</button>
          <button onClick={() => handleClick("8")} style={styles.button}>8</button>
          <button onClick={() => handleClick("9")} style={styles.button}>9</button>
          <button onClick={() => handleClick("-")} style={styles.button}>-</button>

          <button onClick={() => handleClick("4")} style={styles.button}>4</button>
          <button onClick={() => handleClick("5")} style={styles.button}>5</button>
          <button onClick={() => handleClick("6")} style={styles.button}>6</button>
          <button onClick={() => handleClick("+")} style={styles.button}>+</button>

          <button onClick={() => handleClick("1")} style={styles.button}>1</button>
          <button onClick={() => handleClick("2")} style={styles.button}>2</button>
          <button onClick={() => handleClick("3")} style={styles.button}>3</button>
          <button
            onClick={handleCalculate}
            style={{
              ...styles.button,
              gridRow: "span 2",
              backgroundColor: "#27ae60",
              color: "white",
              fontWeight: "bold",
            }}
          >
            =
          </button>

          <button onClick={() => handleClick("0")} style={{ ...styles.button, gridColumn: "span 2" }}>
            0
          </button>
          <button onClick={() => handleClick(".")} style={styles.button}>.</button>
        </div>
      </div>
    </div>
    </div>
  );
}

const styles = {
  page: {
    height: "100vh",
    width:"190vh",
    background: "linear-gradient(135deg, #1e272e, #485460)",
    display: "flex",
    justifyContent: "center",
    alignItems: "center",

  },
  div:
  {
    textAlign:"center",

  },
  calculator: {
    width: 330,
    padding: 25,
    borderRadius: 20,
    background: "#222831",
    boxShadow: "0 0 20px 6px #00adb5",
  },
  display: {
    width: "95%",
    height: 60,
    fontSize: 32,
    marginBottom: 20,
    textAlign: "right",
    paddingRight: 15,
    borderRadius: 12,
    border: "none",
    color: "#000000",
    backgroundColor: "#ffffff",
    fontWeight: "600",
    boxShadow: "inset 2px 2px 6px #ccc",
  },
  buttons: {
    display: "grid",
    gridTemplateColumns: "repeat(4, 1fr)",
    gridGap: 12,
  },
  button: {
    height: 60,
    fontSize: 22,
    borderRadius: 12,
    border: "none",
    backgroundColor: "#eeeeee",
    color: "#000000", // black button text
    cursor: "pointer",
    userSelect: "none",
    transition: "background-color 0.3s ease",
    boxShadow: "0 4px 8px rgba(0,0,0,0.15)",
  },
};

export default App;

```

## OUTPUT

![image](https://github.com/user-attachments/assets/212693ae-91d6-4b0a-9d83-3227584d9ddf)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
