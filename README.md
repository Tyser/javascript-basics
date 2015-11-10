

This is a repo to show some of the basics of programming in the context of
JavaScript. This repo will be using ECMAScript 5 Standard. This is a document
on JavaScript as a language and not on JavaScript in a browser environment.

<!-- TOC depth:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Variables](#variables)
	- [Declaration](#declaration)
	- [Data Types](#data-types)
		- [Primitive](#primitive)
		- [Reference](#reference)
		- [Functions](#functions)
	- [Logic (Control Flow)](#logic-control-flow)
	- [Loops](#loops)
<!-- /TOC -->

# Variables

Data can be stored in different ways, and knowing how to store data is just as
important as knowing where to store it.

In other programming languages, when you declare a variable, you declare the
data type along with it. In those languages, you can't change the data type of
those variables. In JavaScript, a variable has a loose data type, meaning any
given variable can change data types at any time.

## Declaration

Variables are declared with the keyword `var` followed by a space, and then the
name of the variable.

There are only certain characters that you can use in a variable name. The basic
rule is that a variable name must start with a `$`, `_` or a letter, and the
rest of the characters must be `$`, `_` or any letter or number. The actual rule
is a bit more complicated than that. You can look it up if you want.

A variable also can't be a reserved javascript word. You can see a list of them
[here](http://mdn.beonex.com/en/JavaScript/Reference/Reserved_Words.html).

```js
// Valid
var varName;
var $foo;
var _12345;

// Invalid
var 1a; // Starts with a number
var foo-bar; // Invalid character
var new; // Reserved word
```

One of the most important things that you can learn about variable declaration
is consistency. There are several types of variable naming conventions that
developers use:

* `camelCase` - Words are joined together. The first word is all lowercase, and
  every subsequent word has a capitalized first letter.

  ```js
  var foo;
  var firstName;
  var reallyReallyLongVariableName;
  ```

* `PascalCase` - Like camel case, except every word has a capitalized first
  letter. Usually used for "Class" definitions.

  ```js
  var Foo;
  var FirstName;
  var ReallyReallyLongVariableName;
  ```

* `snake_case` - Words are separated by underscores. All words are lowercase.

  ```js
  var foo;
  var first_name;
  var really_really_long_variable_name;
  ```

* `CONST_CASE` - I'm not actually sure of the name for this, but it's like snake
  case, except everything is all caps. This is used alongside any of the other
  cases when declaring a variable that isn't meant to change.

Camel case and pascal case are usually used together, but you should treat
snake case an camel case as mutually exclusive in order to maintain a more
consistent style.

## Data Types

### Primitive

Primitive data types are data types that store simple data such as numbers
and strings.

* `Number` - In most other programming languages, there are several types of
  "number" data types, such as `integer` and `double`. Numbers in JavaScript are
  always 64-bit floating point numbers or `floats`. It's important to know the
  nuances of floating point numbers. In JavaScript, an integer (number without
  decimal places) is considered accurate up to 15 digits. Anything above that and
  the numbers will start to round in odd ways. You can have a maximum of 17
  decimal places, but when you start to do math with decimals, you can run into
  some funny errors. For example, `0.2 + 0.1` evaluates to `0.30000000000000004`.
  Integer arithmetic is just fine (up to 15 digits).

  ```js
  var min = 0;
  var max = 10;
  var percent = 45.6;
  var expire = 10e5;
  var index = -1;
  ```

* `String` - In other programming languages, there is a distinction between the
  String data type, and the Character data type. They are usually differentiated
  by using single quotes `'` for single characters, and double quotes `"` for
  strings of characters. In JavaScript, everything is strings, and you can use
  single quotes or double quotes. Whatever you decide to use, just be consistent.

  If you are using single quotes for your string, and you need to use a single
  quote, you need to use the escape character `\` before the inner single quote.

  If you want to store a new line character, you use `\n`. If you want to use a
  tab, you use `\t`.

  ```js
  var name = 'Jack Bliss';
  var key = 'c';
  var phrase1 = "John's house";
  var phrase2 = 'John\'s house';
  var street = '123 Main St\nSuite 300';
  var table = 'name\tstreet\tcity\tstate';
  ```

* `Boolean` - True or False. One of the simpler data types. Just an on/off
  switch

  ```js
  var test = false;
  var isFast = true;
  ```

* `undefined` and `null` - There is a very important distinction between
  `undefined` and `null`. `undefined` means that a variable has not been
  assigned a value. `null` is an assigned value that means 'no value'.

  ```js
  var test; // This is undefined
  var foo = null; // This is null
  ```

### Reference

Reference variables are variables that are just "pointers" (not c++ pointers)
to other primitive values or other reference values.

* `Array` - An array is a list of ordered items keyed by index. Indexes are
  Numbers, unless you specify custom ones. Items in an array can be any value
  (or non-value). Arrays can contain arrays of arrays of arrays... and so on.
  You access a value in an array by using the variable name that is storing
  the array, and then using square brackets `[]` with the index you want to
  access between them. Note that arrays in most programming languages are

  ```js
  var arr = [ 1, 2, 3 ];
  var names = [ 'jack', 'joe', 'james' ];
  var longArray = [
    '5',
    5,
    [ 'sub', 'array' ]
  ];
  var map = [
    [ 0, 1, 2, 3, 4 ],
    [ 1, 2, 3, 4, 5 ],
    [ 2, 3, 4, 5, 6 ],
    [ 3, 4, 5, 6, 7 ],
    [ 4, 5, 6, 7, 8 ],
    [ 5, 6, 7, 8, 9 ],
  ];
  ```

* `Object` - An object is similar to an array in that their both considered to
  be objects. You can even have an object with numeric keys like an array, but
  the difference is that order is not guaranteed when looping through. Objects


### Functions

## Logic (Control Flow)

## Loops
