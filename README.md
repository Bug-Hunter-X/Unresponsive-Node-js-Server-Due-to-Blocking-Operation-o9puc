# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can block the event loop, making the server unresponsive. The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Bug

The `bug.js` file uses a `while` loop to simulate a long-running task. This blocks the event loop, preventing other requests from being processed and causing the server to become unresponsive.  This is a classic example of how blocking the event loop can cause problems in a Node.js application.

## Solution

The `bugSolution.js` file addresses the issue by using asynchronous operations to avoid blocking the event loop.  The solution demonstrates the use of timers or other non-blocking operations to handle long-running tasks.  This prevents the event loop from becoming blocked and allows the server to remain responsive.