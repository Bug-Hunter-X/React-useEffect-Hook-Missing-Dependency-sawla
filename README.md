# React useEffect Hook Missing Dependency

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example showcases a component where the `useEffect` hook is missing a crucial dependency, leading to unexpected behavior.  The solution shows how to properly add the dependency to resolve the issue. 

## Bug
The `bug.js` file contains a React component that increments a counter.  The `useEffect` hook attempts to log the count to the console, but it does so after *every* render, not just when the count changes, because `count` is missing from the dependency array. This can lead to performance issues and even infinite loops in more complex scenarios.

## Solution
The `bugSolution.js` file shows the corrected component. By including `count` in the dependency array of `useEffect`, the effect only runs when `count` changes, resulting in the expected behavior.  This ensures optimal performance and prevents unnecessary re-renders.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.