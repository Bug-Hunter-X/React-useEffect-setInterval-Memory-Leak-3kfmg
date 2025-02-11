# React useEffect setInterval Memory Leak
This example demonstrates a common mistake in React's `useEffect` hook when using `setInterval`. Forgetting to return a cleanup function from `useEffect` leads to memory leaks as the interval continues indefinitely after the component unmounts.

## Bug
The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook without a cleanup function. This results in an interval that continues even after the component is unmounted, causing a memory leak.

## Solution
The `bugSolution.js` file provides the corrected version.  The `useEffect` hook now returns a function that uses `clearInterval` to stop the interval before the component is unmounted, preventing memory leaks.
