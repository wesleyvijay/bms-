# VoltIQ — Website source code

A responsive two-cell battery management dashboard built with HTML, CSS, and plain JavaScript. This folder contains the latest website source, including the animated battery, analytics, cell monitoring, protection scenarios, event log, and energy-flow animations.

## Run it

1. Extract the ZIP folder.
2. Open `index.html` in your browser.

No installation, API keys, or build step is needed. Keep all files together.

For local development, open this folder in VS Code and use a local web server. If Python is installed, run this from the folder:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. Stop the server with Ctrl+C.

## File guide

- `index.html`: base page and script/style loading order.
- `style.css`: original layout, responsive styling, and first animation layer.
- `experience.css`: separate views, battery gauge, and additional charts.
- `polish.css`: energy-flow, battery, and transition animations.
- `app.js`: simulated readings, scenarios, charts, and event log.
- `experience.js`: Overview, Analytics, Cells, Protection, and Events views; charge slider and extra charts.
- `motion.js`: scroll reveals, chart inspection, animated readings, and cell details.
- `polish.js`: energy-flow diagram, explanatory notes, and additional motion.

Preserve the script order: app.js, experience.js, motion.js, polish.js. Later scripts extend functions and use state from earlier scripts.

## Notes

All battery readings are simulated. This version has no ESP32 connection, backend, database, or real hardware protection. Reloading starts a new demo session. Reduced-motion preferences are supported.

To host elsewhere, upload these files to a static web host with index.html at its root. The optional browser modelContext integration activates only in browsers that support it; the normal dashboard works without it.

## Publish on GitHub Pages

1. Create a public GitHub repository named `voltiq-bms`.
2. Upload the contents of this folder into the repository root on the `main` branch. `index.html` must be at the top level, not inside another folder. Do not upload the ZIP itself.
3. Open Settings > Pages.
4. Under Source, choose Deploy from a branch.
5. Select `main` and `/(root)`, then Save.
6. Wait for deployment. GitHub displays the live website link in Settings > Pages.

The address will normally be `https://YOUR-USERNAME.github.io/voltiq-bms/`. This is an example, not a live deployment URL.

Official guide: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
