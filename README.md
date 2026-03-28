# HYROX PBC Tracker

Personal Hyrox training tracker for Guero. Race day: **May 16, 2026** · Goal: **Sub 1:40**.

## Setup

### 1. Anthropic API Key (for screenshot analysis)

The app uses Claude to extract workout data from Apple Health screenshots. To enable this:

1. Get an API key at [console.anthropic.com](https://console.anthropic.com)
2. Open the app → tap the ⚙ gear icon in the top-right corner
3. Paste your key (`sk-ant-...`) and tap **Guardar API Key**

The key is stored only in your device's `localStorage` — never sent anywhere except Anthropic's API.

### 2. GitHub Pages deployment

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/hyrox-tracker.git
git push -u origin main
```

Then in GitHub → Settings → Pages → Source: **Deploy from branch `main`**, folder `/`.

The app will be live at `https://YOUR_USERNAME.github.io/hyrox-tracker/`

### 3. PWA icons (optional, for "Add to Home Screen")

Add two PNG files to the project root:
- `icon-192.png` — 192×192px
- `icon-512.png` — 512×512px

Without these, the PWA installs but uses a default icon.

## Local development

Just open `index.html` in a browser — no build step required.

## Weekly schedule

| Day | Workout |
|-----|---------|
| Mon | BMoore Bootcamp |
| Tue | Índole Cycling |
| Wed | CrossFit Cholula |
| Thu | Rower Train |
| Fri | Hyrox Training ZP |
| Sat | Run 5–8km |
| Sun | Rest |

## Tech stack

- Pure HTML/CSS/JS — no framework, no build step
- [Chart.js](https://www.chartjs.org/) for analytics charts
- [Anthropic API](https://docs.anthropic.com) (`claude-sonnet-4-20250514`) for image analysis
- `localStorage` for session persistence
- Google Fonts: Bebas Neue, DM Mono, DM Sans
