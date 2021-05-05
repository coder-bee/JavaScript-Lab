Arrays are a a powerful and comprehensive tool of Javascript. They are very intuitive to use and you can do almost everything with it. However, there are important differences between arrays in Javascript and other mainstream languages. Knowing them will help you unleash their true potential.

In this lesson we will go through the important aspects of arrays that are imperative to every JS developer and  also we will see the variety of usages they have.

## Arrays are just regular objects
In Javascript, there are only 6 data types defined:
 – the primitives (boolean, number, string, null, undefined) 
 and object (the only reference type). 
 
 > 🛑 Arrays do not belong to this list because they are objects as well. This is a common confusion among developers who assume that arrays are a special data type in Javascript.

The items in the array are nothing more than properties of that objects. You can use any name as property for an objects, including numbers or even empty string. However, if the property name is not a valid identifier (doesn’t start with a letter), you can only access it through obj[property_name] and not `obj.property_name`.

nothing stop us from taking an object and declaring properties like 0, 1, 2 and so on and accessing through obj[0], obj[1] and so on. You don’t need a special data type for doing that in Javascript.

```js
//  your  object 
var obj = {
0: 1,
1: 2,
'cat': 'meaow', 
'': 'empty string'
};

console.log(obj[0], obj[1], obj['cat'], obj['']);

```

## What is special about array object then?

> 🛑 An array has, alongside its elements, a special property named length and a generous collection of methods for manipulating the elements. They represent the real power of arrays. You can search, sort, delete, insert and even simulate behavior of other collection data types, like queue and stack.

⚠️ Remember:

👉 arrays are normal objects and their elements are properties with names 0, 1 and so on. 

👉 arrays also have a special properties length and many function that can manipulate the elements

## How to Declare an array? 🤔

Javascript’s literal syntax is for the most common building blocks: object, functions and array. 

In Javascript, an array literal is a list of expressions, each of which represents an array element, enclosed in a pair of square brackets ' [ ] ' . When an array is created using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.

👉 Object literal property values can be of any data type, including array literals, functions, and nested object literals. Here is another object literal example with these property types:

```js

let Fruits = {
    // an array literal
    fruits: ["apple", "banana", "grape", "watermelon"],
    pos: { // nested object literal
        x: 40,
        y: 300
    },
    onDelivery: function() { // function
        // code here
    }
};

## Object Literal Syntax
Object literals are defined using the following syntax rules:

- colon separates property name from value.
- comma separates each name-value pair from the next.
- comma after the last name-value pair is optional

> 🛑  A literal is the best way to express an array:

```js
var arr = [1, 2, 3, 4];
```

👉 There is an alternative to that, the **Array constructor**:

```js
var arr = new Array(1, 2, 3, 4);
```

👉 There some subtle things you have to care about when using the **array constructor**. Since **Array is a global variable**, it can be modified somewhere else in the script so it may not behave as you expected.

```JS
Array = String; 
var arr = new Array(1, 2, 3, 4); // "1" 
```

One other issue is that if the Array constructor gets only one numerical argument, it will create a list with no elements but with length equal to that argument. So ['Mary'] is identical to new Array('Mary') but [10] it’s not the same thing to new Array(10).


👉 It is possible to omit the new operator when using the Array constructor. It has the same result so new Array('Mary') or simply Array('Mary') are doing the same thing.

⚠️ Remember:

> use array literals instead of the Array constructor
> the Array constructor behaves differently if its only argument is a number


