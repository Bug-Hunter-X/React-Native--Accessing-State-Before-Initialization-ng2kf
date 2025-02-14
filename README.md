# React Native: Accessing State Before Initialization

This repository demonstrates a common error in React Native: accessing a state variable before it has been initialized. This often happens when using the `useState` hook with asynchronous operations. The `bug.js` file showcases the issue, while `bugSolution.js` provides a corrected version.

## Problem
In functional components, the state variable initialized with `useState` might not be immediately available.  If you attempt to access it before the component mounts completely and the state has been populated, you will encounter `undefined` values, leading to potential crashes or unexpected behavior. 

## Solution
The solution involves using the useEffect hook to ensure the asynchronous operation and state access happen after the component has mounted and the state has been initialized by the useState hook.