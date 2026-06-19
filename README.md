# Greenhouse under photovoltaic shading — QR landing site

Static site (no build step) that the poster QR code points to. Three pages:

| file | role |
|---|---|
| `index.html` | landing hub: 3 cards (ERMESS Green, Digital poster, References) |
| `poster.html` | digital poster with added explanations + figures |
| `references.html` | bibliography with DOI links |
| `img/` | figures used by the digital poster |

## Deploy on GitHub Pages

1. Create a repo (e.g. `agrivolt-greenhouse-sim`) and push the **contents of this `web/` folder** to it (so `index.html` is at the repo root, or under `/docs`).
2. Repo → Settings → Pages → Source = `main` branch, folder `/ (root)` (or `/docs`).
3. The site goes live at `https://<user>.github.io/<repo>/`.

`.nojekyll` is included so GitHub Pages serves the files as-is.

## TWO things to fill in before publishing

1. **ERMESS Green URL** — in `index.html`, replace `https://REPLACE-ME-ermess-green-url` with the real project page.
2. **QR target** — the printed QR currently encodes `agrivolt-greenhouse-sim.usmb.fr`. Point it to the GitHub Pages URL above (regenerate the QR with the new URL, then re-run `make_qr_greenhouse.py` so the poster picks up the new code).

## Local preview

```
cd web && python3 -m http.server 8000
# open http://localhost:8000
```
