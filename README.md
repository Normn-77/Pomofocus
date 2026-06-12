# Focus Noir

Art Deco Pomodoro timer. Installable as a PWA on desktop and web.

## Deploy to GitHub Pages

1. Create a new repo on GitHub (e.g. `focus-noir`)
2. Push these files to the repo root:
   ```
   index.html
   manifest.json
   sw.js
   icon.svg
   ```
3. Go to **Settings → Pages → Source** → select `main` branch, `/ (root)`
4. Your app will be live at `https://yourusername.github.io/focus-noir/`

## Install as desktop PWA

Once live on GitHub Pages (or any HTTPS host):

- **Chrome / Edge**: visit the URL → address bar shows an install icon (⊕) → click it → Install
- **macOS Safari**: Share → Add to Dock
- The app opens in its own window, no browser UI

## Run locally

```bash
# any static server works, e.g.:
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080` — PWA install requires HTTPS in production, but the timer itself works over HTTP locally.

## Features

- Pomodoro timer with configurable durations
- Short break / Long break cycle
- Auto-start break / pomodoro options
- Disable breaks mode
- 6 procedural sounds (Web Audio API, no audio files)
- Volume control + per-phase sound selection
- Statistics: today / this week / total focus time
- Best day / daily average
- Daily / weekly / monthly / yearly chart
- Full session records table
- Accurate timer via Web Worker + timestamp (immune to tab throttle)
- Film grain + vignette + Art Deco aesthetic
- Fully offline after first load (service worker)
