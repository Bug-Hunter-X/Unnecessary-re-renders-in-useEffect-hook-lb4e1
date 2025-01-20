# Unnecessary Re-renders in React useEffect Hook

This example demonstrates a common issue where the `useEffect` hook in React causes unnecessary re-renders and console logs.  The effect runs after every render, even when the dependencies array is not explicitly defined, which can impact performance.

## Bug Description:
The `useEffect` hook in `MyComponent` is executed after every render. This is inefficient because the `console.log` statement and the effect logic itself are performed repeatedly even though the component's state update doesn't affect them. 

## Solution:
To correct this issue, provide an empty dependency array `[]` to `useEffect` to ensure it runs only once after the initial render.  This optimization avoids unnecessary executions.