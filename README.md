# Unexpected behavior with null and undefined values

This repository demonstrates an example of unexpected behavior that can occur in JavaScript when null or undefined values are passed to a function. The `foo` function does not handle these values gracefully, leading to potential errors or unexpected results.

## Bug

The `bug.js` file contains a function `foo` that takes two arguments, `a` and `b`. The function checks if either `a` or `b` is null. If either is null, the function returns without performing any further actions. However, this approach may not be sufficient in all cases. If the function contains operations that could throw errors when null or undefined values are used (such as accessing properties of a null object), the function may behave unexpectedly or throw an error. 

## Solution

The `bugSolution.js` file provides a more robust solution. It uses strict equality to check for null and undefined values explicitly, and it handles those cases gracefully.  If either argument is null or undefined, the function returns a default value or performs an alternative action instead of exiting. This prevents errors and ensures that the function behaves consistently in all cases.