# Foot Rehab Tracker

**A personal plantar fasciitis exercise tracker — made with help from ChatGPT.**

This is a small, mobile-first web app created to make it easier to follow a prescribed foot-rehabilitation routine, record completed exercises, and notice patterns in pain and consistency.

It is designed primarily for personal use on a phone.

---

## What the app does

The tracker organizes rehabilitation by **calendar day** and supports up to three sessions per day.

### Daily goal

- **Minimum goal:** 1 session per day
- **Physical therapy target:** 2–3 sessions per day
- The app shows your progress toward 3 sessions.
- Once 3 sessions are complete, the app treats the day's PT target as reached.

### Exercises

The routine currently contains:

1. Gastrocnemius Stretch on Wall — 3 × 30 seconds
2. Soleus Stretch on Wall — 3 × 30 seconds
3. Arch Lifting — 2 × 2 minutes
4. Towel Scrunches — 2 × 2 minutes
5. Toe Yoga — Alternating Great and Lesser Toe Extension — 2 × 2 minutes
6. Toe Spreading — 2 × 2 minutes
7. Seated Plantar Fascia Stretch — 3 × 30 seconds
8. Seated Plantar Fascia Mobilization with Small Ball — 2 × 2 minutes

Each timed exercise has an in-app timer. Completing a timer marks that exercise as completed, but exercises can also be marked complete manually where applicable.

### Session tracking

Each completed session can record:

- Exercises completed
- Pain before the session
- Pain after the session
- Whether ice or a frozen water bottle was used
- Session notes

**Incomplete sessions can be saved.** A session does not have to be 8/8 exercises to be recorded. For example, a session with 3/8 exercises completed is saved as a 3/8 session and the next session starts fresh.

### History & Progress

The History & Progress area provides:

- Recent session count
- Average pain before sessions
- Average pain after sessions
- Recent sessions
- Exercise completion for each session (for example, **8/8 exercises completed**)
- Session notes

### Data export

The **Export Data** button creates a JSON backup of the tracker data.

It is a good idea to export your data periodically — approximately once a week is a reasonable habit for a short-term rehabilitation plan.

---

## Where your data is stored

This app uses **browser localStorage** to save tracker data.

That means:

**Your session data is stored locally on the device/browser where you use the app.**

It is **not uploaded to GitHub Pages** and there is no cloud database behind this tracker.

GitHub Pages hosts the app's HTML, CSS, JavaScript, and icon files. It does not receive your exercise sessions, pain scores, or notes simply because you use the app.

### What local storage means

Your data should remain available when you:

- Close the app
- Reopen the app
- Reload the page
- Use the Home Screen version of the app

However, local storage is not the same thing as cloud backup.

Your data could be lost if you:

- Clear the website's stored data
- Reset or erase the device
- Change devices without transferring/backing up the data
- Use a different browser or browser storage environment
- Encounter an unusual browser/storage cleanup event

For that reason, **Export Data is the backup mechanism for this version of the app.**

### Important distinction: cache vs. data

The app's cached website files and your saved rehabilitation data are different things.

Clearing a cached copy of the website should not normally erase localStorage data. However, deleting the site's stored data can erase the tracker history.

**If you have important history, export it before deliberately clearing website/site data.**

---

## Backup recommendations

For a roughly two-month rehabilitation period:

1. Use the tracker normally.
2. Export your data about once a week.
3. Keep the JSON backup somewhere safe, such as iCloud Drive or another file location.
4. If you ever need to troubleshoot the app, make a fresh export first.

The exported file contains the app's saved data in JSON format and is intended as a backup/archive.

### Current limitation

The app currently supports **export but not import/restore from a JSON backup**.

That means an exported file is a backup record, but there is not yet an in-app button for automatically restoring it to a new device.

---

## Installing on an iPhone

The app is hosted as a static website on GitHub Pages.

A Home Screen installation can open it in its own app-like window.

If the Home Screen icon ever appears outdated after an icon update, iOS may be displaying a cached Home Screen icon. Removing the old Home Screen shortcut and adding the current version again can refresh it.

---

## Interface notes

The Home Screen icon is supplied as a full-bleed image so that iOS can apply its own rounded-square mask without creating an extra white border around the artwork.

---

## Icon note

The Home Screen icon uses an opaque full-bleed background so iOS can apply its own rounded-square mask without creating a black or white border.

---

## Technical notes

This is intentionally a simple application.

### Hosting

- Static files hosted with GitHub Pages
- No server-side application
- No external database
- No account/login system
- No third-party JavaScript libraries required

### Storage

- Browser `localStorage`
- Storage key: `footRehab`
- Data is stored as JSON

### Files

- `index.html` — the application
- `manifest.webmanifest` — web app metadata and icons
- `foot-icon-512.png` — large app icon
- `foot-icon-192.png` — web app icon
- `foot-icon-180.png` — iOS Home Screen icon
- `foot-icon-152.png` — additional icon size
- `README.txt` — this documentation

### Updating the app

To update the app:

1. Replace the relevant files in the GitHub repository.
2. Commit the changes.
3. Wait for GitHub Pages to deploy.
4. Open the current site and verify the update.
5. If the browser is displaying an older version, a cache-busting query string such as `?v=2` can force a fresh page request.

The application does **not** use a service worker in this version. This was intentional to avoid persistent service-worker caching interfering with updates.

---

## Privacy

This tracker was built as a personal tool.

The app does not have a login system or cloud account, and the tracker data is intended to remain in local browser storage.

Because this is a personal rehabilitation tracker, treat exported JSON backups as private files. They may contain pain scores and personal notes.

---

## Development notes

This project was built iteratively with assistance from ChatGPT.

The design and functionality were developed around a real physical-therapy exercise routine and refined through testing on an iPhone.

ChatGPT assisted with:

- App structure and JavaScript
- Mobile-first UI
- Exercise timers
- Local data storage
- Session/history logic
- Data export
- PWA/web-app metadata
- Home Screen icon setup
- Debugging and iterative fixes

The app is intentionally small and self-contained so it can remain easy to understand, maintain, and modify.

---

## Future ideas

Possible improvements if this becomes a longer-term tool include:

- Import/restore from JSON backups
- Automatic cloud backup/sync
- More detailed progress charts
- Weekly adherence summaries
- Exercise-specific notes
- Editing or deleting individual historical sessions
- Customizable exercise routines
- More robust data validation
- Better migration support when the app's data structure changes

For the current short-term use case, localStorage plus periodic JSON exports keeps the system simple and avoids unnecessary infrastructure.

---

**Foot Rehab Tracker — made with help from ChatGPT.**
