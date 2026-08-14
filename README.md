# Smart Attendance Monitoring System

A responsive smart attendance application with browser-based face enrollment and recognition, student/class management, analytics and CSV reporting.

## Current live features
- Dashboard with attendance statistics
- Student and class management
- Face enrollment using webcam
- Browser-based face detection + face descriptor matching with face-api.js
- Face-based attendance marking with duplicate-day protection
- Daily attendance register
- Seven-day attendance visualization
- CSV report export
- Responsive desktop/mobile UI
- Local browser storage for the GitHub Pages demo

## Important architecture note
The GitHub Pages version is a client-side demo: face templates and attendance data are stored in the browser's localStorage. Camera frames are processed in the browser and are not uploaded by this version.

A production backend is also included in `server/` with Express, MongoDB, JWT authentication and student/attendance APIs. `render.yaml` provides a deployment blueprint. To make the backend live, a MongoDB connection string and a backend hosting service must be configured; those credentials cannot be safely invented or embedded in a public repository.

## Run locally
Open `index.html` through a local HTTPS/static server for camera access, or use GitHub Pages. For the API, run `cd server`, set the environment variables from `.env.example`, then run `npm install` and `npm start`.

## GitHub Pages
The repository contains `.github/workflows/static.yml` for automatic deployment to GitHub Pages.
