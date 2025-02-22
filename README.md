# React Router v6 Nested Route Bug with Wildcard Route

This repository demonstrates a bug in React Router v6 where nested routes within a wildcard route (`users/*`) fail to render correctly. The wildcard route captures all paths, preventing nested route matching.

## Bug Description

The issue occurs when attempting to nest routes under a route that uses a wildcard path segment (`users/*`).  Instead of the nested route rendering, the wildcard route renders, even when the nested route's path is a more specific match.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/users/123`.

You will observe that the `<Users />` component renders instead of a potential nested route component that might handle `/users/123`  specifically.

## Solution

The provided solution demonstrates how to correctly structure routes in React Router v6 to avoid this issue. It involves restructuring the route configuration to prioritize specific nested routes before the wildcard route.

## Technologies Used

* React
* React Router v6