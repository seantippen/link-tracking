# Link Tracking — QR Scan Analytics Dashboard

## Project
GitHub Pages dashboard for the greenvilletriumph.club QR link tracking system. Fetches live scan data from the `/api/scans` endpoint and visualizes it with Chart.js + Leaflet.

- **Dashboard URL**: https://linktracking.seantippen.com/
- **Data source**: https://greenvilletriumph.club/api/scans?days=30
- **Backend code**: `Triumph dot Club/` (Cloudflare Pages + D1)
- **GitHub repo**: https://github.com/seantippen/link-tracking

## Related: seantippen.com Project Card
This project has a card on seantippen.com that links to the dashboard.
- **Card file**: `personal-website/apps/hub/src/content/projects/link-tracking.md`
- **Card links to**: https://seantippen.github.io/link-tracking/
- **When to update the card**: If the dashboard URL changes, status changes, or description/tags need updating, update that markdown file and push the personal-website repo.

## Architecture
- greenvilletriumph.club is ONLY for redirects + API. No dashboard or public UI on the .club domain.
- Dashboard lives on GitHub Pages (this repo)
- Backend code lives in `Triumph dot Club/` (separate Cloudflare Pages project)

## Design System — Triumph Override
Dark theme, green/blue accents.

### Colors
| Token | Value | Usage |
|-------|-------|-------|
| `--bg-base` | `#0a0d12` | Page background |
| `--bg-surface` | `#111827` | Cards, panels |
| `--bg-surface-hover` | `#1f2937` | Hover states |
| `--border` | `rgba(255,255,255,0.06)` | Card borders |
| `--text-primary` | `#f3f4f6` | Headings, values |
| `--text-secondary` | `#9ca3af` | Labels, descriptions |
| `--accent-green` | `#22c55e` | Primary accent, positive metrics |
| `--accent-blue` | `#3b82f6` | Secondary accent, links |

### Typography
- **Headings**: Inter (400/600/700)
- **Mono/Data**: JetBrains Mono
- **Load via Google Fonts** `<link>` tag

### Visual Effects
- Dot grid background, aurora gradient, frosted glass header, subtle card hover glow

## Tech Stack
- Single-file HTML with inline CSS/JS (no build step)
- Chart.js 4.4.7 (CDN)
- Leaflet 1.9.4 for geo map (CDN)
- Fetches live data from greenvilletriumph.club API (CORS enabled)
- Deploy: GitHub Pages (git push to main)

## Git Config
```
user.email=github@seantippen.com
user.name=Sean Tippen
```
