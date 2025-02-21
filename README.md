# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by an incorrectly specified dependency array.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook that attempts to log the current count to the console.  However, because the dependency array is empty (`[]`), the effect runs after every render, causing an infinite loop and potentially crashing the application. 

## The Solution

The `bugSolution.js` file provides a corrected version. By including `count` in the dependency array, the effect only runs when the value of `count` changes, resolving the infinite loop.