# Panthers Shot Tracker

Tap-to-log basketball shot tracker for practice. One tap is a make, a double tap is a miss. Tracks team and individual shooting by court zone, builds single- and multi-session reports, and exports PDF reports and CSV spreadsheets.

Sessions are saved on the phone that tracked them, and the app works with no signal once installed. Use **Sessions → Export backup** to save a copy, and **Import backup** on another phone to add those sessions there.

## Files

| File | What it is |
|---|---|
| `index.html` | The app |
| `sw.js` | Lets the app open with no signal |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` | Home Screen name and icon |

## Hosting

Repository Settings → Pages → Deploy from a branch → `main` / root → Save.

## Updating the app

Replace `index.html` in the repository. Phones get the new version the next time they open the app with a connection. Sessions saved on the phones are not affected.

## Keeping data safe

- Always open the app from its Home Screen icon. Safari and the icon keep separate data.
- Deleting the Home Screen icon deletes that phone's sessions. Export a backup first.
- Export a backup after each practice and keep it in Files, iCloud Drive, or email.
