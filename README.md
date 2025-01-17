# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers where a long-running operation in the request handler can cause the server to hang or become unresponsive to other requests.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

Node.js is single-threaded.  A long-running synchronous operation in the request handler blocks the event loop, preventing the server from processing other requests. This leads to unresponsiveness and a poor user experience.

## Solution

The solution involves using asynchronous operations (like promises or async/await) or offloading the long-running task to a separate thread using worker threads to avoid blocking the main thread.