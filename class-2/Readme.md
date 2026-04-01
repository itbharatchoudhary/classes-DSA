 
# JavaScript Essentials

## 1. Difference between `var`, `let`, and `const

### `var`

* `var` is a function-scoped variable.
* It can be re-declared and reassigned.
* It is hoisted to the top of its scope and initialized with `undefined`.
* It may cause unexpected behavior, so it is not recommended in modern JavaScript.

Example:

```js
var x = 10;
var x = 20; // allowed
x = 30;     // allowed
```

---

### `let`

* `let` is block-scoped (limited to `{ }`).
* It cannot be re-declared, but it can be reassigned.
* It is hoisted but not initialized.

Example:

```js
let y = 10;
// let y = 20;  not allowed
y = 20;     // allowed
```

---

### `const`

* `const` is also block-scoped.
* It cannot be re-declared or reassigned.
* The value must be assigned at the time of declaration.
* Used for constant values.

Example:

```js
const z = 10;
// z = 20;  not allowed
```

---

### Comparison Table

| Feature    | var             | let       | const     |
| ---------- | --------------- | --------- | --------- |
| Scope      | Function        | Block     | Block     |
| Re-declare | Yes             | No        | No        |
| Reassign   | Yes             | Yes       | No        |
| Hoisting   | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |

---

## 2. Sum of Two Values

### String + String = string 

* When two strings are added. 
* string concatenation occurs.

```js
"Hello" + "World"  // "HelloWorld"
```

---

### String + Integer = string

* The integer is converted into a string.
* Result is string concatenation.

```js
"Age: " + 21   // "Age: 21"
```

---

### Integer + Integer = Integer

* Arithmetic addition takes place.
* Result is an integer.

```js
10 + 20   // 30
```

---

## 3. Relation between Integer and String

* JavaScript is a dynamically typed language.
* It automatically converts data types when required.
* This behavior is called Type Coercion.

Example:

```js
"5" + 5   // "55" (string)
"5" - 2   // 3 (number)
```

---

## 4. Sum and Message (Type Coercion)

### 1. **problem**

```javascript
let a = 5;
let b = 10;
console.log("the sum of " + a + " and " + b + " is " + a + b);
```

**Output:**

```
the sum of 5 and 10 is 510
```

Wait… you expected `15`, right? That’s because **JavaScript evaluates `+` differently depending on types**.

---

### 2. **Concept: + is Overloaded**

In JavaScript:

* `+` **adds numbers** if both operands are numbers.
* `+` **concatenates strings** if **any operand is a string**.

JavaScript evaluates **left-to-right** here:

```javascript
"the sum of " + a      // "the sum of 5"  (string)
"the sum of 5" + " and " // "the sum of 5 and"
"the sum of 5 and" + b   // "the sum of 5 and 10"
"the sum of 5 and 10" + a // "the sum of 5 and 105"
```

So finally:

```
"the sum of 5 and 10" + 5 → "the sum of 5 and 105"
```

If your original code had `+ a + b` at the end, JavaScript concatenates both as **strings**, producing `510` instead of adding them.


---

### 3. **Key Concepts Behind This Problem**

1. **Operator Overloading**: `+` works for **numbers (addition)** and **strings (concatenation)**.
2. **Type Coercion**: JS automatically converts numbers to strings if a string is present in `+`.
3. **Evaluation Order**: JS evaluates left-to-right in expressions.
4. **Parentheses Control Precedence**: `(a + b)` ensures addition happens before concatenation.
5. **Template Literals**: Modern way to embed expressions without worrying about type coercion.

### Type Coercion

* Automatic conversion of one data type into another.
* Occurs during operations involving different data types.

Example:

```js
let a = 10;
let b = "5";

let result = a + b;
console.log(result); // "105"
```

---

### Greet the User

```js
let name = "Bharat";
console.log("Hello " + name + ", welcome to JavaScript!");
```

---

## 5. Accept and Print the Answer

### Using `prompt()`

```js
let answer = prompt("Enter your answer:");
console.log("Your answer is: " + answer);
```

* `prompt()` accepts input from the user.
* Input is always received as a string.

---

## 6. Swap Two Variables (Three Methods)

### Method 1: Using a Third Variable

```js
let a = 10;
let b = 20;

let temp = a;
a = b;
b = temp;
```

✔ Most common and easiest method.

---

### Method 2: Using Arithmetic Operators

```js
let a = 10;
let b = 20;

a = a + b;
b = a - b;
a = a - b;
```

 Does not require extra variable
 Not suitable for very large numbers

---

### Method 3: Using Destructuring Assignment (ES6)

```js
let a = 10;
let b = 20;

[a, b] = [b, a];
```

✔ Modern and clean approach
✔ Most recommended in JavaScript




