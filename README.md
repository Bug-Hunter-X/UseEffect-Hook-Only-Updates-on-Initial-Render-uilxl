# React useEffect Hook Only Updates on Initial Render

This repository demonstrates a common issue with the React `useEffect` hook where the dependency array is incorrectly specified, leading to unexpected behavior. The component updates the document title only when the count is initially 0, and it fails to update when the count changes.

## Problem
The `useEffect` hook is designed to perform side effects based on changes in dependencies. The issue in `bug.js` is that the effect function only runs when `count` is 0. This is because the condition `if (count === 0)` prevents the title update from happening if the count is anything other than 0.

## Solution
The `bugSolution.js` file fixes this by removing the unnecessary `if` condition. Now, the title updates correctly with every change in the `count` value.

## How to reproduce:
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the page title in your browser as you click the increment button.