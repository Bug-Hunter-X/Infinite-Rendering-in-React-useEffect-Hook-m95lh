# Infinite Rendering in React useEffect Hook

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.

## Bug Description

The `MyComponent` component renders infinitely because the `useEffect` hook lacks a dependency array.  This causes the effect to run on every render, leading to an infinite loop.

## Bug Solution

The solution involves adding a dependency array to the `useEffect` hook.  The dependency array specifies which values the effect should depend on.  If none of these values change, the effect will not run again.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console log, showing the component rendering repeatedly.

## How to fix

1. Open `bugSolution.js` to see the corrected code.
2. The solution adds `[count]` as a dependency array to the `useEffect` hook. The effect now only runs when the value of `count` changes. 

