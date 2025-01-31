# Loose Comparison with null in JavaScript
This repository demonstrates an uncommon error in JavaScript related to loose comparison (==) with null and other falsy values.

The issue lies in the use of loose equality (==) instead of strict equality (===). Loose equality can lead to unexpected results when comparing null with undefined, 0, and other falsy values. 

## Bug Description
The `foo` function is intended to return 0 only when the input `x` is null. However, due to the loose comparison, it also returns 0 for undefined and 0, and NaN for NaN.  This behavior might be unexpected and lead to bugs in larger programs. 

## Solution
The solution replaces the loose equality operator (==) with the strict equality operator (===). Strict equality checks both the value and type of the operands, thus avoiding the unintended behavior. 

## How to reproduce
1. Clone this repository.
2. Open `bug.js` and run the code in a JavaScript environment (e.g., a browser's console or Node.js).
3. Observe the unexpected output for undefined, 0, and NaN. 
4. Open `bugSolution.js`, run the code. The code will show the correct output only for null.