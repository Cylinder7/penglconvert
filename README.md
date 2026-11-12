# PenGL Universal Converter — static site

A single-page converter that turns 3D models (`.obj` `.stl` `.glb` `.fbx`)
or images (`.png` `.jpg` `.webp` …) into a **universal string** you paste into
the [PenGL Universal] Scratch project (press `0` in-game, paste, done).

Everything runs in the browser — no server, no uploads.

## Deploy to GitHub Pages

1. Unzip this folder into a GitHub repository (root of `main`, or a `docs/`
   folder, or a `gh-pages` branch — all work).
2. Repo **Settings → Pages** → *Build and deployment* →
   **Deploy from a branch**:
   - Branch: `main` (or `gh-pages`)
   - Folder: `/ (root)` — or `/docs` if you put the files there
3. Save. Your site goes live at `https://<user>.github.io/<repo>/`.

All asset paths are **relative** (`./assets/...`), so it works at any
sub-path, on a custom domain, or even opened straight from disk.

## What's inside

| File | Purpose |
| --- | --- |
| `index.html` | The converter page |
| `assets/` | Bundled JS + CSS (React, model parsers, encoders) |
| `PenGL_Universal.sb3` | The one-size-fits-all player project (in-page download) |
| `PenGL_3D_Renderer.sb3` | Base project for the "Build my .sb3" button |
| `logo.svg` | Favicon |
| `.nojekyll` | Tells GitHub Pages to skip Jekyll processing |

Note: fonts (Baloo 2 / Nunito) load from Google Fonts, so the page needs
internet for the exact typography — everything else is fully offline.

## Rebuilding from source

The source lives in the main PenGL repo under `converter-site/`
(Vite + React + Tailwind CSS 4). `npm install && npm run build` regenerates
this folder.
