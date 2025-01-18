# React Router Dom: Catch-all Route Conflict

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router Dom with nested routes. The catch-all route unintentionally overrides more specific routes, resulting in unexpected routing behavior.

## Problem Description

The `/*` catch-all route, intended to handle 404 errors, matches all routes, even those that are more specific. This can lead to the catch-all route always being rendered, preventing nested routes from working correctly. The example shows how a nested route defined below the catch-all is never matched.

## Solution

The solution involves re-ordering routes, placing the catch-all route last. This ensures more specific routes are matched before the catch-all route handles unmatched paths.
