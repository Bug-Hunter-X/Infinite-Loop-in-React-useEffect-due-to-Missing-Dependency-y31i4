# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by omitting a necessary dependency from the `useEffect` hook's dependency array, leading to an infinite loop.

## Bug Description
The `MyComponent` component uses `useState` to manage a count.  The `useEffect` hook logs the count to the console. However, because `count` is missing from the dependency array, the effect runs after every render, causing the `count` to update infinitely.

## Solution
The solution is to include `count` in the dependency array of `useEffect` so the effect runs only when `count` changes.