# Firebase Data Persistence Issue After Inactivity

This repository demonstrates a peculiar issue encountered with Firebase Realtime Database data persistence.  Writes to the database appear successful initially, but fail after a period of inactivity or when the device restarts. The problem doesn't seem related to data formatting, authentication, or database rules. 

The `bug.js` file contains the code exhibiting this behavior.  The `bugSolution.js` file offers a solution to address the problem, ensuring data persistence across sessions.

## Reproduction

1. Clone this repository.
2. Ensure you have Node.js and npm installed.
3. Install Firebase: `npm install firebase`
4. Configure your Firebase project credentials in a `firebase.json` file.
5. Run `node bug.js` to reproduce the issue.
6. Run `node bugSolution.js` to observe the solution.

## Solution

The solution involves explicitly enabling data persistence in the Firebase configuration, ensuring that data is persistently stored and synchronized even after the application closes or the device restarts.