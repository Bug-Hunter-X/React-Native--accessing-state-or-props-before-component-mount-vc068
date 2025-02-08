# React Native: Accessing State/Props Before Component Mount

This repository demonstrates a common error in React Native development: attempting to access component state or props before the component has fully mounted.  The `bug.js` file showcases the erroneous code, while `bugSolution.js` provides the corrected implementation.

## Problem

Accessing `this.state` or `this.props` too early in a component's lifecycle (e.g., within the constructor) can lead to unexpected behavior, often resulting in `undefined` values or runtime errors. React Native's lifecycle methods ensure data is available at the appropriate times.

## Solution

The solution involves leveraging the `componentDidMount` lifecycle method.  This method guarantees that the component has fully mounted and that `this.props` and `this.state` are initialized and accessible.