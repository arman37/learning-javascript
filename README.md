## 📝 Author
[<img src="https://media.licdn.com/dms/image/C5103AQE3SdZqmIyW0A/profile-displayphoto-shrink_200_200/0?e=1533168000&v=beta&t=reTZbwaCbB9R9V47Q9XiBGgGpY6_dS0KSK_gA8WsVCc" align="right" height="70" width="70">](http://armanbhuiyan.com)

##### Arman Bhuiyan <kbd>[Github](https://github.com/arman37) / [LinkedIn](https://www.linkedin.com/in/arman-bhuiyan) / [Facebook](https://www.facebook.com/arman.it37) / [Site](http://armanbhuiyan.com) /  [E-Mail](mailto:arman.it37@gmail.com)</kbd>

# Learning JavaScript

## :top: Topics:
&nbsp; :large_orange_diamond: [Why JavaScript](#whyjs) <br />
&nbsp; :large_orange_diamond: [Function](#function) <br />
&nbsp; :large_orange_diamond: [Object](#object) <br />
&nbsp; :large_orange_diamond: [Prototypal Inheritance](prototype#) <br />
&nbsp; :large_orange_diamond: [Closure/Lexical Scope](#closure) <br />
&nbsp; :large_orange_diamond: [Variable & Function Hoisting](#hoisting) <br />
&nbsp; :large_orange_diamond: [Understanding `this`](#this) <br />
&nbsp; :large_orange_diamond: [The `apply`, `call`, and `bind` methods](#applycallbind) <br />
&nbsp; :large_orange_diamond: [Immediately invoked function expressions (IIFE)](#IIFE) <br />
&nbsp; :large_orange_diamond: [Private properties using closures](#private) <br />
&nbsp; :large_orange_diamond: [Understanding the difference between ‘==’ and ‘===’](#equal) <br />

## :hash: <a name="whyjs">Why JavaScript</a>:
:arrow_right: Why should I use JavaScript? :one:  we don’t have a choice :two: JavaScript is really good. It is lightweight and expressive. <br />
:arrow_right: It is possible to get work done quickly with JavaScript without knowing much about the language, or even knowing much about programming. <br />
:arrow_right: It is a language with enormous expressive power. <br />
:arrow_right: JavaScript is an universal programming language <br />
:arrow_right: JavaScript is a remarkably powerful language because it has more in common with Lisp and Scheme than with Java. It is Lisp in C’s clothing. <br />
:arrow_right: JavaScript functions are first class objects with lexical scoping. <br />
:arrow_right: JavaScript has a very powerful object literal notation. Objects can be created simply by listing their components which was the inspiration for JSON (data interchange format). <br />
:arrow_right: **Functions**, **loose typing**, **dynamic objects**, **expressive object literal notation** are some of the good parts of JS (except a programming model based on global variables). <br />

## :hash: <a name="hoisting">Variable & Function Hoisting</a>:
In JavaScript, a **variable** or a **function** can be used before its been declared.
Consider the Following code example:

```
a = 10;
f();

function f() {
  console.log(a);         // prints value of a
}

var a;
```
Why code works this way in JavaScript? Its because of the term **_Hoisting_**. Before code execution, JavaScript has a default behavior of scanning and moving all declared variables and functions to the top of the current scope of the **current script** or **current function** called hoisting. <br /><br />
JavaScript code runs in two phases: :one: Declaration Phase :two: Execution Phase. <br />
**Declaration Phase**: When JavaScript interpreter starts to run code from a script or function, first it scans for all variables and functions declared in that script or function and move them to the top of the scope but doesn't assign them any value yet. <br />
**Execution Phase**: In this phase JavaScript interpreter starts to run code from top to bottom, line by line. <br /> <br />
**Note**: Functions declared with `var` keyword (`var f = function() {}`) are not hoisted and JavaScript only hoists variable declaration not assignment/initialization.
Consider the Following code example:

```
f();                     //  logs error 'f is not a function' since assignment isn't hoisted.
var f = function() {
  //function body
};

var a;
console.log(a);         // prints 'undefined' since variable initialization isn't moved to the top of scope.
a = 10;
```
**Note**: Although with ES6 JavaScript offers block level scope, variables declared with `let` or `const` keyword are only hoisted to the top of the block not to the top of the script or function. <br />
**Best Practice**:
 - Always declare variables to the top of the function or script.
 - Use function level `strict mode` to expose undeclared variables.
 - Avoid using `var`, use `let` or `const` instead.

### Contributing
If you like the project, shoot a :star2: and feel free to fork & send PR.


### License

[MIT licensed](./LICENSE)
