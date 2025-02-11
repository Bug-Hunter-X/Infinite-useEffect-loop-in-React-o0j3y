# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite useEffect loop.  The component `MyComponent` utilizes `useEffect` without a dependency array, leading to an infinite render cycle.  This example highlights the problem and provides a solution.

## Problem

The `useEffect` hook in the `bug.js` file is used to log the count to the console after each render. However, it's missing a dependency array.  This means the effect is triggered after every render, including those caused by the effect itself, creating an infinite loop.

## Solution

The `bugSolution.js` file provides a corrected version of the component. The dependency array `[count]` ensures that the effect only runs when the `count` value changes. This prevents the infinite loop and fixes the performance issue.