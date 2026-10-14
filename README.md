# 100 — A Creative HTML Showcase

One hundred standalone, self-contained HTML experiments in motion, light and mathematics.
Every piece is a **single `.html` file** — open it, read it, ship it. No build step, no dependencies to install.

## What's inside

| | |
|---|---|
| `index.html` | The gallery — a searchable, filterable grid of all 100 pieces. **Start here.** |
| 100 × `*.html` | The pieces themselves, one file each, organised in 10 disciplines. |

**The 10 disciplines:** 3D Worlds · Shaders · Generative · Physics · Fractals · CSS · SVG · Retro · Organic · Data & Geometry.

Every piece:
- is a single self-contained HTML file (all CSS/JS inline);
- fills the viewport and handles resize + devicePixelRatio;
- animates smoothly (requestAnimationFrame / CSS);
- carries a discreet title badge with a link back to the gallery;
- uses libraries only via CDN (Three.js r128, Google Fonts) — so an internet connection is needed on first load for those.

## Preview locally

Open `index.html` in any modern browser. Hover a card for a **live render** of the piece.
(Some browsers restrict `file://` iframes; for the best experience serve the folder over HTTP.)

```bash
# from inside this folder
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publish to GitHub Pages (a github.io page)

1. Create a new **public** repository. To get a URL like `https://<your-username>.github.io`, name the repo exactly `<your-username>.github.io`. (Any other repo name works too — it just serves at `https://<your-username>.github.io/<repo-name>/`.)
2. Upload the contents of this folder to the repo root — `index.html` and all 100 `.html` files must sit at the top level.
3. In the repo, go to **Settings → Pages**, set **Source** to *Deploy from a branch*, choose branch `main` and folder `/ (root)`, and save.
4. Wait a minute. Your gallery is live at `https://<your-username>.github.io/`.

From the command line instead:

```bash
git init
git add .
git commit -m "100 creative HTML pieces"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

## Notes

- The gallery's hover previews load each piece in a small iframe; toggle them off with the **Live previews** button if you're on a slow connection.
- Press `/` anywhere in the gallery to jump to the search box, and **surprise me** opens a random piece.
- All visuals are original code. No image or video assets are bundled — everything is generated at runtime.
