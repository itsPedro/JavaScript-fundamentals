# JavaScript fundamentals you need to know in React

> There's its a article focus to explain not the basics => const, let, var etc...


# Table of contents

- [Functions](#Functions)
- [Arrow Functions](#Arrow)
- [Exporting a function](#Exporting)
- [Conditioning](#Conditioning)
- [Ternary Operator](#Ternary)
- [Objects](#Objects)


## **Functions**


## Arrow Functions

Arrow functions its another way to define one function Examples:


**Before (Without arrow function)**

``` javaScript
function doSomething() {

}
```


**After (With arrow function)**

``` javaScript
const doSomething = () => {

}
```


## Exporting a function


**Before**

``` javaScript
export default doSomething() {

}
```
**After**

``` javaScript
export const doSomething = () => {

}
```


You might ask, "Why is this important in React?" The answer is that in React, you define components that are basically functions that return HTML. This is specific to React.



**Example:**

``` javaScript
const MyComponent = () => {
    return <div></div>
}
```

Another important thing is anonymous functions. This can be a bit weird when you first see it in the context of React.


**Example:**

``` html
<button onClick={() => {console.log('Hello');}}></button>;
```


## **Conditioning**


## Ternary Operator


This is very useful in React because when you're coding the UI portion of the site, it's important to make the code clear and use the minimum number of lines of code. Simply put, it allows you to write more concise and readable code.



**When you're coding in React, you don't want something like this:**

``` javaScript
if (true) {

} else {

}
```

Imagine you have a number `age = 18` and a string `name = 'Pedro'`. You want to check if `age` is greater than 18, and if it is, set `name` to 'Pedro', otherwise, set it to 'John'. With an if statement, you would do something like this:

``` javaScript
let age = 18;
let name = 'Pedro';

if (age > 18) {
    name = 'Pedro'
} else {
    name = 'John'
}
```

This takes up a lot of space in your code. There is another way to do this using the ternary operator. It's like speaking to the computer and saying "Ok, let `name` equal 'Pedro' if `age` is greater than 18."

**Example:**

``` javaScript
let age = 18;
let name = age > 18 ? 'Pedro' : 'John';
```

**This is a specific case, but you can also use it in a different way, like this:**

``` javaScript
let age = 18;
let name = age > 18 && 'Pedro';
```

**Applying this to what we learned before:**

``` javaScript
let age = 18;
let name = age > 18 ? 'Pedro' : 'John';

const Component = () => {
    return age > 18 ? <div> Pedro</div> : <div> John</div>;
}
```

# Objects

Objects are very useful and probably one of the most useful data structure a language can have and in react its a very important thing.

Imagine we have a object called `person` and has three proprieties witch its `name` (string), `age` (number) and `isMarried` (boolean).

``` javaScript
const person = {
    name: "Pedro",
    age: 18,
    isMarried: false,
};
```


Usually if you want to create variables to represent these values inside the object you can make on that way.

``` javaScript
const name = person.name;
const age = person.age;
const isMarried = person.isMarried;
```


Thats one way to do it, its fine but we want to write more concise and readable code here. With that in mind you could make using structuring proprieties of objects in a single line.

``` javaScript
const { name, age, isMarried } = person;
```


On that you declare three different variables with corresponding proprieties inside `person` and this its a good thing to do in React.


Another thing about objects are if you have a variable with `same name of the property` on the object.

**Instead of doing it this way**
``` javaScript
const name = "Pedro";

const person = {
    name: name,
    age: 18,
    isMarried: false,
};
```
**You can do**
``` javaScript
const name = "Pedro";

const person = {
    name,
    age: 18,
    isMarried: false,
};
```


Keep in mind that its just a recommend both ways will work normally

# I'm will add more information here in the future.

### License

Copyright © 2023, [Pedro Reis](https://github.com/itsPedro). Released under the [MIT License](LICENSE).
