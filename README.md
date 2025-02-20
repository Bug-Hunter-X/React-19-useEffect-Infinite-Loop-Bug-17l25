# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common error in React 19 involving the `useEffect` hook, specifically an infinite loop caused by incorrect dependency management.

## Bug Description
The bug is in `bug.js`. The `useEffect` hook attempts to log the count after every render without listing `count` in the dependency array. This causes an infinite loop because the effect runs continuously, updating the count, triggering a re-render and so on. 

## Solution
The solution (`bugSolution.js`) fixes the issue by adding `count` to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` variable changes.