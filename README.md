# React useEffect Dependency Array Issue

This repository demonstrates a common issue in React applications involving the `useEffect` hook and its dependency array.  Forgetting to include state variables in the dependency array can lead to unexpected behavior, infinite loops, and incorrect updates.

The `bug.js` file contains the code with the error, while `bugSolution.js` provides the corrected version.

## Problem

The initial `useEffect` hook in `bug.js` is missing `count` in its dependency array. This means the effect runs after every render, regardless of whether `count` has changed.  This can lead to performance problems and unexpected behavior.

## Solution

The corrected code in `bugSolution.js` includes `count` in the dependency array, ensuring that the effect only runs when the value of `count` changes. This is crucial for preventing infinite loops and ensuring the effect updates properly.