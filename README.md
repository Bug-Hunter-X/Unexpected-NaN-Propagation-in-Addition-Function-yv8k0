# Unexpected NaN Propagation in JavaScript Addition Function

This repository demonstrates a common pitfall in JavaScript related to handling null and NaN values in arithmetic operations.  The `foo` function aims to safely add two numbers, returning 0 if either input is null. However, it fails to correctly handle NaN (Not a Number) values, resulting in NaN propagation.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version that explicitly checks for NaN using `isNaN()` and handles it appropriately.

## How to reproduce

1. Clone the repository.
2. Open `bug.js` and run it in a JavaScript environment (e.g., Node.js or a browser's developer console).
3. Observe the unexpected NaN outputs.
4. Open `bugSolution.js` to see the corrected implementation.

## Bug and Solution Explanation

The bug stems from the loose comparison (`==`) and the nature of NaN in arithmetic.  The solution involves using `isNaN()` to explicitly identify and handle NaN cases, providing a more robust and predictable result.