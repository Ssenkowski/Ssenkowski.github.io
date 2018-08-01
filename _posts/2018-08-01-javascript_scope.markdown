---
layout: post
title:      "Javascript "Scope""
date:       2018-08-01 12:30:29 -0400
permalink:  javascript_scope
---


The concept of scope in JavaScript determines the accessibility of variables or basically when and where you can use a variable.

In JavaScript there are two types of scope the ***local scope*** and the ***global scope***.

### Local Scope

***Local scope*** JavaScript variables can also have what's called ***function scope***.

 Variables defined within a function can only be used within that function ( ***"function scope"***).  

  For example:

	```
	function breakfast() {

	var meal = "Eggs and Toast";

	// the variable "meal" can be used here and return "Eggs and Toast"

	}

	// Out here the variable "meal" will return undefined.  It is out of "scope".
	```

	 These local variables are created when a function starts and deleted when the function is complete.

### Global Scope

 For variables declared outside of the function it  has a global  scope.   Variables with a ***global scope*** can be accessed by any scripts or function on a webpage.

### Weird Part!!!

 ***If you assign a variable of value without declaring it with "var", "let", or "const"  it will automatically become a global variable even if it's assigned within a function.***
