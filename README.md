# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to an incorrect dependency array, leading to performance issues and potential crashes.

## Bug Description
The provided code utilizes `useState` and `useEffect`.  An incorrect conditional statement within the `useEffect` callback causes the component to re-render infinitely after the count exceeds 5. The dependency array is missing, causing re-renders on every state change.

## Bug Reproduction
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console and the non-stop incrementing counter.

## Solution
The solution involves correctly specifying the dependency array to ensure that `useEffect` only runs when the `count` changes and prevent the infinite loop.