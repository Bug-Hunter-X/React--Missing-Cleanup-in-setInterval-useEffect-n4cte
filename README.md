# React useEffect setInterval Cleanup Bug

This repository demonstrates a common bug in React applications involving the use of `setInterval` within the `useEffect` hook.  The bug stems from the failure to properly clean up the interval, resulting in memory leaks and potential performance issues.

## Bug Description
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks the essential cleanup function within the `useEffect` hook's return statement.  This means that the interval continues to run even after the component unmounts, leading to unnecessary resource consumption.

## Solution
The `bugSolution.js` file provides a corrected version of the component. The crucial change is the addition of a cleanup function to the `useEffect` hook's return statement. This function uses `clearInterval` to stop the interval when the component unmounts, preventing memory leaks.

## How to Reproduce
1. Clone the repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server. Observe the console after unmounting the component.