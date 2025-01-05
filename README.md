# JavaScript Closure Gotcha in setTimeout Loops

This repository demonstrates a common JavaScript error related to closures and the `setTimeout` function within loops.  The `bug.js` file contains code that produces unexpected results due to how JavaScript handles variable scoping and closures. The `bugSolution.js` file shows how to correct the issue.

## Problem

The seemingly straightforward code in `bug.js` aims to log numbers 0 through 9 with a one-second delay between each log. However, it incorrectly logs 10 ten times.  This is a classic closure gotcha in JavaScript.

## Solution

The solution, provided in `bugSolution.js`, utilizes an immediately invoked function expression (IIFE) or `let` within the loop to create a new scope for the variable `i` for each iteration of the loop. This ensures that the correct value of `i` is captured by the closure for each `setTimeout` callback.