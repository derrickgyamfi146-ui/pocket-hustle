# Pocket Hustle v1.0

A mobile-first, offline-first small-business manager built with HTML, CSS and vanilla JavaScript.

## Files
- `index.html` — application screens and layout
- `styles.css` — responsive design and light/dark themes
- `app.js` — IndexedDB storage, business logic and interactions
- `manifest.webmanifest` — PWA install metadata
- `sw.js` — offline app-shell caching

## Run locally
Open `index.html` in a browser for a basic preview. IndexedDB works on modern browsers. Service workers and PWA installation require HTTPS or localhost; use an HTTPS static host such as GitHub Pages or Cloudflare Pages for install/offline caching.

## Android publishing
Upload the folder to a GitHub repository, enable GitHub Pages (Settings → Pages → deploy from branch → main/root), then open the HTTPS Pages URL in Chrome and choose Install app / Add to Home screen.

## Data and limitations
All business records are stored in IndexedDB on the current browser/device. This version has no login, cloud sync, payment processing, or multi-device backup. Export JSON backups regularly. Product images are compressed and stored locally in IndexedDB. The catalogue shares product text through WhatsApp; product images are not attached automatically.

## Financial logic
Sale profit = sale revenue after discount − recorded unit buying cost × quantity. Estimated net profit = sale profit across non-cancelled sales − recorded expenses. Revenue is shown separately from profit. Pending orders are included until cancelled; this is a simple cash/sales tracker, not formal accounting or tax software.
