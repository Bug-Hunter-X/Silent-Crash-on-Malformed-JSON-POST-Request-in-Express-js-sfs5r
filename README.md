# Silent Crash on Malformed JSON POST Request in Express.js

This repository demonstrates a common error in Express.js applications where the application silently crashes when it receives a malformed JSON payload in a POST request.  The issue stems from the lack of proper error handling when accessing properties of the request body (`req.body`).

The `bug.js` file showcases the problematic code.  The `bugSolution.js` file provides a corrected version with robust error handling.

## Problem

The original code lacks checks to ensure that `req.body` contains the expected data.  If the request body is missing or contains unexpected data, accessing properties like `user.name` will throw an error, causing the application to crash without informative error messages.

## Solution

The solution involves adding error handling to validate the request body before accessing its properties. This helps prevent crashes and provide more informative responses to the client.