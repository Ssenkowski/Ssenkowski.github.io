---
layout: post
title:      "Javascript "Hoisting""
date:       2018-07-28 13:51:23 -0400
permalink:  javascript_hoisting
---


The JavaScript engine does a few things that may seem weird to me developers or even experienced developers.  "Hoisting"  is one of those things.

  **Hoisting** is JavaScript's programmed behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).   (https://www.w3schools.com/js/js_hoisting.asp)

```
y = 5; // Assign 5 to y

element = document.getElementById("demo"); // Find an element
element.innerHTML = y;                     // Display y in the DOM element

var y; // Declare y
```



```
var y; // Declare y
y = 5; // Assign 5 to y

element = document.getElementById("demo"); // Find an element
element.innerHTML = y;                     // Display y in the DOM element
```

In both of the previous code  examples the browser would output the number five despite the order of assigning "y" a value and declaring the variable "y".   Again the reason is because JavaScript by default, moves all declarations of variables to the top of the current scope.

 It's worth noting that JavaScript only does this with declarations.   A JavaScript initialization like the following example would not be hoisted.

 ```
var x = 9; // Initialize x

element = document.getElementById("demo"); // Find an element
element.innerHTML = x + " " + y;           // Display x and y in the DOM element

var y = 10; // Initialize y
```

 In the above example from  you would see the number 9 in the DOM, but you would not see the number 10.   Because the variable Y is being initialized after being called and not declared, it will not be hoisted to the top and therefore displayed in the DOM.  In the next example, both x and y will appear in the DOM as "9" and "10" because they have been initialized prior to being called.

 ```
var x = 9; // Initialize x
var y = 10; // Initialize y

element = document.getElementById("demo"); // Find an element
element.innerHTML = x + " " + y;           // Display x and y in the DOM element
 ```

  It's usually recommended that since hoisting is commonly overlooked by developers, that best practice is to simply **declare your variables at the top** of whatever scope they're being used in.
