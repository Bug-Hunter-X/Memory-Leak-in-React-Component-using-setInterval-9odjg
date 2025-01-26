# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior when the component is unmounted.

## Problem

The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts. This causes the interval to continue running even after the component is removed from the DOM, resulting in a memory leak.

## Solution

The solution involves using the return value of `useEffect` to clear the interval before the component unmounts.  This ensures that the interval is stopped and prevents memory leaks.