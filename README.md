# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and its dependency array. The provided `MyComponent` uses `setInterval` to update a counter, but the dependency array is empty (`[]`), causing the effect to run repeatedly, leading to an infinite loop.  The solution demonstrates the correct usage of the dependency array to resolve this.

## Bug

The `bug.js` file contains the buggy code. The `setInterval` function within the `useEffect` hook lacks the `count` state in its dependency array. This results in the effect constantly re-running, creating an infinite loop and potentially crashing the application.

## Solution

The `bugSolution.js` file contains the corrected code. The `count` state is added to the dependency array, ensuring the effect runs only when `count` changes.  This prevents the infinite loop.

## How to reproduce

1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the count in the browser. (Buggy version will rapidly increment).
