# Panthers Shot Tracker

Tap-to-log basketball shot tracker for practice. One tap is a make, a double tap is a miss. Tracks team and individual shooting by court zone, builds single- and multi-session reports, and exports PDF reports and CSV spreadsheets.

All signed-in coach phones share the same live data through a free Firebase database. Shots logged without a connection are kept on the phone and sync when it reconnects.

## Files

| File | What it is |
|---|---|
| `index.html` | The app |
| `firebase-config.js` | Your Firebase settings (paste them in once) |
| `firestore.rules` | Database rules that limit access to coach emails (paste into Firebase) |
| `sw.js` | Lets the app open with no signal |
| `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png` | Home Screen name and icon |

## Setup

1. **Firebase project:** console.firebase.google.com → Create a project → turn off Google Analytics.
2. **Sign-in:** Build → Authentication → Get started → Email/Password → Enable. Then Users → Add user for each coach.
3. **Database:** Build → Firestore Database → Create database → Production mode. Then Rules → paste `firestore.rules` with your coach emails → Publish.
4. **Settings:** Project settings → Your apps → Web (`</>`) → Register app. Copy the six values into `firebase-config.js`.
5. **Authorized domain:** Authentication → Settings → Authorized domains → Add your `username.github.io`.
6. **GitHub Pages:** Repository Settings → Pages → Deploy from a branch → `main` / root → Save.

## Adding a coach later

Add them in Firebase Authentication → Users, then add their email to the list in Firestore → Rules → Publish.

## Updating the app

Replace `index.html` in the repository. Phones pick up the new version the next time they open the app online. If a phone still shows the old version, close the app and open it again.
