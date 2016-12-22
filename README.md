### Explain the two strategies for improving JavaScript: ES6 (es2005) + ES7, versus Typescript. What does it require to use these technologies: In our backend with Node, in (many different) Browsers.

ES6 and Typescript are not yet implemented in the browsers, therefore we need to compile it to ES5, since most browsers will support that.

--------------------------------------------------------------------------------------------------------------------

### Provide examples and explain the es2005 features: let, arrow functions, this, rest parameters, de-structuring assignments, maps/sets etc.

- Let
  - "let" is the way you narrow down the scope. If you use "let" in a function, that variabel will only be accessible inside that very function.
    No other function is able to see that variabel.

- Arrow
  - We are using the arrow function to make ones code easier to read. It's used to shorten down ones code aswell, and if is easy to use if you don't have to name the function.
    Another thing to add, it treats "this" differently than normal.

- Rest parameters
  - Rest parameters allows your functions to have variable number of arguments without using the arguments object. The rest parameter is an instance of Array so all the array methods just work. 
    Note that there can only be a single rest parameter for a given function. This means that listAnimals(...cats, ...dogs) will not work, whilst listAnimals(...cats) will work just fine.

--------------------------------------------------------------------------------------------------------------------

### Provide an example of ES6 inheritance and reflect over the differences between Inheritance in Java and in ES6

In ES6, the class that inherits from another class, will not need a kontstruktor. Square still have access to the constructor from the Shape class. But in JavaScript there MUST be a constructor.

In JAVA there is no need for a constructor, but if you do have a constructor, there have to be a constructor in the classes that inherits.

```javascript
class Shape {
  constructor(color) {
    this._color = color;
    this._perim = "";
    this._area = "";
  }
}

class Firkant extends Shape {
  returncolor() {
    return this._color;
  }
}

var firkant = new Firkant("grøn");
console.log(firkant.returncolor())
```

--------------------------------------------------------------------------------------------------------------------

### Explain about TypeScript, how it relates to JavaScript, the major features it offers and what it takes to develop Server and Client side applications with this technology.

Typescript is built on javascript: The TypeScript compiler is itself written in TypeScript, transcompiled to JavaScript. It's class-based.

One is able to make types:

```javascript
let isDone: boolean = false;
let msg: string = "Hello World";
//Array
let numbers: Array<number> = [1,2,3];
//Enum
enum Color {Red, Green, Blue}
//void
function warnUser(): void {
    alert("This is my warning message");
}
```

TypeScript add Classes and Inheritance "much" like we know from Java/C# with:
Class, Constructor, Extends, Implements, Access Modifiers, public (default), private, protected, readonly, Parameter properties, abstract, static, getters/setters (like C#)
