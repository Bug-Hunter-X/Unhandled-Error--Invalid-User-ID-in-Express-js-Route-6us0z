# Express.js Unhandled Error: Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer but fails to gracefully handle cases where the `id` is not a valid integer.

## Bug

The `bug.js` file contains the flawed route handler.  If you try to access a user with an invalid ID (e.g., a string or a non-numeric value), the server will either crash or return an unexpected error.

## Solution

The `bugSolution.js` file shows the corrected code.  It includes error handling to check if the `id` parameter is a valid integer and returns a 400 Bad Request response if it's not.