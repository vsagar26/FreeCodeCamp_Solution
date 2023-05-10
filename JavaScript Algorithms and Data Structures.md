# [freeCodeCamp](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/)


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

## Create Decimal Numbers with JavaScript

We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.

### Test
1. Create a variable myDecimal and give it a decimal value with a fractional part (e.g. 5.7).

### Given Code

```javascript
const ourDecimal = 5.7;

// Only change code below this line
```
### Answer
```javascript
const ourDecimal = 5.7;

// Only change code below this line

const myDecimal = 5.7
```

## Multiply Two Decimals with JavaScript

In JavaScript, we can also perform calculations with decimal numbers, just like whole numbers.

### Test
1. Change the 0.0 so that product will equal 5.0.

### Given Code
```javascript
const product = 2.0 * 0.0;
```

### Answer
```javascript
const product = 2.0 * 2.5;
```

## Divide One Decimal by Another with JavaScript

Now let's divide one decimal by another.

### Test
1. Change the 0.0 so that quotient will equal to 2.2

### Code Given
```javascript
const quotient = 0.0 / 2.0; // Change this line
```

### Answer
```javascript
const quotient = 4.4 / 2.0
```

## Finding a Remainder in JavaScript

The remainder operator % gives the remainder of the division of two numbers.

**Example**

5 % 2 = 1
5 / 2 = 2 remainder 1
2 * 2 = 4
5 - 4 = 1
Usage
In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2. Even numbers have a remainder of 0, while odd numbers a remainder of 1.

17 % 2 = 1
48 % 2 = 0 <br><br>
**Note:** The remainder operator is sometimes incorrectly referred to as the modulus operator. It is very similar to modulus, but does not work properly with negative numbers.

### Test
1. Set remainder equal to the remainder of 11 divided by 3 using the remainder (%) operator.

### Code Given
```javascript
const remainder = 0;
```

### Answer
```javascript
const remainder = 11%3;
console.log(remainder);
```

## Compound Assignment With Augmented Addition

In programming, it is common to use assignments to modify the contents of a variable. Remember that everything to the right of the equals sign is evaluated first, so we can say:

myVar = myVar + 5;
to add 5 to myVar. Since this is such a common pattern, there are operators which do both a mathematical operation and assignment in one step.

One such operator is the += operator.

let myVar = 1;
myVar += 5;
console.log(myVar);
6 would be displayed in the console.

### Test
1. Convert the assignments for a, b, and c to use the += operator.

### Code Given
```javascript
let a = 3;
let b = 17;
let c = 12;

// Only change code below this line
a = a + 12;
b = 9 + b;
c = c + 7;
```

### Answer
```javascript
let a = 3;
let b = 17;
let c = 12;

// Only change code below this line
a += 12;
b += 9;
c += 7;

console.log(a);
console.log(b);
console.log(c);
```
## Compound Assignment With Augmented Subtraction

Like the += operator, -= subtracts a number from a variable.

myVar = myVar - 5;
will subtract 5 from myVar. This can be rewritten as:

myVar -= 5;

### Test
1. Convert the assignments for a, b, and c to use the -= operator.

### Code Given
```javascript
let a = 11;
let b = 9;
let c = 3;

// Only change code below this line
a = a - 6;
b = b - 15;
c = c - 1;
```

### Answer
```javascript
let a = 11;
let b = 9;
let c = 3;

// Only change code below this line
a -= 6;
b -= 15;
c -= 1;

console.log(a);
console.log(b);
console.log(c);
```


## Compound Assignment With Augmented Multiplication

The *= operator multiplies a variable by a number.

myVar = myVar * 5;
will multiply myVar by 5. This can be rewritten as:

myVar *= 5;

### Test
1. Convert the assignments for a, b, and c to use the *= operator.

### Code Given
```javascript
let a = 5;
let b = 12;
let c = 4.6;

// Only change code below this line
a = a * 5;
b = 3 * b;
c = c * 10;
```

### Answer
```javascript
let a = 5;
let b = 12;
let c = 4.6;

// Only change code below this line
a *= 5;
b *= 3;
c *= 10;

console.log(a);
console.log(b);
console.log(c);
```

## Compound Assignment With Augmented Division

The /= operator divides a variable by another number.

myVar = myVar / 5;
Will divide myVar by 5. This can be rewritten as:

myVar /= 5;

### Test
1. Convert the assignments for a, b, and c to use the /= operator.

### Code Given 
```javascript
let a = 48;
let b = 108;
let c = 33;

// Only change code below this line
a = a / 12;
b = b / 4;
c = c / 11;
```

### Answer
```javascript
let a = 48;
let b = 108;
let c = 33;

// Only change code below this line
a /= 12;
b /= 4;
c /= 11;

console.log(a);
console.log(b);
console.log(c);
```

## Escaping Literal Quotes in Strings

When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: " or ' inside of your string?

In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash (\) in front of the quote.

```javascript
const sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```
This signals to JavaScript that the following quote is not the end of the string, but should instead appear inside the string. So if you were to print this to the console, you would get:

```javascript
Alan said, "Peter is learning JavaScript".
```

### Test
1. Use backslashes to assign a string to the myStr variable so that if you were to print it to the console, you would see:

```javascript
I am a "double quoted" string inside "double quotes".
```

### Code Given

```javascript
const myStr = ""; // Change this line
```

### Answer

```javascript
const myStr = "I am a \"double quoted\" string inside \"double quotes\".";
```


## Quoting Strings with Single Quotes

String values in JavaScript may be written with single or double quotes, as long as you start and end with the same type of quote. Unlike some other programming languages, single and double quotes work the same in JavaScript.

```javascript
const doubleQuoteStr = "This is a string"; 
const singleQuoteStr = 'This is also a string';
```
The reason why you might want to use one type of quote over the other is if you want to use both in a string. This might happen if you want to save a conversation in a string and have the conversation in quotes. Another use for it would be saving an `<a>` tag with various attributes in quotes, all within a string.

```javascript
const conversation = 'Finn exclaims to Jake, "Algebraic!"';
```
However, this becomes a problem if you need to use the outermost quotes within it. Remember, a string has the same kind of quote at the beginning and end. But if you have that same quote somewhere in the middle, the string will stop early and throw an error.

```javascript
const goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"'; 
const badStr = 'Finn responds, "Let's go!"';
```

Here badStr will throw an error.

In the goodStr above, you can use both quotes safely by using the backslash \ as an escape character.

**Note:** The backslash \ should not be confused with the forward slash /. They do not do the same thing.


### Test
1. Change the provided string to a string with single quotes at the beginning and end and no escape characters.

Right now, the `<a>` tag in the string uses double quotes everywhere. You will need to change the outer quotes to single quotes so you can remove the escape characters.

### Code Given
```javascript
const myStr = "<a href=\"http://www.example.com\" target=\"_blank">Link</a>";
```

### Answer
```javascript
const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```

## Escape Sequences in Strings

Quotes are not the only characters that can be escaped inside a string. Escape sequences allow you to use characters you may not otherwise be able to use in a string.

```javascript
Code	Output
\'	single quote 
\"	double quote
\\	backslash
\n	newline
\t	tab
\r	carriage return
\b	backspace
\f	form feed
```
Note that the backslash itself must be escaped in order to display as a backslash.

### Test
1. Assign the following three lines of text into the single variable myStr using escape sequences.

```javascript
FirstLine
    \SecondLine
ThirdLine
```

You will need to use escape sequences to insert special characters correctly. You will also need to follow the spacing as it looks above, with no spaces between escape sequences or words.

**Note:** The indentation for SecondLine is achieved with the tab escape character, not spaces.

### Code Given
```javascript
const myStr = ""; // Change this line
```

### Answer
```javascript
const myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
```

## Concatenating Strings with Plus Operator

In JavaScript, when the + operator is used with a String value, it is called the concatenation operator. You can build a new string out of other strings by concatenating them together.

Example

`'My name is Alan,' + ' I concatenate.'` <br>

**Note:** Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

`const ourStr = "I come first. " + "I come second.";`<br>

The string I come first. I come second. would be displayed in the console.

### Test
1. Build myStr from the strings `This is the start.` and `This is the end.` using the `+` operator. Be sure to include a space between the two strings.

### Code Given
```javascript
const myStr = ""// Change this line;
```

### Answer
```javascript
const myStr = "This is the start. " + "This is the end.";
```


## Concatenating Strings with the Plus Equals Operator
We can also use the `+=` operator to concatenate a string onto the end of an existing string variable. This can be very helpful to break a long string over several lines.

**Note:** Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

Example:

```javascript
let ourStr = "I come first. ";
ourStr += "I come second.";
```
`ourStr` now has a value of the string `I come first. I come second..`

### Test
1. Build myStr over several lines by concatenating these two strings: `This is the first sentence.` and `This is the second sentence.` using the `+=` operator. Use the `+=` operator similar to how it is shown in the example and be sure to include a space between the two strings. Start by assigning the first string to `myStr`, then add on the second string.


### Code Given
```javascript
let myStr;
```

### Answer
```javascript
let myStr = "This is the first sentence. "
myStr += "This is the second sentence."
```

## Constructing Strings with Variables

Sometimes you will need to build a string. By using the concatenation operator (+), you can insert one or more variables into a string you're building.

Example:

```javascript
const ourName = "freeCodeCamp";
const ourStr = "Hello, our name is " + ourName + ", how are you?";
```
ourStr would have a value of the string Hello, our name is freeCodeCamp, how are you?.

### Test
1. Set `myName` to a string equal to your name and build `myStr` with myName between the strings `My name is and` and `I am well!`

### Code Given

```javascript
// Only change code below this line
const myName = "";
const myStr = "";
```

### Answer

```javascript
// Only change code below this line
const myName = "V Sagar";
const myStr = "My name is and " + myName + "I am well!";
```

## Appending Variables to Strings

Just as we can build a string over multiple lines out of string literals, we can also append variables to a string using the plus equals `(+=)` operator.

Example:

```javascript
const anAdjective = "awesome!";
let ourStr = "freeCodeCamp is ";
ourStr += anAdjective;
```
`ourStr` would have the value freeCodeCamp is awesome!.

### Test
1. Set `someAdjective` to a string of at least 3 characters and append it to `myStr` using the `+=` operator.

### Code Given
```javascript
// Change code below this line
const someAdjective = "";
let myStr = "Learning to code is ";
```

### Answer
```javascript
// Change code below this line
const someAdjective = "awesome";
let myStr = "Learning to code is ";
myStr += someAdjective;
```

## Find the Length of a String

You can find the length of a String value by writing `.length` after the string variable or string literal.

`console.log("Alan Peter".length);` <br>

The value 10 would be displayed in the console. Note that the space character between "Alan" and "Peter" is also counted.

For example, if we created a variable `const firstName = "Ada",` we could find out how long the string `Ada` is by using the `firstName.length` property.

### Test
1. Use the `.length` property to set `lastNameLength` to the number of characters in lastName.

### Code Given
```javascript
// Setup
let lastNameLength = 0;
const lastName = "Lovelace";

// Only change code below this line
lastNameLength = lastName;
```

### Answer
```javascript
// Setup
let lastNameLength = 0;
const lastName = "Lovelace";

// Only change code below this line
lastNameLength = lastName.length;
```


## Use Bracket Notation to Find the First Character in a String

Bracket notation is a way to get a character at a specific index within a string.

Most modern programming languages, like JavaScript, don't start counting at 1 like humans do. They start at 0. This is referred to as Zero-based indexing.

For example, the character at index 0 in the word Charles is C. So if const firstName = "Charles", you can get the value of the first letter of the string by using firstName[0].

Example:

```javascript
const firstName = "Charles";
const firstLetter = firstName[0];
```
firstLetter would have a value of the string C.

### Test
1. Use bracket notation to find the first character in the lastName variable and assign it to firstLetterOfLastName.

### Code Given
```javascript
// Setup
let firstLetterOfLastName = "";
const lastName = "Lovelace";

// Only change code below this line
firstLetterOfLastName = lastName; // Change this line
```

### Answer
```javascript
// Setup
let firstLetterOfLastName = "";
const lastName = "Lovelace";

// Only change code below this line
firstLetterOfLastName = lastName[0];
```

## Understand String Immutability

In JavaScript, String values are immutable, which means that they cannot be altered once created.

For example, the following code will produce an error because the letter B in the string Bob cannot be changed to the letter J:

```javascript
let myStr = "Bob";
myStr[0] = "J";
```
Note that this does not mean that myStr could not be re-assigned. The only way to change myStr would be to assign it with a new value, like this:

```javascript
let myStr = "Bob";
myStr = "Job";
```

### Test
1. Correct the assignment to myStr so it contains the string value of Hello World using the approach shown in the example above.

### Code Given
```javascript
// Setup
let myStr = "Jello World";

// Only change code below this line
myStr[0] = "H"; // Change this line
// Only change code above this line
```

### Answer
```javascript
// Setup
let myStr = "Jello World";

// Only change code below this line
myStr = "Hello World"; 
```

## Use Bracket Notation to Find the Nth Character in a String

You can also use bracket notation to get the character at other positions within a string.

Remember that computers start counting at 0, so the first character is actually the zeroth character.

Example:

```javascript
const firstName = "Ada";
const secondLetterOfFirstName = firstName[1];
```
`secondLetterOfFirstName` would have a value of the string `d`.

### Test
1. Let's try to set thirdLetterOfLastName to equal the third letter of the lastName variable using bracket notation.

### Code Given
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const thirdLetterOfLastName = lastName; // Change this line
```

### Answer
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const thirdLetterOfLastName = lastName[2];
```

## Use Bracket Notation to Find the Last Character in a String

In order to get the last letter of a string, you can subtract one from the string's length.

For example, if 
```javascript
const firstName = "Ada",
```
 you can get the value of the last letter of the string by using `firstName[firstName.length - 1]`.

Example:

```javascript
const firstName = "Ada";
const lastLetter = firstName[firstName.length - 1];
```
`lastLetter` would have a value of the string `a`.

### Test
1. Use bracket notation to find the last character in the lastName variable.

### Code Given
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const lastLetterOfLastName = lastName; // Change this line
```

### Answer
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const lastLetterOfLastName = lastName[lastName.length - 1];
```

## Use Bracket Notation to Find the Nth-to-Last Character in a String

You can use the same principle we just used to retrieve the last character in a string to retrieve the Nth-to-last character.

For example, you can get the value of the third-to-last letter of the const `firstName = "Augusta"` string by using `firstName[firstName.length - 3]`

Example:

```javascript
const firstName = "Augusta";
const thirdToLastLetter = firstName[firstName.length - 3];
```
`thirdToLastLetter` would have a value of the string `s`.

### Test
1. Use bracket notation to find the second-to-last character in the lastName string.

### Code Given
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const secondToLastLetterOfLastName = lastName; // Change this line
```


### Answer
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const secondToLastLetterOfLastName = lastName[lastName.length-2];
```

## Word Blanks

You are provided sentences with some missing words, like nouns, verbs, adjectives and adverbs. You then fill in the missing pieces with words of your choice in a way that the completed sentence makes sense.

Consider this sentence:

It was really ____, and we ____ ourselves ____.
This sentence has three missing pieces- an adjective, a verb and an adverb, and we can add words of our choice to complete it. We can then assign the completed sentence to a variable as follows:

`const sentence = "It was really " + "hot" + ", and we " + "laughed" + " ourselves " + "silly" + ".";`

### Test
1. In this challenge, we provide you with a noun, a verb, an adjective and an adverb. You need to form a complete sentence using words of your choice, along with the words we provide.

You will need to use the string concatenation operator + to build a new string, using the provided variables: myNoun, myAdjective, myVerb, and myAdverb. You will then assign the formed string to the wordBlanks variable. You should not change the words assigned to the variables.

You will also need to account for spaces in your string, so that the final sentence has spaces between all the words. The result should be a complete sentence.

### Code Given
```javascript
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

// Only change code below this line
const wordBlanks = ""; // Change this line
// Only change code above this line
```

### Answer
```javascript
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

// Only change code below this line
const wordBlanks = "That " + myAdjective +" " + "size " + myNoun +" " + myVerb + " " + "very "+ myAdverb; 
```

## Store Multiple Values in one Variable using JavaScript Arrays

With JavaScript array variables, we can store several pieces of data in one place.

You start an array declaration with an opening square bracket, end it with a closing square bracket, and put a comma between each entry, like this:

`const sandwich = ["peanut butter", "jelly", "bread"];`

### Test
1. Modify the new array `myArray` so that it contains both a string and a number (in that order).

### Code Given
```javascript
// Only change code below this line
const myArray = [];
```

### Answer
```javascript
const myArray = ["Apple",  1, "Mango", 2];
```
## Nest one Array within Another Array
You can also nest arrays within other arrays, like below:

`const teams = [["Bulls", 23], ["White Sox", 45]];` <br>

This is also called a multi-dimensional array.


### Test
1. Create a nested array called myArray.

### Code Given
```javascript
// Only change code below this line
const myArray = [];
```

### Answer
```javascript
const myArray = [["Apple", 1], ["Mango", 2]];
```

## Access Array Data with Indexes

We can access the data inside arrays using indexes.

Array indexes are written in the same bracket notation that strings use, except that instead of specifying a character, they are specifying an entry in the array. Like strings, arrays use zero-based indexing, so the first element in an array has an index of 0.


Example

```javascript
const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];
```
The `console.log(array[0])` prints `50`, and data has the value 60.

### Test
1. Create a variable called `myData` and set it to equal the first value of `myArray` using bracket notation.

### Code Given
```javascript
const myArray = [50, 60, 70];
```

### Answer
```javascript
const myArray = [50, 60, 70];
const myData = myArray[0]

```


## Modify Array Data With Indexes
Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with const.

*Example*

```javascript
const ourArray = [50, 40, 30];
ourArray[0] = 15;
```
`ourArray` now has the value `[15, 40, 30]`.

**Note:** There shouldn't be any spaces between the array name and the square brackets, like array [0]. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

### Test

1. Modify the data stored at index 0 of myArray to a value of 45.

### Code Given
```javascript
// Setup
const myArray = [18, 64, 99];

// Only change code below this line
```

### Answer
```javascript
// Setup
const myArray = [18, 64, 99];

myArray[0] = 45;
```

### Access Multi-Dimensional Arrays With Indexes

One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outermost (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

*Example*

```javascript
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

In this example, `subarray` has the value `[[10, 11, 12], 13, 14]`, `nestedSubarray` has the value `[10, 11, 12]`, and `element` has the value `11` .

Note: There shouldn't be any spaces between the array name and the square brackets, like `array [0][0]` and even this `array [0] [0]` is not allowed. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

### Test
1. Using bracket notation select an element from myArray such that myData is equal to 8.

### Code Given
```javascript
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[0][0];
```

### Answer
```javascript
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[2][1];
```

## Manipulate Arrays With push Method
An easy way to append data to the end of an array is via the `push()` function.

`.push()` takes one or more parameters and "pushes" them onto the end of the array.

Examples:

```javascript
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```
`arr1` now has the value `[1, 2, 3, 4]` and `arr2` has the value `["Stimpson", "J", "cat", ["happy", "joy"]]`.


### Test
1. Push `["dog", 3]` onto the end of the myArray variable.

### Code Given
```javascript
// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line
```

### Answer
```javascript
const myArray = [["John", 23], ["cat", 2]];
myArray.push(["dog", 3]);
```

## Manipulate Arrays With pop Method

Another way to change the data in an array is with the `.pop()` function.

`.pop()` *is used to pop a value off of the end of an array.* We can store this popped off value by assigning it to a variable. In other words, `.pop()` removes the last element from an array and returns that element.

Any type of entry can be popped off of an array - numbers, strings, even nested arrays.

```javascript
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```
The first `console.log` will display the value `6`, and the second will display the value `[1, 4]`.

### Test
1. Use the `.pop()` function to remove the last item from myArray and assign the popped off value to a new variable, removedFromMyArray.

### Code Given
```javascript
// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line

```

### Answer
```javascript
// Setup
const myArray = [["John", 23], ["cat", 2]];

const removedFromMyArray = myArray.pop();

```

## Manipulate Arrays With shift Method

`pop()` always removes the last element of an array. What if you want to remove the first?

That's where `.shift()` comes in. It works just like `.pop()`, except it removes the first element instead of the last.

Example:

```javascript
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```
`removedFromOurArray` would have a value of the string Stimpson, and ourArray would have `["J", ["cat"]]`.

### Test
1. Use the `.shift()` function to remove the first item from `myArray` and assign the "shifted off" value to a new variable, `removedFromMyArray`.

### Code Given
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];

// Only change code below this line

```

### Answer
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];
const removedFromMyArray = myArray.shift();
```
## Manipulate Arrays With unshift Method

Not only can you shift elements off of the beginning of an array, you can also unshift elements to the beginning of an array i.e. add elements in front of the array.

`.unshift()` *works exactly like `.push()`, but instead of adding the element at the end of the array*, `unshift()` adds the element at the beginning of the array.

Example:
```javascript
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```
After the shift, `ourArray` would have the value `["J", "cat"]`. After the `unshift`, `ourArray` would have the value `["Happy", "J", "cat"]`.

### Test
1. Add ["Paul", 35] to the beginning of the myArray variable using unshift().

### Code Given 
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];
myArray.shift();

// Only change code below this line
```

### Answer
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];
myArray.shift();
myArray.unshift(["Paul", 35]);
```

## Shopping List
Create a shopping list in the variable myList. The list should be a multi-dimensional array containing several sub-arrays.

The first element in each sub-array should contain a string with the name of the item. The second element should be a number representing the quantity i.e.

`["Chocolate Bar", 15]`

### Test 
1. There should be at least 5 sub-arrays in the list. `myList` should be an array.

### Code Given
```javascript
const myList = [];
```

### Answer
```javascript
const myList = [["Colddrink", 2], ["Apple", 6], ["Deodrant", 3], ["Toothpaste", 1], ["Towel", 2],];
```
## Write Reusable JavaScript with Functions
*In JavaScript, we can divide up our code into reusable parts called* `functions`.

Here's an example of a function:

```javascript 
function functionName() {
  console.log("Hello World");
}
```
You can call or invoke this function by using its name followed by parentheses, like this: `functionName()`; Each time the function is called it will print out the message Hello World on the dev console. All of the code between the curly braces will be executed every time the function is called.

### Test
1. Create a function called `reusableFunction` which prints the string `Hi World` to the dev console.
2. Call the function.

### Answer
```javascript
function reusableFunction(){
console.log("Hi World")};
reusableFunction();
```

## Passing Values to Functions with Arguments
*Parameters are variables that act as placeholders for the values that are to be input to a function when it is called.* When a function is defined, it is typically defined along with one or more parameters. *The actual values that are input (or "passed") into a function when it is called are known as arguments.*

Here is a function with two parameters, param1 and param2:

```javascript
function testFun(param1, param2) {
  console.log(param1, param2);
}
```
Then we can call `testFun` like this: `testFun("Hello", "World");`. We have passed two string arguments, Hello and World. Inside the function, `param1` will equal the string `Hello` and `param2` will equal the string `World`. Note that you could call testFun again with different arguments and the parameters would take on the value of the new arguments.

### Test
1. Create a function called `functionWithArgs` that accepts two arguments and outputs their sum to the dev console.
2. Call the function with two numbers as arguments.

### Answer
```javascript
function functionWithArgs(a,b){
    console.log(a+b)
}
functionWithArgs(1,2);
functionWithArgs(7,9);
```

### Return a Value from a Function with Return
We can pass values into a function with arguments. You can use a return statement to send a value back out of a function.

Example

```javascript
function plusThree(num) {
  return num + 3;
}

const answer = plusThree(5);
```
answer has the value 8.

plusThree takes an argument for num and returns a value equal to num + 3.


### Test
1. Create a function `timesFive` that accepts one argument, multiplies it by 5, and returns the new value.

### Answer
```javascript
function timesFive (num){
    return num*5
}
console.log(5);
console.log(2);
console.log(0);
```


