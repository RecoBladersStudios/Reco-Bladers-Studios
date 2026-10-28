# Reco Bladers Studios™ — Cinematic Static Website

A cinematic, responsive static website with animated backgrounds, a custom splash screen, interactive story cards, story search and filters, dark/light mode, announcement cards and an optional user-triggered sound toggle.

## Run it

1. Extract the ZIP.
2. Open `index.html` in a modern browser.
3. If your browser restricts any local features, run a local server from this folder:
   - Python: `python -m http.server 8000`
   - Then visit `http://localhost:8000`

No build step, database, account or external JavaScript library is required. Google Fonts are loaded from the internet when available; the site falls back to system fonts offline.

## Files

- `index.html` — site structure
- `styles.css` — theme, responsive layout and CSS animation system
- `js/config.js` — animation settings
- `js/motion.js` — ambient and splash particle canvases
- `js/theme.js` — dark/light mode
- `js/data.js` — local story and announcement data
- `js/app.js` — interactions, search, filters, dialogs and optional sound
- `data/stories.json` and `data/announcements.json` — human-editable data copies for content management
- `logo.png` and `assets/logo.png` — replaceable RBS logo asset
- `manifest.webmanifest` — optional PWA metadata
- `sitemap.xml` — starter sitemap (update the domain before hosting)
- `robots.txt` — crawler guidance

## Editing content

Update the story and announcement arrays in `js/data.js` to change what appears on the website. The `data/*.json` files are included as clean reference/editing copies; browsers cannot synchronously import local JSON from a `file://` page in every browser, so the site uses the data bundled in `js/data.js` for maximum compatibility.

For each story, use:
- `id`, `title`, `series`, `genres`, `status`, `symbol`
- `art.a`, `art.b`, `art.c` — colour values for the generated cover artwork
- `synopsis` and `detail`

## Logo

The included `logo.png` is a designed placeholder because no original logo file was attached when this ZIP was created. Replace both `logo.png` and `assets/logo.png` with your official logo, keeping the filename `logo.png`.

## Notes

- The contact section intentionally does not pretend to send messages. Connect a real form service if message delivery is needed.
- The sound toggle generates a short original synthesized tone only after a visitor clicks it; there is no autoplay audio.
- Animation respects reduced-motion preferences, and particle density is reduced on smaller screens.
- The exact required footer is included: `© 2026 ALL RIGHTS RESERVED RECO BLADERS STUDIOS™`.
