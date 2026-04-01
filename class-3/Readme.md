
#  Operators in Programming

An operator is a symbol that tells the computer what action to perform.

Example:
`+` tells the computer to add
`>` tells the computer to compare

---

## 1. Arithmetic Operators

-> Used to do math calculations

| Operator | Name           | Example | Meaning            |
| -------- | -------------- | ------- | ------------------ |
| `+`      | Addition       | `5 + 3` | Adds numbers       |
| `-`      | Subtraction    | `5 - 3` | Subtracts numbers  |
| `*`      | Multiplication | `5 * 3` | Multiplies numbers |
| `/`      | Division       | `6 / 3` | Divides numbers    |
| `%`      | Modulus        | `5 % 2` | Gives remainder    |

### Example:

```js
let a = 10;
let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.33
console.log(a % b); // 1
```

-> Used in DSA for: calculations, loops, indexes.

---

## 2 Relational Operators

-> Used to compare two values
-> Result is true or false

| Operator | Meaning          | Example  |
| -------- | ---------------- | -------- |
| `>`      | Greater than     | `5 > 3`  |
| `<`      | Less than        | `3 < 5`  |
| `>=`     | Greater or equal | `5 >= 5` |
| `<=`     | Less or equal    | `3 <= 5` |
| `==`     | Equal to         | `5 == 5` |
| `!=`     | Not equal        | `5 != 3` |

### Example:

```js
let x = 10;
let y = 20;

console.log(x > y);  // false
console.log(x < y);  // true
console.log(x == y); // false
```

-> Used in DSA for: conditions, searching, sorting.

---

## 3 Logical Operators

-> Used to combine conditions

| Operator | Name | Meaning                      |                              
| -------- | ---- | ---------------------------- | 
| `&&`     | AND  | Both conditions must be true |                              
| `//`     |  OR  | At least one condition true  |             
| `!`      | NOT  | Reverses the result          |                              

### Example:

```js
let age = 20;

console.log(age > 18 && age < 30); // true
console.log(age < 18 || age > 60); // false
console.log(!(age > 18));          // false
```

-> Used in DSA for: decision making, complex conditions.

---

## 4 Unary Operators

Sure! Let’s break down **Unary Operators** clearly with a table for easy understanding.

---

### **Unary Operators in JavaScript**

A **unary operator** is an operator that **works with only one operand** (single value). It performs operations like increment, decrement, negation, or type conversion.



| Operator       | Description                                  | Example           | Result / Explanation                                 |
| -------------- | -------------------------------------------- | ----------------- | ---------------------------------------------------- |
| `+`            | Unary plus – converts operand to a number    | `+ "5"`           | `5` (string `"5"` converted to number)               |
| `-`            | Unary minus – negates the value              | `- 10`            | `-10`                                                |
| `++` (prefix)  | Increment by 1 **before** using the value    | `let a = 5; ++a;` | `6` (`a` becomes 6 immediately)                      |
| `++` (postfix) | Increment by 1 **after** using the value     | `let a = 5; a++;` | `5` (expression evaluates to 5, `a` becomes 6 after) |
| `--` (prefix)  | Decrement by 1 **before** using the value    | `let a = 5; --a;` | `4` (`a` becomes 4 immediately)                      |
| `--` (postfix) | Decrement by 1 **after** using the value     | `let a = 5; a--;` | `5` (expression evaluates to 5, `a` becomes 4 after) |
| `!`            | Logical NOT – inverts boolean value          | `!true`           | `false`                                              |
| `typeof`       | Returns the type of operand                  | `typeof 5`        | `"number"`                                           |
| `void`         | Evaluates expression and returns `undefined` | `void(0)`         | `undefined`                                          |
| `~`            | Bitwise NOT – inverts bits                   | `~5`              | `-6` (binary inversion)                              |

---

#### **Examples in Code:**

```javascript
let a = 5;
console.log(+a);   // 5
console.log(-a);   // -5
console.log(++a);  // 6 (prefix)
console.log(a++);  // 6 (a becomes 7 after this line)
console.log(!true);// false
console.log(typeof a); // "number"
console.log(~5);   // -6
```

