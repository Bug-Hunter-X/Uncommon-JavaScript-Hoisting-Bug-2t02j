# Uncommon JavaScript Hoisting Bug
This repository demonstrates a subtle bug related to variable hoisting in JavaScript.  The code appears to declare a variable, but due to hoisting, this leads to unexpected behavior. 
The `bug.js` file shows the buggy code. The `bugSolution.js` file demonstrates the fix.

## Bug Description
In JavaScript, variable declarations using `var` are hoisted to the top of their scope. However, only the *declaration* is hoisted, not the *initialization*.  This means that referencing a variable before it's assigned a value results in `undefined`, not a ReferenceError.

## How to Reproduce
1. Clone this repository.
2. Run `bug.js` using Node.js (or a similar JavaScript runtime).
3. Observe that the output is `undefined` rather than `10`.

## Solution
The solution is to ensure variables are assigned a value before being accessed.