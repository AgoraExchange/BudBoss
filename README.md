# Bud Boss: Dispensary Tycoon 🌿

A mobile-first, installable business-sim game inspired by shop/grow-management games like *Weed Shop 2*. Plant and cure strains, run the storefront, upgrade your grow room, and manage your "heat" so you don't get busted — all in the browser, installable as a full-screen app on your iPhone.

## What's included
- `index.html` — the entire game (UI + logic, no build step needed)
- `manifest.json` — PWA manifest (name, icons, standalone display)
- `sw.js` — service worker for offline caching
- `icon-192.png`, `icon-512.png` — app icons

## How to play
- **🏪 Shop** — customers walk in wanting a strain and quantity. Sell if you have stock; watch out, some customers are undercover cops (risk rises with "heat").
- **🌱 Grow Room** — plant seeds in pots, water them (or buy the Shop Runner upgrade to auto-water), and harvest once ready.
- **🫙 Cure** — harvested buds cure in jars over time for a quality bonus (Rough → Decent → Fire → Legendary), then buy seeds for your next crop.
- **⬆️ Upgrades** — spend cash on more pots, better lighting, soil, curing jars, and security to lower bust risk.
- **📊 Stats** — track lifetime earnings, sales, reputation, and unlocked strains.

Progress autosaves to your phone/browser's local storage every few seconds.

## Deploy to GitHub Pages (so you can open it on your iPhone)

1. **Create a new GitHub repo** (e.g. `bud-boss`), and upload these 5 files to the root of the repo — you can drag-and-drop them right in the GitHub web UI ("Add file" → "Upload files").
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch = `main` (or `master`), folder = `/ (root)`. Click **Save**.
4. Wait ~1 minute, then GitHub will show your live URL, something like:
   `https://YOUR-USERNAME.github.io/bud-boss/`
5. Open that URL — the game should load right away.

## Add it to your iPhone Home Screen (turns it into a full PWA)

1. Open the GitHub Pages URL in **Safari** on your iPhone (must be Safari, not Chrome — Chrome on iOS can't install PWAs).
2. Tap the **Share** button (square with an arrow pointing up).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add** in the top right.
5. A "Bud Boss" icon now appears on your home screen. Opening it launches the game full-screen with no Safari address bar, and it works offline once loaded thanks to the service worker.

## Notes / customization ideas
- All game balance numbers (strain prices, grow times, upgrade costs) live near the top of the `<script>` block in `index.html` in the `STRAINS` and `UPGRADES` objects — easy to tweak.
- Want a different game name or icon? Update the `<title>`, the `#splash` text, `manifest.json`, and swap out `icon-192.png` / `icon-512.png`.
- This is themed as a lighthearted business simulator (fictional strains, no real-world cultivation or drug-use info) — safe to share as a portfolio/game project.
