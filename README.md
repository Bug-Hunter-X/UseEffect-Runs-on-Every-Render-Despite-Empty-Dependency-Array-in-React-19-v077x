# React 19 useEffect Bug: Unexpected Re-renders with Empty Dependency Array

This repository demonstrates a subtle bug in React 19 where a `useEffect` hook with an empty dependency array still runs on every render.  This unexpected behavior can lead to performance issues and incorrect application state.

## Problem Description

The `useEffect` hook is designed to run after every render. However, when provided with an empty dependency array (`[]`), it's expected to only run once, after the initial render.  In this example, we've encountered a situation where this behavior is not consistent in React 19.

## Reproduction

The `bug.js` file contains a simple counter component. Observe the console logs to see that the effect runs more than once, despite having an empty dependency array.

## Solution

The `bugSolution.js` demonstrates a solution that ensures the useEffect runs only once.  The fix may involve analyzing the component's dependencies more closely or refactoring the component itself.

## Technologies Used

- React 19
- JavaScript