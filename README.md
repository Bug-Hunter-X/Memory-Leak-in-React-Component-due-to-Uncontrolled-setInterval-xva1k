# React setInterval Cleanup Issue
This repository demonstrates a common mistake in React development: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Problem
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, causing the interval to continue running even after the component is no longer rendered. This results in a memory leak and potential performance issues. 

## Solution
The solution involves using the return function of `useEffect` to clear the interval when the component is unmounted, preventing the memory leak.