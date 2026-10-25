# Second Brain

Eight notes for ideas, reminders, birthdays and a monthly reset. Works offline and installs like an app.
Notes are stored in your browser (localStorage) on the device you use.

## Files
- `index.html` the whole app
- `manifest.webmanifest` name, icons, standalone display
- `sw.js` offline cache (change `VERSION` whenever you edit a file)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`

## Run locally
    python3 -m http.server 8000
    # open http://localhost:8000

## Publish with GitHub Pages
    git init
    git add .
    git commit -m "Second Brain notes app"
    git branch -M main
    git remote add origin https://github.com/<your-username>/second-brain-notes.git
    git push -u origin main

Then on GitHub: Settings > Pages > Source: "Deploy from a branch" > Branch: `main` / `/ (root)` > Save.
Your app will be at `https://<your-username>.github.io/second-brain-notes/` after about a minute.

## Install on your phone
- Android (Chrome): open the URL, tap the three-dot menu, then "Install app" or "Add to Home screen".
- iPhone (Safari): open the URL, tap Share, then "Add to Home Screen".

## Updating later
    git add .
    git commit -m "Describe the change"
    git push

Bump `VERSION` in `sw.js` (for example `v2`) so installed copies pick up the new files.
