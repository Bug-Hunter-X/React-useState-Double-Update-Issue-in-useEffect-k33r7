# React useState Double Update Issue in useEffect

This repository demonstrates a common issue in React applications involving the `useState` hook and the `useEffect` hook. Specifically, it shows a race condition that can occur when updating state multiple times within a single render cycle. This is especially prominent when the state update depends on the previous state.

## Bug Description

The bug is related to multiple calls to `setCount` in a single `handleClick` function, resulting in unexpected behavior that the counter may not always increment by the correct amount.  The `useEffect` hook amplifies the issue because it runs after every render.

## Solution

The solution provided utilizes the functional update syntax of `setCount` to avoid the race condition. By ensuring only one state update occurs, we guarantee the counter increments correctly every time the button is clicked. Refer to `bugSolution.js` for the corrected implementation.