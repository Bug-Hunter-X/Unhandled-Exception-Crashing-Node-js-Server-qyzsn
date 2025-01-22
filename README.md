# Unhandled Exception Crashing Node.js Server

This repository demonstrates a common error in Node.js applications:  unhandled exceptions causing server crashes.  The `bug.js` file shows a server that throws an error without proper handling.  `bugSolution.js` provides a solution using error handling best practices.

## Bug

The server crashes when the `/error` endpoint is accessed because the thrown `Error` isn't caught.  This is a crucial issue for production environments, leading to downtime.

## Solution

The solution employs a `try...catch` block to gracefully handle the error and prevent a server crash.  It also logs the error for debugging and sends an appropriate response to the client.