## Comment Your JavaScript Code

Comments are lines of code that JavaScript will intentionally ignore. Comments are a great way to leave notes to yourself and to other people who will later need to figure out what that code does.

There are two ways to write comments in JavaScript:

Using // will tell JavaScript to ignore the remainder of the text on the current line. This is an in-line comment:

// This is an in-line comment.
You can make a multi-line comment beginning with /* and ending with */. This is a multi-line comment:

/* This is a
multi-line comment */
NOTE: As you write code, you should regularly add comments to clarify the function of parts of your code. Good commenting can help communicate the intent of your code—both for others and for your future self.

### Tests
1. You should create a // style comment that contains at least five letters.
2. You should create a /* */ style comment that contains at least five letters.

### Answers

```javascript

// Hello World

/* Hi Welcome to world of Web Development */

```

## Declare JavaScript Variables

In computer science, data is anything that is meaningful to the computer. JavaScript provides eight different data types which are undefined, null, boolean, string, symbol, bigint, number, and object.

For example, computers distinguish between numbers, such as the number 12, and strings, such as "12", "dog", or "123 cats", which are collections of characters. Computers can perform mathematical operations on a number, but not on a string.

Variables allow computers to store and manipulate data in a dynamic fashion. They do this by using a "label" to point to the data rather than using the data itself. Any of the eight data types may be stored in a variable.

Variables are similar to the x and y variables you use in mathematics, which means they're a simple name to represent the data we want to refer to. Computer variables differ from mathematical variables in that they can store different values at different times.

We tell JavaScript to create or declare a variable by putting the keyword var in front of it, like so:

var ourName;
creates a variable called ourName. In JavaScript we end statements with semicolons. Variable names can be made up of numbers, letters, and $ or _, but may not contain spaces or start with a number.


### Test

1. declare myName with the var keyword, ending with a semicolon

### Answer

```javascript
var myName;
```

## Storing Values with the Assignment Operator

In JavaScript, you can store a value in a variable with the assignment operator (=).

myVariable = 5;
This assigns the Number value 5 to myVariable.

If there are any calculations to the right of the = operator, those are performed before the value is assigned to the variable on the left of the operator.

var myVar;
myVar = 5;
First, this code creates a variable named myVar. Then, the code assigns 5 to myVar. Now, if myVar appears again in the code, the program will treat it as if it is 5.

### Test
1. Assign the value 7 to variable a.

### Given Code

```javascript
// Setup
var a;

// Only change code below this line
```

### Answer
```javascript
// Setup
var a;

// Only change code below this line

a = 7;
```

## Assigning the Value of One Variable to Another

After a value is assigned to a variable using the assignment operator, you can assign the value of that variable to another variable using the assignment operator.

```var myVar; 
myVar = 5; 
var myNum; 
myNum = myVar;
```

The above declares a myVar variable with no value, then assigns it the value 5. Next, a variable named myNum is declared with no value. Then, the contents of myVar (which is 5) is assigned to the variable myNum. Now, myNum also has the value of 5.

### Test
1. Assign the contents of a to variable b.

### Given Code
```javascript
// Setup
var a;
a = 7;
var b;

// Only change code below this line
```

### Answer
```javascript
// Setup
var a;
a = 7;
var b;

// Only change code below this line
b = a;
```

## Initializing Variables with the Assignment Operator

It is common to initialize a variable to an initial value in the same line as it is declared.

```javasccript
var myVar = 0;
```
Creates a new variable called myVar and assigns it an initial value of 0.

### Test
1. Define a variable a with var and initialize it to a value of 9.


### Answer
```javascript
var a = 9;
```


## Declare String Variables

Previously you used the following code to declare a variable:

```javascript
var myName;
```
But you can also declare a string variable like this:

```javascript
var myName = "your name";
```
"your name" is called a string literal. A string literal, or string, is a series of zero or more characters enclosed in single or double quotes.

### Test
1. Create two new string variables: myFirstName and myLastName and assign them the values of your first and last name, respectively.

### Answer

```javascript
var myFirstName = "Vidya";
var myLastName = "Sagar";
```

## Understanding Uninitialized Variables

When JavaScript variables are declared, they have an initial value of undefined. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a string of undefined.


### Test
1. Initialize the three variables a, b, and c with 5, 10, and "I am a" respectively so that they will not be undefined.

### Given Code

```javascript
// Only change code below this line
var a;
var b;
var c;
// Only change code above this line

a = a + 1;
b = b + 5;
c = c + " String!";
```

### Answer

```javascript
// Only change code below this line
var a = 5;
var b = 10;
var c = "I am a";
// Only change code above this line

a = a + 1;
b = b + 5;
c = c + " String!";
```

## Understanding Case Sensitivity in Variables

In JavaScript all variables and function names are case sensitive. This means that capitalization matters.

MYVAR is not the same as MyVar nor myvar. It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.

Best Practice

Write variable names in JavaScript in camelCase. In camelCase, multi-word variable names have the first word in lowercase and the first letter of each subsequent word is capitalized.

Examples:

```javascript
var someVariable;
var anotherVariableName;
var thisVariableNameIsSoLong;
```

### Test
1. Modify the existing declarations and assignments so their names use camelCase.

### Given Code

```javascript
// Variable declarations
var StUdLyCapVaR;
var properCamelCase;
var TitleCaseOver;

// Variable assignments
STUDLYCAPVAR = 10;
PRoperCAmelCAse = "A String";
tITLEcASEoVER = 9000;
```

### Answer

```javascript
// Variable declarations
var studlyCapVar;
var properCamelCase;
var titleCaseOver;

// Variable assignments
studlyCapVar = 10;
properCamelCase = "A String";
titleCaseOver = 9000;
```

## Explore Differences Between the var and let Keywords

One of the biggest problems with declaring variables with the var keyword is that you can easily overwrite variable declarations:

var camper = "James";
var camper = "David";
console.log(camper);
In the code above, the camper variable is originally declared as James, and is then overridden to be David. The console then displays the string David.

In a small application, you might not run into this type of problem. But as your codebase becomes larger, you might accidentally overwrite a variable that you did not intend to. Because this behavior does not throw an error, searching for and fixing bugs becomes more difficult.

A keyword called let was introduced in ES6, a major update to JavaScript, to solve this potential issue with the var keyword. You'll learn about other ES6 features in later challenges.

If you replace var with let in the code above, it results in an error:

let camper = "James";
let camper = "David";
The error can be seen in your browser console.

So unlike var, when you use let, a variable with the same name can only be declared once.

### Test

1. Update the code so it only uses the let keyword.

### Code Given
```javascript
var catName = "Oliver";
var catSound = "Meow!";
```

### Answer
```javascript
let catName = "Oliver";
let catSound = "Meow!";
```

## Declare a Read-Only Variable with the const Keyword

The keyword let is not the only new way to declare variables. In ES6, you can also declare variables using the const keyword.

const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned:

```javascript
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```
The console will display an error due to reassigning the value of FAV_PET.

You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.

***Note:*** It is common for developers to use uppercase variable identifiers for immutable values and lowercase or camelCase for mutable values (objects and arrays). You will learn more about objects, arrays, and immutable and mutable values in later challenges. Also in later challenges, you will see examples of uppercase, lowercase, or camelCase variable identifiers.

### Test
1. Change the code so that all variables are declared using let or const. Use let when you want the variable to change, and const when you want the variable to remain constant. Also, rename variables declared with const to conform to common practices. Do not change the strings assigned to the variables.

***Suggestion:*** 
- var should not exist in your code.
- You should change fCC to all uppercase.
- FCC should be a constant variable declared with const.
- The string assigned to FCC should not be changed.
- fact should be declared with let.
- console.log should be changed to print the FCC and fact variables.

### Code Given

```javascript
var fCC = "freeCodeCamp"; // Change this line
var fact = "is cool!"; // Change this line
fact = "is awesome!";
console.log(fCC, fact); // Change this line
```

### Answer

```javascript
const FCC = "freeCodeCamp"; // Change this line
let fact = "is cool!"; // Change this line
fact = "is awesome!";
console.log(FCC, fact); // Change this line
```


## Add Two Numbers with JavaScript

Number is a data type in JavaScript which represents numeric data.

Now let's try to add two numbers using JavaScript.

JavaScript uses the + symbol as an addition operator when placed between two numbers.

Example:

```javascript
const myVar = 5 + 10;
```
myVar now has the value 15.

### Test
1. Change the 0 so that sum will equal 20.

### Code Given

```javascript
const sum = 10 + 0;
```

### Answer
```javascript
const sum = 10 + 10;
```

## Subtract One Number from Another with JavaScript

We can also subtract one number from another.

JavaScript uses the - symbol for subtraction.

Example

const myVar = 12 - 6;
myVar would have the value 6.

### Test

1. Change the 0 so the difference is 12.

### Code Given
```javascript
const difference = 45 - 0;
```

### Answer
```javascript
const difference = 45 - 33;
```

## Multiply Two Numbers with JavaScript

We can also multiply one number by another.

JavaScript uses the * symbol for multiplication of two numbers.

Example

```javascript
const myVar = 13 * 13;
```
myVar would have the value 169.

### Test
Change the 0 so that product will equal 80.

### Code Gievn
```javascript
const product = 8 * 0;
```

### Answer
```javascript
const product = 8 * 10;
```

## Divide One Number by Another with JavaScript

We can also divide one number by another.

JavaScript uses the / symbol for division.

Example

```javascript
const myVar = 16 / 2;
```
myVar now has the value 8.

### Test

1. Change the 0 so that the quotient is equal to 2.

### Given Code
```javascript
const quotient = 66 / 0;
```

### Answer
```javascript
const quotient = 66 / 33;
```

## Increment a Number with JavaScript

You can easily increment or add one to a variable with the ++ operator.

i++;
is the equivalent of

i = i + 1; <br>
***Note:*** The entire line becomes i++;, eliminating the need for the equal sign.

### Test
1. Change the code to use the ++ operator on myVar.

### Code Given
```javascript
let myVar = 87;

// Only change code below this line
myVar = myVar + 1;
```

### Answer
```javascript
let myVar = 87;

// Only change code below this line
myVar++;
```

## Decrement a Number with JavaScript

You can easily decrement or decrease a variable by one with the -- operator.

i--;
is the equivalent of

i = i - 1;
***Note:*** The entire line becomes i--;, eliminating the need for the equal sign.

### Test
1. Change the code to use the -- operator on myVar.

### Given Code

```javascript
let myVar = 11;

// Only change code below this line
myVar = myVar - 1;
```

### Answer

```javascript
let myVar = 11;

// Only change code below this line
myVar--;
```