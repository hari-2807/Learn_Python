# Day 1: Working with Variables in Python to Manage Data

## 🎯 Goal
Build a **Band Name Generator** while mastering the basic mechanics of Python, including printing, inputting, and variable management.

---

## 📖 Lessons & Key Concepts

### 1. Printing and Strings
The `print()` function is used to output data to the console. Text must be wrapped in **Double Quotes `""`** to be recognized as a **String**.

* **String Concatenation:** Combining strings using the `+` sign.
    * *Example:* `"Hello" + " " + "World"` becomes `"Hello World"`.
* **New Line Character:** Use `\n` inside a string to move the text to the next line.

### 2. The Input Function
The `input()` function allows the user to provide data to the program.
* **Flow:** The program prints the prompt $\rightarrow$ Pauses for user entry $\rightarrow$ Returns the user's text.
* **Nesting:** You can wrap an input inside a print statement: 
  `print("Hello " + input("What is your name?"))`

### 3. Python Variables
Variables are used to "save" data so we can use it later. 
* **Assignment:** Use the `=` operator to assign a value to a name.
* **Naming Rules:**
    1. **No Spaces:** Use underscores (e.g., `user_name`).
    2. **No Starting Numbers:** Must start with a letter (e.g., `length1` is okay, `1length` is not).
    3. **Keywords:** Avoid using names like `print` or `input`.
    4. **Case-Sensitive:** `Name` and `name` are different variables.

### 4. Debugging & Error Types
* **SyntaxError:** Code "grammar" is broken (e.g., missing a quote).
* **IndentationError:** Unexpected spaces at the start of a line.
* **NameError:** Using a variable name that hasn't been defined or is misspelled.

---

## 🛠️ Final Project: Band Name Generator
This project combines all the day's skills into a functional script.

### The Logic
1. Create a greeting.
2. Ask for the user's city and store it in a variable.
3. Ask for the user's pet name and store it in a variable.
4. Combine them (Concatenation) and display the result.

### Final Code
```python
print("Welcome to the Band Name Generator.")
city = input("What's the name of the city you grew up in?\n")
pet = input("What's your pet's name?\n")
print("Your band name could be " + city + " " + pet)
