---
chapter: 7
pageNumber: 50
description: A for loop is a powerful control structure used to execute a block of code multiple times, either for a specific number of iterations or over a defined range. It is highly versatile and commonly used for iterating through arrays, strings, and other iterable objects
---

## For

The easiest form of a loop is the for statement. This one has a syntax that is similar to an if statement, but with more options:

### Syntax

The syntax of `for` loop in javascript is given below

```javascript
for (initialization; end condition; change) {
    // do it, do it now
}
```

### Explanation:

- In the `initialization` part, executed before the first iteration, initialize your loop variable
- In the `end codition` part, put a condition that may be checked before each iteration. The moment the condition becomes `false`, the loop ends.
- In the `change` part, tell the program how to update the loop variable.
  Let's see how to execute the same code ten-times using a `for` loop:

```javascript
for (let i = 0; i < 10; i = i + 1) {
  // do this code ten-times
}
```

> _**Note**_: `i = i + 1` can be written `i++`.

## ```for...in``` loop

To loop through the enumerable properties of an object `for in` loop can be used. For each distinct property, JavaScript executes the specified statements.

### Syntax

```javascript
for (variable in object) {
  // iterate each property in the object
}
```

### Example

Let use suppose we have following object:

```javascript
const person = {
  fname: "John",
  lname: "Doe",
  age: 25,
};
```

Then, with the help of `for in` loop we can iterate over the `person` object to access it property like `fname`, `lname` and `age` as shown below.

```javascript
let info = "";
for (let x in person) {
  console.log(person[x]);
}
```

The output of above code snippet will be:

```pseudo
John
Doe
25
```

> **Note: The iterable objects such as `Arrays`, `Strings`, `Maps`, `NodeLists` can be looped using `for in` statement.&#x20;**

```javascript
// Example with Arrays
const myArray = [1, 2, 3, 4, 5];
for (const item of myArray) {
  console.log(item);
}

// Example with Strings
const myString = "Hello, World!";
for (const char of myString) {
  console.log(char);
}

// Example with Maps
const myMap = new Map();
myMap.set("name", "John");
myMap.set("age", 30);

for (const [key, value] of myMap) {
  console.log(key, value);
}

// Example with NodeLists (HTML elements)
const paragraphs = document.querySelectorAll("p");
for (const paragraph of paragraphs) {
  console.log(paragraph.textContent);
}
```
