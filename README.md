# React useEffect Hook Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook: forgetting to include a cleanup function in the effect's return statement. This can lead to memory leaks and unexpected behavior.

## The Problem

The `bug.js` file contains a component with an `useEffect` hook that logs a message to the console when the component mounts. However, it's missing the crucial `return` statement, preventing the cleanup function from executing when the component unmounts.

## The Solution

The `bugSolution.js` file provides the corrected component with a cleanup function in the `useEffect` hook. This ensures that any resources or subscriptions created within the effect are properly cleaned up when the component unmounts, preventing memory leaks.