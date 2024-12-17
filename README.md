# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous routes.  The `bug.js` file shows an example of an asynchronous route that doesn't properly handle errors.  The `bugSolution.js` provides a corrected version with robust error handling.

## Problem

Asynchronous operations in Express.js routes often involve promises.  If an error occurs within the promise's `.then()` block, or if the promise is rejected, and no `.catch()` block is present, the application might crash or behave unpredictably.

## Solution

Always include a `.catch()` block within your asynchronous routes to handle potential errors gracefully.  Proper error handling improves the robustness of your application and prevents unexpected failures.