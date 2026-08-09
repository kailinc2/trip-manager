# Trip Manager

A single-file, mobile-first web app for planning trips: day-by-day itinerary,
activities with times/locations/costs, and a budget breakdown. No backend, no
build step — all data lives in the browser's localStorage.

## Features

- Multiple trips (name, destination, dates, currency, optional budget)
- Day-by-day itinerary with a scrollable all-days overview and jump-to-day chips
- Activities with time, category, location (Google Maps link), cost, and notes
- Budget tab: total spent vs budget meter, per-category and per-day breakdowns
- Export/import trips as JSON files for backup or sharing between devices
- PWA: installable to the home screen, works offline

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000. (Any static file server works.)

## Deploy

Serve the repo root from any static host (GitHub Pages, Netlify, Cloudflare
Pages). All paths are relative, so a subpath like `/trip-manager/` works.
The service worker requires HTTPS (or localhost).

When shipping changes to `index.html` or other cached assets, bump the
`CACHE` version in `sw.js` so installed clients pick up the update.
