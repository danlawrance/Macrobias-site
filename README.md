# Macrobias — Netlify deploy folder

This folder is ready to drop onto Netlify (or Vercel / Cloudflare Pages).

## How to deploy
1. Go to app.netlify.com → "Add new site" → "Deploy manually".
2. Drag this whole folder onto the upload area.
3. Done — your site is live at a netlify.app URL.
4. Add your domain (macrobias.com) under Site settings → Domain management.

## What's here
- `index.html` — the homepage (served at the root URL).
- `Polaris Landing.dc.html` — same homepage under its original name (internal "Home" links use this).
- `Dashboard.dc.html`, `News Hub.dc.html`, `Methodology.dc.html`, `Indicator.dc.html`, `Pricing.dc.html`, `Login.dc.html`, `Legal.dc.html` — the other pages.
- `support.js` — the runtime that powers the pages (required; do not rename).
- `news-feed.json`, `bias-feed.json`, `calendar-feed.json` — the live-data files.

## About the data
The site reads the three `*-feed.json` files. They currently hold sample/demo data,
so the site works immediately but isn't "live" yet. To make data real, your data
collector overwrites these three files on a schedule (see DEPLOYMENT.md and the
feed specs in the main project). The site picks up changes automatically — no redeploy.

Keep all files in the same folder (same origin) so the pages' relative fetches resolve.
