# React Native useEffect Hook with Function Dependency Issue

This repository demonstrates a common but subtle bug in React Native involving the `useEffect` hook and function dependencies.  The issue arises when a function is included in the dependency array of `useEffect`, and that function's internal state changes without a corresponding change in its reference. This leads to the `useEffect` callback not re-running, even when its logic depends on the new state.

The bug is explained in detail in the `bug.js` file, along with a solution in `bugSolution.js`. The solution explains how to correctly handle situations where a function's behavior changes without changing its reference, ensuring `useEffect` re-renders as intended.