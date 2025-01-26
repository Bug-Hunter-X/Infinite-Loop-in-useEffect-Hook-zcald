# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications where an infinite loop occurs within a `useEffect` hook.  The issue stems from incorrectly managing the dependencies within the hook's array.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` attempts to update the `count` state variable on every render cycle. Because `count` is not included as a dependency, the effect runs indefinitely, causing the component to re-render constantly and potentially crashing the application.

## Solution

The corrected code in `bugSolution.js` addresses this by adding `count` to the dependency array.  Now, the `useEffect` hook only runs when the value of `count` changes, breaking the infinite loop.  This ensures the component renders as expected and does not cause unexpected behavior.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.
5. Observe the buggy behavior in the initial `bug.js` and then observe the corrected behavior in `bugSolution.js`