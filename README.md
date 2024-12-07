# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to a missing dependency in the useEffect's dependency array.

## Bug Description

The `MyComponent` function uses the `useEffect` hook to log the current count to the console after every render. However, the `count` state variable is missing from the dependency array, causing the effect to run repeatedly, resulting in an infinite loop and excessive logging.

## Solution

The solution involves adding `count` to the dependency array of `useEffect`. This ensures that the effect only runs when the `count` state changes, thus resolving the infinite loop.