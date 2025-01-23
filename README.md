# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6. The catch-all route unintentionally intercepts navigation to other defined routes, leading to unexpected behavior. 

## Problem Description

The problem arises from the order of routes defined in the `Routes` component.  A catch-all route (`/*`) should typically be placed last to ensure it only catches routes that don't match any other specific routes.  However, placing it earlier causes it to always match, regardless of the path.

## Solution
The solution is simple; rearrange the order of routes within the `Routes` component, ensuring the catch-all route is placed last. 

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/about` always displays the 404 page. 

## How to fix

1. Refer to the `AppSolution.js` file for the corrected code.
2. Observe that the navigation works as expected after moving the catch-all route to the end.