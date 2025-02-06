# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js applications: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem
The original code contains a `for` loop that performs a computationally intensive task.  This synchronous operation blocks the event loop, preventing the server from responding to new requests until the loop completes.  This can lead to the server appearing to hang or become unresponsive.

## Solution
The solution involves refactoring the code to use asynchronous operations.  This allows the event loop to continue processing other events while the long-running task executes in the background, maintaining server responsiveness.