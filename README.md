# React Router Dom v6 Catch All Route Issue

This repository demonstrates a bug in React Router Dom v6 where the catch-all route (`/*`) always triggers, regardless of whether a more specific route matches first. This prevents other routes from working correctly.

## Bug Description
The issue is demonstrated in `App.js`.  The catch all route `/*` will always be rendered, even if a path like `/about` is specified.  This means the `/about` route and others will never be rendered.

## Solution
The solution provided in `AppSolution.js` uses a more specific catch-all route at the end of the route array in `Routes`. By moving the catch-all route to the end, the other routes can be rendered as expected.