# Javascript Training

## Walkthrough

```javascript
function add(a, b) {
  return a + b;
}
console.log(add(5, -12));

var clickMe = document.getElementById("clickMe");

clickMe.addEventListener("click", (event) => {
  alert("You clicked me");
});
clickMe.addEventListener("click", function (event) {
  fetch("https://jsonplaceholder.typicode.com/todos")
    .then((response) => response.json())
    .then((todos) => {
      todos.forEach((todo) => {
        var todoElement = `<p>${todo.title}</p>`;
        console.log(todoElement);
      });
    });
});
```

## Variables

```javascript
let result = 20; // var
function sum(a, b) {
  result = a + b;
  return result;
}
console.log(result);
console.log(sum(15, 12));
console.log(result);

let message = "Hello World";
console.log(message);
message = "Test";
console.log(message);

// variable which don't change
const PI = 3.142;

function area(radius) {
  return PI * radius * radius;
}
console.log(area(5));

console.log(PI);

const add = (a, b) => a + b;

console.log(add(5, 18));

let age = 20;

console.log("My Age is " + age);

let studentName = "Mackrine";

console.dir(studentName);
console.dir(studentName.split(""));
console.dir(studentName.toUpperCase(""));
console.dir(studentName.toLowerCase(""));
console.dir(studentName.includes("ack"));
```

## Data types

```javascript
let stringVariable = "hello";
console.log(typeof stringVariable);

let age = 20.25;
console.log(typeof age);

var testUndefined;
console.log(typeof testUndefined);

var testNull = null;
console.log(typeof testNull);

var test = false;
console.log(typeof test);

let fruits = ["Orange", "Banana", "Mango", "Madafu"];

var array = new Array(fruits);

console.log(typeof fruits);
console.log(typeof array);
console.log(typeof 10n);

var student = {};
console.log(typeof student);
```

## Interaction with alert, confirm, prompt

```javascript
// interaction with alert, confirm, prompt

// alert("Hello, your door bell is not working")
/* let isBoss = confirm("Is Musili in class?")
console.log(isBoss); */

let ageString = prompt("What is your age?");
console.log(typeof ageString);
console.log(ageString);
```

## Data Conversions

```javascript
let ageString = prompt("What is your age?");
console.log(typeof ageString);
//number
let age = Number(ageString);
console.log(typeof age);
console.log(age);

// let isBoss = confirm("Is your boss?");
// console.log(typeof isBoss);

let myAgeIs = `My Age is ${age}`;

let isAgeSet = Boolean(myAgeIs);
console.log(myAgeIs);

console.log(typeof isAgeSet); // number
console.log(isAgeSet);

let myAgeIs2 = "";
console.log(myAgeIs2);
let isAgeSet2 = Boolean(myAgeIs2);
console.log(typeof isAgeSet2);
console.log(isAgeSet2); // false

alert("6" / "2"); // 3

let ageTwoSTring = String(age);
console.log(typeof ageTwoSTring); //string
console.log(ageTwoSTring);

let test = null;
let test2 = undefined;

let numberOne = Number(test); // 0
console.log(typeof numberOne);
console.log(numberOne);

let numberTwo = Number(test2); //undefined
console.log(typeof numberTwo);
console.log(numberTwo); //NaN
```

## Operators and Math

```javascript
function sum(a, b) {
  console.log(a);
  console.log(b);
  return a + b;
}

let a = 10;
// a = -a // unary negation operator

let b = 25;
let result = a - b; // binary (minus) operator
console.log(result);
```

## math Operators

```javascript
// Addition Operator
let a = 10;
let b = 15;

let result = a + b; //binary plus

console.log(result); //25

let c = -10;

console.log(-c); // 10

// - * - = +
// + * + = +
// + * - = -

// Subtraction
let result2 = b - c; // 15 -- 10
console.log(result2); // 25

// Multiplication

let result3 = b * a;

console.log(result3); // 150

let result4 = a * "3";

console.log(typeof result4);

console.log(result4); // 30

let result5 = "3" * a;
console.log(typeof result5);
console.log(result5); // 30

// Division

let months = 99;
let interval = 12;

let noOfYears = months / interval;
console.log(parseFloat(interval)); //12

console.log(typeof noOfYears);
console.log(noOfYears); // 8.25
console.log(parseInt(noOfYears)); // 8
console.log(parseFloat("85.63")); // 85.63

// Remainder operator

let ageRemainder = months % interval;
console.log(ageRemainder); // 3

// Exponential operator
let radius = 5;

console.log(Math.PI);
let area = Math.PI * radius ** 2; // PIr2 === PI*r*r

console.log(area);
```

## Comparisons

### Greater than Sign `>`

```javascript
let a = 10;
let b = 20;

let result = a > b;

console.log(result); //false

let c = 50;
let result2 = c > b;
console.log(result2); // true
```

### less than Sign `< `

```javascript
let a = 10;
let b = 20;

let result = a < b;

console.log(result); //true

let c = 50;
let result2 = c < b;
console.log(result2); //false
```

### less than or equal to Sign `<=`

```javascript
let a = 10;
let b = 10;

let result = a <= b;

console.log(result); //true

let c = 50;
let result2 = c <= b;
console.log(result2); //false
```

### greater than or equal to Sign `>=`

```javascript
let a = 10;
let b = 10;

let result = a >= b;

console.log(result); //true

let c = 50;
let result2 = c >= b;
console.log(result2); //true
```

### Equals and Equality Sign `==` vs `===`

```javascript
let a = 10;
let b = "10";

let result = a == b; //equals  checks on the content

console.log(typeof a);
console.log(typeof b);
console.log(typeof result);
console.log(result); //true;

let result2 = a === b; //equality => checks the type of variable and content

console.log(typeof result2);
console.log(result2); //false;
```

### Equals and Equality Sign `!=` vs `!==`

```javascript
let a = 10;
let b = "10";

let result = a != b; //equals

console.log(typeof a);
console.log(typeof b);
console.log(typeof result);
console.log(result); //false

let result2 = a !== b; //equality => checks the type of variable and value

console.log(typeof result2);
console.log(result2); //true
```

### Bonus

```javascript
let a = "Z"; // 90
let b = "A"; //65

let result = a > b;
console.log(typeof a);

console.log(result); //true

let str1 = "Glow";
let str2 = "Glee";
console.log(str1 > str2); //true
```

## Conditions

## logical Operators

## Loops

## Switch statement

## Functions

```javascript
//function declaration and implementation
function sayHello() {
  console.log("just greetings");
}

function sayHelloWithMessage(message = "just greetings 2") {
  console.log(message);
}

sayHello();
sayHelloWithMessage(undefined);
sayHelloWithMessage(null);
sayHelloWithMessage("test");
let username = "John"; //global variable
function showMessage() {
  // local variable
  let message = "Hello, " + username;
  username = "Bob";
  console.log(message);
}
showMessage();
console.log(username);
```

### Variable scopes

```javascript
let username = "John"; //global variable
function showMessage() {
  // local variable
  let username = "Jane";
  let message = "Hello, " + username;
  username = "Bob";
  console.log(message);
}
showMessage();
console.log(username); // John
```

### functions that return

```javascript
function add(a, b) {
  return a + b;
}

let result = add(45, 78);

console.log(result);
console.log(add(45, 120));

function doesContain(text, key) {
  let data = String(text);
  return data.includes(key);
}
console.dir(doesContain);
console.log(doesContain("It is a new day, let's learn javascript", "lets"));

function messageWithDefaultParameter(text = "dred") {
  if (text === undefined) {
    text = "default Value";
  }
  console.log("Hello, " + text);
}
messageWithDefaultParameter();
messageWithDefaultParameter("My new message");

function doQualifyForId(age) {
  console.log(typeof age);
  age = Number(age);
  console.log(typeof age);
  console.log(age);
  if (age < 18) {
    return false;
  }
  return true;
}

console.log(doQualifyForId("45t")); // 45 true
```

## Arrow functions

### Functions that don't return values

```javascript
// Arrow functions
let username = "John"; //global variable
let showMessage = () => {
  // local variable
  let message = "Hello, " + username;
  username = "Bob";
  console.log(message);
};

showMessage();
console.log(username);
```

### Functions with defaulted value parameters

```javascript
let sayHelloWithMessage = (message = "just greetings 2") =>
  console.log(message);

sayHelloWithMessage(undefined);
sayHelloWithMessage(null);
sayHelloWithMessage("test");
```

### Functions with defaulted value parameters

```javascript
let add = (a, b) => a + b;
let subtract = (a, b) => a - b;
console.log(add(45, 89));
```

### Functions that return other functions as values

```javascript
let age = prompt("What is your age?");

// let welcome = age < 18 ? () => alert("Hello") : () => alert("Greetings!");

function welcome2() {
  if (age < 18) {
    return function () {
      return alert("Hello");
    };
  }
  return function () {
    return alert("Greetings!");
  };
}

welcome2()();
```

## Objects

```javascript
// Objects
// defining an object
let student = new Object();
let studentTwo = {};

student.name = "Teresa";
console.log(student.name);

let studentThree = {
  name: "John",
  age: 24,
  "student no": 1,
  print: function () {
    console.log("Hello, " + this.name);
  },
  address: {
    lat: -10.2569854556,
    lng: 4.589632445,
  },
};

// set values by key
studentThree["student no"] = 89;

console.log(studentThree);

//get values by key
console.log(studentThree.name);
console.log(studentThree.age);
console.log(studentThree["student no"]);
studentThree.print();
console.log(studentThree.address.lat);
console.log(studentThree.address.lng);

//removing properties
delete studentThree.age;

console.log(studentThree);

let studentFour = {
  name: "Paul",
  age: 20,
  "student no": 3,
  print: function () {
    console.log("Hello, " + this.name);
  },
};
let studentFive = null;

// null coalescing -> error silencing operator
console.log(studentFour.address?.lat);
console.log(studentThree.address?.lat);
// console.log(studentFive.address?.lat); // is not ideal on the first object

// Check if property exists in an object
console.log("address" in studentFour); // false
console.log("address" in studentThree); // true
console.dir(studentThree);
console.log(Object.hasOwnProperty.call(studentThree, "age")); // false
console.log("-------------------");
// extract all keys
for (const key in studentThree) {
  console.log(key);
  console.log(studentThree[key]);
}
```

## Object References and clone

```javascript
let student = {
  name: "Martin",
  age: 45,
  address: {
    lat: -45,
    lat: 50,
  },
};

let studentTwo = student;

console.log(student.name);
console.log(studentTwo.name);

studentTwo.name = "John 5";

console.log(student.name);
console.log(studentTwo.name);

let studentThree = {
  city: "Nairobi",
};

console.log(student == studentTwo);
console.log(student === studentTwo);
console.log(student == studentThree);
console.log(student === studentThree);

// cloning

let studentFour = {};

for (const key in student) {
  studentFour[key] = student[key];
}
console.log(studentFour);

let studentFive = {};

Object.assign(studentFive, student, studentThree);
console.log(studentFive);
```

## use of `this` keyword

```javascript
// Use of `this` keyword
let name = "Test";
let student = {
  name: "John",
  age: 45,
  greet() {
    console.log(this);
    console.log(`Hello ${this.name}`);
  },
  sayHi() {
    console.log(student.name);
  },
};

student.greet();
student.sayHi();
```
## Classes
```javascript

// Classes

class Student{

    constructor(name){
        this.name = name
    }

    sayHello(){
        console.log(this.name);
    }

}

let studentOne = new Student("John");
console.log(typeof Student); // function
console.log(typeof studentOne);// object
console.log(studentOne);
```
