# Node.js Server Hanging During Long Requests

This repository demonstrates a common issue in Node.js where the server hangs or becomes unresponsive during long-running requests.  The example uses a simple HTTP server that simulates a long-running task, causing the server to block and fail to respond to other requests.

## Problem

Node.js is single-threaded. When a request triggers a long-running operation, it blocks the event loop preventing other requests from being handled. This leads to the server appearing unresponsive or slow.

## Solution

The solution involves using asynchronous programming techniques such as promises or async/await to prevent blocking the event loop.  The provided solution demonstrates the use of `setTimeout` to simulate asynchronous task handling.  In a real-world scenario, you would use asynchronous I/O operations, database calls, etc., that are inherently non-blocking.