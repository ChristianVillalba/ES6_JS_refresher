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

### Spread & Rest Operator

The spread and rest operators use the same syntax: `...`       
Its usage determines whether you're using it as the Spread or Rest operator.     

**Spread:** used to split up Array Elements or Object Properties.   
```javascript
const newArr = [...oldArr,4,5,6]
const newObj = {...oldObj,newProp:9}
```
* We want to add all the elements from that oldArr to a newArr plus the elements 4,5 & 6      
* We create newObj with all the props of the oldObj (keys-values) and the newProp

[ES6: Spread Operator](https://github.com/ChristianVillalba/ES6_spread_operator/edit/main/README.md)   

**Rest:** used to merge a list of function arguments into an array.
```javascript
function sortArgs(...args) {
    return args.sort()
}
```
sortArgs receives an unlimited amount of arguments,       
using ...args we only write one argument but we may actually receive more than one       
and they will all be merged together into an array.     

### Destructuring

Destructuring allows you to easily extract Array elements or Object properties and store them in variables.      
It takes out all elements all properties and distributes them in a new array or object (or other data types).   

* Array Destructuring
```javascript
[a,b] = ["123","456"]
console.log(a) // "123"
console.log(b) // "456"
```
* Object Destructuring
```javascript
{name} = {name:"Bilbo", age:129}
console.log(name) // "Bilbo"
console.log(age) // undefined
```

Array Destructuring: the order defines which property we take.          
Object Destructuring: the property name (left) targets the name property of the object (right) and pulls out the value.    
This is the reason why age returns *undefined*           
[Documentation: Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)  

[ES6 Object & Array Destructuring](https://github.com/ChristianVillalba/ES6_object_and_array_destructuring/edit/main/README.md) 


### Reference and Primitive Types

**Primitive Types**      
Numbers, Strings, Booleans, these are Primitive Types.         
Whenever you reassign or you store a variable in another variable, It will **copy** the value.         
eg:
```javascript
const numberA = 1
const numberB = numberA
console.log(numberA) // 1
console.log(numberB) // 1
```


**Reference Types**        
Objects and Arrays are Reference Types.       
Even if we return the same value it will **NOT** actually have copied the value. (It copies the poiter).           
eg:
```javascript
const person1 = {
    name: "Frodo"
};
const person2 = person1;
console.log(person1) // [object Object] {name:"Frodo"}
console.log(person2) // [object Object] {name:"Frodo"}
```
person2 didn't copied person1, instead       
person1 (the Object - {name: "Frodo"}) is stored in memory       
and in the constant person1 we store a **pointer** to that place in memory.       
And if we then assign person1 to person2 that **pointer will be copied**.

We can check this case changing person1.name after it was copied:
```javascript
const person1 = {
    name: "Frodo"
};
const person2 = person1;
person1.name = "Sam"
console.log(person2) // [object Object] {name:"Sam"}
```
We changed person1 and when printing person2, it was changed as well.       
The reason for it is that it just **copied the pointer** and points to the exact same object in memory.      
It's important keep this in mind because it can lead to unexpected behaviors in React.       
We will learn techniques to copy this in an immutable way which means         
we copy that by really copying the object and not just a pointer 

### Refreshing Array Functions



