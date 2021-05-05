Arrays are a a powerful and comprehensive tool of Javascript. They are very intuitive to use and you can do almost everything with it. However, there are important differences between arrays in Javascript and other mainstream languages. Knowing them will help you unleash their true potential.

In this lesson we will go through the important aspects of arrays that are imperative to every JS developer and  also we will see the variety of usages they have.

## Arrays are just regular objects
In Javascript, there are only 6 data types defined:
 – the primitives (boolean, number, string, null, undefined) 
 and object (the only reference type). 
 
 > 🛑 Arrays do not belong to this list because they are objects as well. This is a common confusion among developers who assume that arrays are a special data type in Javascript.

The items in the array are nothing more than properties of that objects. You can use any name as property for an objects, including numbers or even empty string. However, if the property name is not a valid identifier (doesn’t start with a letter), you can only access it through obj[property_name] and not obj.property_name.

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

👉 arrays also have a special properties lenght and many function that can manipulate the elements

## How to Declare an array? 🤔