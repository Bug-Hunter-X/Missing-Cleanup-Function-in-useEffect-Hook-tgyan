# Missing Cleanup Function in useEffect Hook

This repository demonstrates a common error in React 18+ related to missing cleanup functions within the useEffect hook.  Forgetting to return a cleanup function from a useEffect hook that uses timers (like setInterval or setTimeout) can lead to memory leaks. This example showcases the problematic code and its solution.

## Bug

The `bug.js` file contains code that uses `setInterval` without a cleanup function. In React 18+, this will trigger a warning, indicating a potential memory leak. 

## Solution

The `bugSolution.js` file provides the corrected version of the code.  It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, preventing the memory leak.