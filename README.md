# EI-REC Redirect

Simple redirect site for `ei-rec.com` → `eirec-ets.com`.

Hosted on GitHub Pages with custom domain `ei-rec.com`.

## Behavior

- `ei-rec.com` → `eirec-ets.com`
- `ei-rec.com/*` → `eirec-ets.com` (path is NOT preserved)

## How it works

- `index.html` uses a JavaScript redirect (`window.location.replace`) and a meta refresh fallback.
- The deploy workflow copies `index.html` to `404.html` so GitHub Pages serves the redirect page for all unknown paths.
- `public/CNAME` tells GitHub Pages to serve the custom domain `ei-rec.com`.

## Deployment

Pushes to `main` trigger the GitHub Actions workflow to deploy to GitHub Pages automatically.
