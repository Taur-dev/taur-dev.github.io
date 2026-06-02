# Taur Studios — link-in-bio hub

The landing page used as the single link in the Taur Studios Instagram and Facebook bios.
It lists every Taur Studios app with store buttons, matching the studio's gold-on-charcoal brand.

Live URL (once published): **https://taur-dev.github.io/**

## Files

```
index.html        the page (self-contained HTML + CSS)
icons/            app icons (equine, flock, goat, rabbit) — 160px PNGs
screens/          Equine Companion screenshot previews — webp
```

Keep `index.html`, `icons/`, and `screens/` together — the page references them with
relative paths.

## Publish to GitHub Pages (user/org site → clean root URL)

This repo is meant to be the GitHub **user site**, which must be named exactly
`taur-dev.github.io`. It then serves from the root: `https://taur-dev.github.io/`.

1. Create a new, empty repo on GitHub named **`taur-dev.github.io`** (no README/license — keep it empty).
2. From this folder, point it at that repo and push:

   ```bash
   git remote add origin https://github.com/taur-dev/taur-dev.github.io.git
   git branch -M main
   git push -u origin main
   ```

3. In the repo on GitHub: **Settings → Pages → Build and deployment**.
   Set **Source: Deploy from a branch**, **Branch: `main` / `root`**, Save.
4. Wait 1–2 minutes, then open **https://taur-dev.github.io/**.

> Already using `taur-dev.github.io` for something else? Instead, drop these files into
> your existing `legal` repo (e.g. as a `/hub/` subfolder) — it would then serve at
> `https://taur-dev.github.io/legal/hub/`. The clean root URL above is preferable for a bio link.

## Updating

Edit `index.html` (or swap images in `icons/` / `screens/`), then:

```bash
git add -A
git commit -m "Update hub"
git push
```

GitHub Pages redeploys automatically within a minute or two.

## Still-optional placeholder

- `FLOCK_TEST_URL` (in the setup comment only) — if Flock Companion gets a public Google Play
  opt-in link, replace the Flock button's `mailto:` href with it. Until then, the button lets
  people request access by email.
