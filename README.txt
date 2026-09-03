FOOT REHAB TRACKER

This is a standalone mobile web app/PWA.

Included:
- 2–3 sessions/day tracking, with a minimum of 1
- 8 exercises in the order from your PT sheet
- Per-exercise timers
- Optional ice/frozen-water-bottle final step
- Pain before/after
- Session notes
- Same-day session count
- History & progress summary
- Local persistence on the device
- Export data backup (JSON)

DATA STORAGE
Your rehab data is stored in the browser's localStorage on the device/browser where you use the app. It is not sent to a server by this app. The GitHub Pages site hosts the app files; it does not receive your session entries.

Important: localStorage is tied to the browser/site on that device. Clearing website data, using a different browser/device, or some privacy/storage settings can remove or isolate the data. This version does not automatically sync between your iPhone and computer or back up your history to the cloud.

iPHONE HOME SCREEN
1. Host these files on an HTTPS web host (GitHub Pages is a simple free option).
2. Open the site in Safari on your iPhone.
3. Share -> Add to Home Screen -> enable Open as Web App if offered.

If you already deployed an earlier version to GitHub Pages, replace/commit the updated index.html, manifest.webmanifest, and sw.js files from this package. The app's local data key remains "footRehab", so existing data from the same deployed site/browser should remain available after the update.

This tracker does not replace your PT's instructions.


BACKUP
Use the Export data button about once a week or whenever you remember. It downloads a JSON backup of your current history. Keep the file somewhere safe. The app does not currently include an import/restore button; if you ever need to restore data, the backup can be used to rebuild the local data.
