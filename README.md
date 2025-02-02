# Unexpected Re-renders in React useEffect Hook

This repository demonstrates a common issue with the React `useEffect` hook: unexpected re-renders due to missing dependencies in the dependency array.

## Bug Description
The `useEffect` hook in `bug.js` is designed to log the current count to the console. However, because it lacks the `count` variable in its dependency array, it runs after *every* render, not just when the count changes. This leads to unnecessary logging and potential performance problems, especially with more complex components.

## Bug Solution
The `bugSolution.js` file provides a corrected version. By including `count` in the dependency array, the `useEffect` now only runs when the value of `count` actually changes, fixing the unnecessary re-renders.