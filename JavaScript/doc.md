## Reference ##
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide

JavaScript 
- client side (place elements on the webpage, respond to user events)
- server side (nodeJS, respond to REST calls, IAM, interact with Db, etc)
            
JS v/s Java
- no type checking in JS
- you can add proterties and methods to an object on run time in case of JS
- no need to decare variables and mothods in JS
- no public or private or proteced in JS
- no type for variables and function return types in JS

ECMA - international association for standardizing JS

- JS is case sensitive
- A semicolon is not necessary after a statement if it is written on its own line. But if more than one statement on a line is desired, then they must be separated by semicolons.

Declarations
- var (local or gloabal variable, optionally initialized)
- let (block scoped variable, optionally initialized)
- const (block scoped variable, read only, mandatory initialized)
- x=32 (uninitialized global variable)
- Uninitialized variables have default value of undefined
- An attempt to access an undeclared variable results in a ReferenceError exception being thrown
  console.log('The value of c is ' + c); // Uncaught ReferenceError: c is not defined
- The undefined value behaves as false when used in a boolean context.
- The undefined value converts to NaN when used in numeric context.
- When you evaluate a null variable, the null value behaves as 0 in numeric contexts and as false in boolean contexts.

Variable Scope (before ES6)
- JS has no block level scope but only a function level scope.
- a variable declared within a block is local to the function (or global scope) that the block resides within.
if (true) {
  var x = 5;
}
console.log(x);  // x is 5 as x has global scope

Variable Hoisting
- var :- you can refer to a variable declared later, without getting an exception. variables in JavaScript are in a sense "hoisted" or lifted to the top of the function or statement.
- let/const :- Referencing the variable in the block before the variable declaration results in a ReferenceError.

Function Hoisting
- only function declaraion gets hoisted at the top, not function expression
- function foo() { ...} // function declaration hoisted, you can call this function before its definition
- var foo = function() { ...} // function expression not hoisted,  calling this before definition leads to Reference Exception

const variable in JS
- Block scope as let
- if const keyword is omitted, it becomes a var
- const cannot be reassigned a value and you cannot re-declare a variable declared as const in the same scope
- const objects :- properties or contents of the object are not protected/constant i.e you can add/modify properties
  eg const obj = {a:b}; obj.a=c;
- const arrays :- array values or contents of the array are not protected i.e you can add/modify array values

Type Conversion
- As JS is a dynamically types language, type conversions and assignments happen automatically at run time.
  eg var ans = 5; ans = true; ans = "hello" // ans can be re-assigned any type of value
- '+' operator converts numerals to string. Other operators do not perform this conversion
  eg var res = '34'+5 \\ res becomes 345
     var res = '34'-5 \\ res becomes 29

String to numbers
- parseInt() and parseFloat()
- Unary '+' operator
  eg +'6.5' + +'6.2' // 12.7

Array Literals
- Extra comma means value is undefined. Extra comma at the last is ignored
  eg var arr = [,2,,3,,] // arr is undefined, 2, undefined, 3, undfined.
  
Numeric Literals
- eg var lit = 054 // octal 54, var lit = 0o34 // octal 34, var lit = 0xA4 // hex A4, var lit = 0b10 // binary 10

Object Properties
- can be any identifier including numerals, special char, empty string.
- Property names that are not valid identifiers also cannot be accessed as a dot (.) property, but can be accessed and set with the array-like notation("[]").
  eg var obj = { '' : 'abc', '@' : 'bcd', 5: 'xyz'}
    obj.'' or obj.@ or obj.5 // error
    obj[''] or obj['@'] or obj[5] // no error

Object Literals (from ES6)
- Property names that are not valid identifiers also cannot be accessed as a dot (.) property, but can be accessed and set with the array-like notation("[]").
  eg var obj = {
    // __proto__
    __proto__: theProtoObj,
    // Shorthand for ‘handler: handler’
    handler,
    // Methods
    toString() {
     // Super calls
     return 'd ' + super.toString();
    },
    // Computed (dynamic) property names
    [ 'prop_' + (() => 42)() ]: 42
    };
    
Template Literals (introduced in ES6)
- enclosed within back ticks`` instead of quotes or double quotes.
  eg var name = 'Bob', time = 'today';
    `Hello ${name}, how are you ${time}?`



