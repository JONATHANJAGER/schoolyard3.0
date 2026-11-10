# Schoolyard 3.0 — GitHub Pages preview

This is a **new functional UI preview**, not a merge of the old Cyber-Course code (the older ZIP archives were not available in this chat). Do not delete the existing repository until you have tested this separately.

## Included
- Responsive dashboard, nine course cards, course/lesson navigation, notes, knowledge checks, skip-and-return tracking, portfolio overview, local JSON backup/import.
- Approved Professor David portrait, floating/minimizable/fullscreen panel, pulsing indicator, **browser text-to-speech demo**.
- Firebase Email/Password sign-in and automatic Firestore sync of preview progress/notes, with simple latest-updated conflict selection.
- Example Firestore rules and existing Firebase public web config.

## Not yet implemented
- Full nine-month authored curriculum and 5-question graded assessments (4/5 pass). Preview questions do **not** grant completion.
- Real-time AI conversation, microphone, persistent conversation memory, lip-synced video tutorials, real lab environments, fully built MASS prototype, or production-grade offline conflict merging.
- Do not treat this preview as a production-ready school or a complete security audit.

## Deploy
1. Create a **new test GitHub repository** (or use a separate branch), rather than replacing your current Schoolyard immediately.
2. Unzip, then upload the **contents** of this folder to the repository root. `index.html` must be at the root.
3. GitHub Settings → Pages → Deploy from a branch → `main` / `(root)`.
4. In Firebase Authentication settings, add `YOUR-USERNAME.github.io` as an authorized domain if required.
5. In Firestore Rules, review and publish `firestore.rules` **only if** appropriate for your other app data. Rules shown protect `users/{uid}/progress/{id}` and do not grant access to unrelated collections.
6. Open the HTTPS GitHub Pages site, sign up or sign in under Account & Sync, and test saving notes on two devices.

Browser-only local `file://` access will not load `courses.json` reliably; use HTTPS hosting.
