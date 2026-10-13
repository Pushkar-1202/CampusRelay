# CampusRelay

**A living, evidence-backed timeline for student opportunities.**

CampusRelay is a browser-based prototype for tracking hackathons, competitions, and workshops as their details change. It brings participation stages, dates, source references, and change history into one view.

## Try it

Open the [private live demo](https://campusrelay-living-timeline.abloomsage128.chatgpt.site), select **View demo flow**, or import a communication from the dashboard.

The seeded records are explicitly labeled as sample or simulated data. To test your own message, paste its text, inspect the proposed event match and extracted facts, then approve or dismiss it in the review queue.

## Features

- Unified living timeline with event details and milestones
- Local text extraction for event names, dates, registration IDs, and participation updates
- Ranked event matching using registration IDs, URLs, names, and organizer clues
- Review queue for uncertain matches and proposed changes
- Deadline history that preserves old and new values with source references
- Browser-local persistence via `localStorage`
- Responsive interface

## Run locally

This is a static HTML/CSS/JavaScript app. Serve the repository root with any static HTTP server, such as:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Current scope

Extraction uses deterministic browser-side rules rather than a connected AI model. There is no image upload, email forwarding, account sync, backend database, or multi-user sharing yet. Imported text is student-provided and is not independently authenticated. Browser storage is specific to the current device and browser profile.

## Architecture

`index.html` contains the app shell and import dialogs, `styles.css` defines the responsive interface, and `app.js` handles extraction, matching, review, versioned changes, and rendering.
