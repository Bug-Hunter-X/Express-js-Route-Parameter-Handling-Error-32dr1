# Express.js Route Parameter Handling Bug

This repository demonstrates a common error in Express.js applications related to handling route parameters. Specifically, it showcases the issue of improper error handling when a route parameter is not in the expected format (e.g., a non-numeric ID when an integer is expected).

## Bug Description

The `bug.js` file contains an Express.js route that fetches a user based on their ID.  However, it fails to properly handle cases where the `userId` parameter is not a valid number. This can lead to unexpected behavior, including crashes or incorrect data being returned.

## Solution

The `bugSolution.js` file provides a corrected version of the code. The solution includes explicit checks to ensure the `userId` is a number before attempting to use it in the `users` array lookup.  It also uses a more robust error-handling mechanism to return a 404 status code when the user is not found.