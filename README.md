# 🦄 Unicorn Times Tables

A sparkly, unicorn-themed game that helps kids master multiplication tables **1 to 20** (each table from ×1 to ×10). Built for a 9-year-old — big friendly buttons, cheerful sounds, confetti, and a galloping unicorn. No backend, no login, no ads: everything runs in the browser and progress is saved on the device.

## ✨ Features

- **Practice mode** — 10 cozy, untimed multiple-choice questions per table, with smart wrong-answer options and gentle feedback. Missed facts come back sooner (simple spaced repetition).
- **Rainbow Race** — a 60-second dash! Every correct answer makes the unicorn gallop further along the rainbow. High scores are saved per table.
- **Star Meadow** — a progress map. Answer a fact correctly 3 times to *capture* its star. See per-table mastery (e.g. 7/10 ⭐) and overall progress toward all 200 facts.
- **Rewards** — stars for every correct answer, streak counter with a special rainbow celebration at every 5-in-a-row, best streak and personal bests remembered.
- **Sound** — cheerful chimes generated with the Web Audio API (no audio files), with a mute toggle that remembers its setting.
- **PWA** — can be added to a phone's home screen and opened full-screen like a real app. Works offline after the first visit.
- Respects `prefers-reduced-motion` and stays smooth on low-end phones.

## 📁 Files

| File | What it is |
|---|---|
| `index.html` | The whole game (HTML + CSS + JavaScript in one file) |
| `manifest.json` | PWA manifest (app name, colors, icons) |
| `sw.js` | Service worker for offline play |
| `icon-192.png`, `icon-512.png` | Unicorn app icons |

## 🚀 Deploy to Vercel (free)

### Method 1 — Drag & drop (fastest)

1. Go to [vercel.com](https://vercel.com) and sign up / log in (free Hobby plan is fine).
2. Open [vercel.com/new](https://vercel.com/new).
3. Drag this **entire project folder** onto the page (or click *Browse* and select it).
4. Leave every setting as-is (no framework, no build command needed) and click **Deploy**.
5. In ~10 seconds you'll get a live URL like `https://your-project.vercel.app` — share it and play!

### Method 2 — GitHub (auto-deploys on every change)

1. Push this folder to a GitHub repository.
2. On [vercel.com/new](https://vercel.com/new), click **Import** next to that repository.
3. Leave the defaults (Framework Preset: *Other*, no build command, output directory: root) and click **Deploy**.
4. Every future `git push` to the main branch redeploys automatically.

## 📱 Add it to a phone's home screen

1. Open the live URL in the phone's browser.
2. **Android (Chrome):** tap the ⋮ menu → **Add to Home screen** → **Install**.
3. **iPhone (Safari):** tap the Share button → **Add to Home Screen**.
4. A unicorn icon appears — tapping it opens the game full-screen, even offline.

## 🧪 Run locally

The service worker needs a web server (opening `index.html` directly via `file://` works for playing, but offline/PWA features won't activate). From the project folder:

```bash
npx serve .
# or
python -m http.server 8000
```

Then open the printed local URL.

## 💾 Where progress is stored

All progress (stars, captured facts, best streak, race high scores, mute preference) lives in the browser's `localStorage` on the device. Clearing browser data resets the game; different devices/browsers each keep their own progress.
