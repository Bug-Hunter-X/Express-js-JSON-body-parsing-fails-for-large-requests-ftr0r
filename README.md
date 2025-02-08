# Express.js JSON Body Parsing Issue
This repository demonstrates a common issue in Express.js applications where parsing large JSON request bodies fails due to exceeding the default body-parser limit.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution.

## Problem
The Express.js application uses `express.json()` to parse incoming JSON requests. However, when a large JSON payload is sent, the application might fail to parse it correctly, often resulting in an empty request body (`req.body`). This is because `express.json()` has a default limit on the size of the request body it can handle.

## Solution
The solution involves setting a larger limit for the body-parser using `express.json({ limit: '10mb' })`. This allows the application to handle larger JSON payloads.
