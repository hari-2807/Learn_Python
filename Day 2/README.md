# Day 2: Understanding Data Types and Manipulating Numbers

## 🎯 Goal
Build a **Tip Calculator** that can handle user input, perform mathematical calculations involving percentages, and format numerical output using f-strings.

---

## 📖 Lessons & Key Concepts

### 1. Python Primitive Data Types
Python categorizes data into four main primitive types. Understanding these prevents "Type Errors" when performing operations.



| Type | Name | Description | Example |
| :--- | :--- | :--- | :--- |
| **String** | `str` | Text wrapped in quotes. Support "Subscripting" (e.g., `"Hello"[0]`). | `"123"` |
| **Integer** | `int` | Whole numbers. Use underscores for readability. | `1_000_000` |
| **Float** | `float` | Numbers with decimal points. | `3.14159` |
| **Boolean** | `bool` | Logical values (True or False). | `True` |

### 2. Type Checking and Conversion
* **Type Check:** Use `type(variable_name)` to see the data type.
* **Type Conversion (Casting):** Manually changing data types using `str()`, `int()`, `float()`, or `bool()`.
    * *Example:* `str(123)` turns the number into the text `"123"`.

### 3. Mathematical Operations & PEMDAS
Python follows the mathematical order of operations.

1. **P**arentheses `()`
2. **E**xponents `**`
3. **M**ultiplication `*` & **D**ivision `/` (handled Left-to-Right)
4. **A**ddition `+` & **S**ubtraction `-` (handled Left-to-Right)



**Special Division:**
* `/` : Floating point division (always returns a decimal, e.g., `4 / 2 = 2.0`).
* `//`: Floor division (chops off decimals, e.g., `7 // 3 = 2`).

### 4. Number Manipulation
* **Rounding:** Use `round(number, ndigits)` to round to a specific decimal place.
    * *Example:* `round(2.666, 2)` becomes `2.67`.
* **Shorthand Assignment:** Update variables efficiently.
    * `score += 1` is the same as `score = score + 1`.

### 5. f-Strings
f-Strings provide an easy way to mix different data types into one string without manual conversion.



* **Syntax:** `f"Your score is {score}"`
* Python handles the conversion of the `{score}` integer into a string automatically behind the scenes.

---

## 🛠️ Final Project: Tip Calculator
The project applies type casting (converting input strings to floats) and complex math to solve a real-world problem.

### The Logic
1. Ask for the total bill (Float).
2. Ask for the tip percentage (Integer/Float).
3. Ask for the number of people (Integer).
4. Calculate: $Total \div People \times (1 + Tip\%)$
5. Round to 2 decimal places and output via an f-string.

### Final Code Snippet
```python
bill = float(input("What was the total bill? $"))
tip = int(input("Tip percentage? 10, 12, or 15? "))
people = int(input("How many people? "))

total_with_tip = bill * (1 + tip / 100)
per_person = total_with_tip / people

print(f"Each person should pay: ${round(per_person, 2)}")
