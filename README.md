# Express.js - Empty or Invalid JSON Request Body Parsing Issue

This repository demonstrates a common issue in Express.js applications where parsing the JSON request body fails when the body is empty or contains invalid JSON data. The issue arises because the `express.json()` middleware expects a properly formatted JSON payload.  If the request body is empty or malformed, parsing will fail silently, leading to unexpected behavior or errors.

## Bug Description

The provided `bug.js` file contains a simple Express.js server that attempts to parse the JSON request body using `express.json()`. When a POST request is sent to `/data` with an empty body or a body containing invalid JSON, the server does not handle the error correctly, potentially leading to unexpected behavior in the application.

## Bug Solution

The `bugSolution.js` file provides a corrected version of the server. It uses a `try...catch` block to handle potential parsing errors and responds with an appropriate error message when invalid JSON is received. This makes the application more robust and easier to debug.