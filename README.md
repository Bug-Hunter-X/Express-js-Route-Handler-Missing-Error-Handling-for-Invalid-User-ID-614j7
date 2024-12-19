# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid user IDs. The provided code attempts to parse the user ID as an integer without checking if the ID is valid. If the ID is not a valid integer, the code will throw an error, causing the server to crash.

## Bug

The `bug.js` file contains the buggy code.  The route handler for `/users/:id` attempts to parse the `id` parameter as an integer and use it to find a user. If the ID is not an integer, the `parseInt` function returns `NaN`, leading to an error when comparing to user IDs.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  This version adds error handling to check if the ID is a valid integer. If it is not, a 400 Bad Request response is returned.

This example highlights the importance of robust error handling in Express.js applications. Always validate user input to prevent unexpected errors and crashes.