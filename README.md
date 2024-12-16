# React useEffect Cleanup Function Issue

This repository demonstrates a common issue with React's `useEffect` hook: improper usage of the cleanup function, potentially causing memory leaks or unexpected side effects.

## Bug Description
The provided `MyComponent` uses `useEffect` to log the current count.  However, the cleanup function isn't correctly handling the scenarios where the component unmounts or updates rapidly leading to potential issues.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output as you click the button.  Note the order and timing of the logs in relation to component updates.

## Solution
The solution involves ensuring that the cleanup function is executed correctly in all scenarios, particularly when the component unmounts before the next render.