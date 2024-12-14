# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the route `/users/:id` attempts to parse the `id` parameter as an integer without checking for potential errors (e.g., non-numeric input). This can lead to unexpected crashes or incorrect behavior.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`.
4. Send a request to `/users/abc` (or any non-numeric ID).  You'll likely see an error.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  It includes explicit checks to ensure that the `userId` is a valid number before attempting to parse it.