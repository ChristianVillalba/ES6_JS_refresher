# ES6: JavaScript Refresher
Keeping up with the new ES6 (JavaScript)

Notes from: JavaScript Refresher 
[React - The Complete Guide](https://www.udemy.com/course/react-the-complete-guide-incl-redux/)  
Instructor: Maximilian Schwarzmüller

## Description

React apps typically are built with the latest version of JavaScript (ES6)        
and using the next gen features allows us to write clean and robust React apps.

Content:
* Let & Const
* Arrow Functions
* Exports and Imports
* Classes
* Classes, Properties & Methods
* The Spread & Rest Operator
* Destructuring
* Reference and Primitive Types Refresher
* Refreshing Array Functions
* Wrap Up
* Summary: Next-Gen JS
---

### Let & Const

`var`: creates a variable in JavaScript.      
With ES6, a version of JS, two different keywords were introduced: **let & const**.        
Var still works but you're highly encouraged to use let and const.

`let`: for **variable values**. The new var, for values that will change.       
`const`: for **constant value**, we only assign once and never change.

### Arrow Functions

`param => expression`

The **Arrow Function** is a compact alternative to a traditional function expression,       
but is limited and can't be used in all situations.       
[Arrow function expressions - Mozilla Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)  

The **Arrow Function** snyntax is shorter than the normal syntax since it omits the **function** keyword.         
It solves a lot of the issues you often had with the **this** keyword in JS:        
Using **this** inside an arrow function will always keep its context and not change it surprisingly.         
[ES6: Arrow Functions JS practice](https://github.com/ChristianVillalba/ES6_arrow_functions)  

### Exports & Imports

ES6 allow us to write modular code so JS code you split up over multiple files.       
The idea behind **export and import Statements** and so-called modules is that       
inside of a JS file we can import content from another file so that           
the JS files themselves know their **dependencies**.
[ES6: import, export and modules](https://github.com/ChristianVillalba/es6_import_export_and_modules)    

### Classes

Classes are kind of a more convenient way of creating constructor functions        
so you create javascript objects with classes and classes also support inheritance.      
In order to support inheritance, we must add the method `super()`.        
Classes are used by React to create its components (there are 2 ways for that).      
[Functional Component & Class Component](https://github.com/ChristianVillalba/functional_components_and_class_components)    

### Classes, Properties & Methods

ES6  also offers a different syntax of initializing properties and methods.       
**Properties:** variables attached to classes / objects.       
**Methods:** functions attached to  classes / objects.   

ES7:     
We can assign a Property directly inside our Class with:        
`myProperty = "value"`         
We can think of a Method as a property which stores a function as a value:         
`myMethod = () => {...}`  (eg: using an Arrow Function)        


