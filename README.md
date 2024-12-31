# React Native useRef Hook and Asynchronous Operations

This repository demonstrates a common error that occurs when using the `useRef` hook in React Native with asynchronous operations: attempting to update a reference after the component has unmounted.

## Problem
The `bug.js` file showcases an example of this issue.  An asynchronous function is called within a `useEffect` hook, updating a ref. If the component is unmounted before the asynchronous operation completes, it will lead to an error because `myRef.current` might be null.