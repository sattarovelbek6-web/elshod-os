# Elshod OS — PWA v0.2

Personal, Russian-language productivity dashboard designed for iPhone. The app is a lightweight static site with no backend or external dependencies.

## Features

- Dashboard with daily task progress and priorities
- Tasks with priority, category, deadline, edit, complete, and delete
- IELTS practice tracker and vocabulary list
- University schedule and assignment deadlines
- Fitness checklist, workout history, weight log, and habits
- Finance tracker with monthly budget, income, and expenses
- Daily journal
- JSON export and import for backups
- Local browser storage and offline app-shell caching

## Publish with GitHub Pages

1. Put `index.html`, `sw.js`, and this `README.md` in the repository’s publishing folder (usually the repository root).
2. On GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the branch containing the files and the folder (`/(root)` if they are in the root), then save.
5. Wait for GitHub Pages to publish. Open the HTTPS address shown in Pages settings.

No `manifest.webmanifest` upload is required. The manifest is embedded in `index.html`; iOS Safari’s Home Screen installation also uses the Apple web-app metadata.

## Install on iPhone 15 Pro

1. Open the published HTTPS address in **Safari**.
2. Tap **Share**.
3. Tap **Add to Home Screen**, then **Add**.
4. Launch Elshod OS using its Home Screen icon.

Open the site once while online so the service worker can install and cache the app shell. Offline behavior is available after that successful load.

## Data and backups

Data is stored in the browser’s local storage on this device. It is not synchronized or encrypted and can be removed when browser data is cleared. Use **Настройки → Экспортировать JSON** to save a backup. Importing a backup replaces the current app data after confirmation.

For an update, publish the new files and reload the app online. The service worker updates its cache to version `elshod-os-v02`.