---
layout: cover
title: Class Summary
class: center middle
background: https://images.unsplash.com/photo-1581090700227-1e8e8d5d4f5d?auto=format&fit=crop&w=1950&q=80
---

# **JavaScript Class Summary**

### Highlights from second semester classes so far 

Presented by **[CIRCLE 14]**  
TINYUKA —2025

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!-- Next page -->

---
transition: fade-out
---

# Table of Contents

1. [Introduction to JavaScript](#/intro)
2. [Data Types](#/data-types)
   - [Number](#/number)
   - [String](#/string)
   - [Object](#/object)
3. [Function](#/function)
4. [Array](#/array)
5. [DOM & Event Handling](#/dom-event)
6. [Modules](#/modules)

---
## id: intro
---
## Introduction to JavaScript

- JavaScript is a versatile programming language for web development.
- It runs in the browser and enables interactive features.
- Created by Brendan Eich in 1995.
- Evolved into modern frameworks like React, Vue, and Angular.

---
## id: data-types
---
## Data Types

JavaScript has several core data types, including:

- **Primitive Types**: Number, String, Boolean, Null, Undefined, Symbol
- **Reference Types**: Objects, Arrays, Functions

---
## id: number
---
# Number

They can be used in calculations and can include both integers (whole numbers) and floating-point numbers (decimals).

**Number Types**

- **Integers**: Whole numbers without decimals
- **Floating-point numbers**: Numbers with decimals

```js
let integer = 35;
let float = 4.57;
```

**Special numeric values:** e.g. NaN and Infinity

- NaN (Not a number): Represents an invalid or unreliable numeric result.

```js
let result = "hello" * 2;
console.log(result); // NaN
```

---

- Infinity: we have the positive infinity that represents a value that is greater than any other number and negative infinity that represents a value that is less than any other number.

```js
let a = 1
let b = 0
console.log (a/b); // Infinity

let a = -1
let b = 0
console.log (a/b); // -Infinity
```

---

# Number operations

Refers to ways you can manipulate and work with numbers. Below are the most common number operations in JavaScript using arithmetic operators like +, -, \*, /, %

Note an **operator** is a received syntax consisting of punctuation or alphanumeric characters that carries out built in functionalities while **operands** are the values the operator works on

       operator
           |
       20  +  7
       |      |
       operands

```js
let a = 20;
let b = 7;

console.log(a + b); // 27
console.log(a - b); // 13
console.log(a * b); // 140
console.log(a / b); // 2.857142857142857
console.log(a % b); // 6
```

---

- Numeric separator (\_) : They are used to improve readability of large numbers in JavaScript.

```js
let largeNumber = 1_000_000_000; // equivalent to 1000000000
console.log (largeNumber); // Output: 1000000000
```

They don't affect the value of the number but are just there to make the number easier to read.

```js
let float = 3.141_59; // No impact on the value
console.log(float); // 3.14159
```

- Number.parseInt(): Converts a string into an integer by removing any decimal point. It reads from left to right until it hits something that isn’t a number and then stops.

```js
let x = Number.parseInt("100px"); // 100
let y = Number.parseInt("3.14"); // 3
let z = Number.parseInt("Hello 12"); // NaN (can't convert text/can’t read if it starts with text)
```

- Number.parseFloat (): reads the string and keeps the decimal part if it exists.

```js
let x = Number.parseFloat("100.50px"); // 100.5 (reads until it sees non-numeric)
let y = Number.parseFloat("3.14"); // 3.14
let z = Number.parseFloat("Hello 12"); // NaN (no valid number to start with)
```

---

- .toString(): This is a method you can use to turn a number into text (a string).

```js

let age = 25;
let ageText = age.toString();
console.log(ageText); // "25"
console.log(typeof ageText); // string
```
You use .toString() when you need to:

- Display numbers as text (like in a sentence or on a webpage).
- Format output, like showing "You have 5 new messages"
