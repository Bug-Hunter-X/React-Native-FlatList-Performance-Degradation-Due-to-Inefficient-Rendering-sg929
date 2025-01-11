# React Native FlatList Performance Issue

This repository demonstrates a common performance problem in React Native applications using `FlatList` or `SectionList` with complex data structures. The issue is characterized by slow UI updates and poor user experience due to excessive re-renders triggered by minor data modifications.

The `bug.js` file showcases the problem. The `bugSolution.js` provides an optimized solution.

## Problem

The initial implementation of the `FlatList` inefficiently handles data updates, leading to unnecessary re-renders of the entire list, or large portions of it.  This is particularly noticeable with large datasets or deeply nested components.

## Solution

The optimized version utilizes techniques like `useMemo` and `React.memo` to prevent unnecessary re-renders, as well as potentially using `shouldComponentUpdate` for more granular control.  Data structures are examined and simplified where possible to reduce the amount of work necessary.

## How to Run

1. Clone the repository.
2. `npm install`
3. `npx react-native run-android` or `npx react-native run-ios`