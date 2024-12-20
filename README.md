# React useEffect Infinite Loop with useState Object
This repo demonstrates a common error in React's useEffect hook: using a non-primitive value (object) in the dependency array, which can lead to an infinite loop of re-renders.

## Bug Description
The `MyComponent` uses `useState` to manage a count. The `useEffect` hook logs the count to the console. However, there is an error where the count is treated as an object instead of a primitive, causing an infinite re-render.

## Solution
The solution involves updating the count to ensure that the value stored in `useState` is always a primitive and properly included in the dependency array.