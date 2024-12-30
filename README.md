# Node.js Server Port Already in Use
This repository demonstrates a common error in Node.js where a server fails to start because the specified port is already in use.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a robust solution.

## Problem
Attempting to start a Node.js HTTP server on a port that's already occupied by another process results in an error.  This usually occurs when you're running multiple Node.js applications simultaneously, or if another service is using the same port.

## Solution
The solution involves using the `listen` method's callback function to handle potential port binding errors gracefully. The callback function receives an error object if the port is unavailable and allows for error handling and alternative actions.