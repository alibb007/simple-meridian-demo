# Simple Meridian · live demo

**Live site: https://alibb007.github.io/simple-meridian-demo/**

A static website that walks through what [Google Meridian](https://developers.google.com/meridian) can tell a business, as an auto-playing guided tour of a made-up company's results. Nothing to install: it runs in the browser and sets no cookies. [GoatCounter](https://www.goatcounter.com/) counts visits and button clicks without storing anything that identifies a visitor.

The full app (your own data, model fits, budget plans, GeoX lift tests) lives in [alibb007/Simple-Meridian](https://github.com/alibb007/Simple-Meridian) and runs on your computer with Docker.

## What is in here

| Path | What it is |
|---|---|
| `index.html` | the page: the tour itself |
| `assets/site.css`, `assets/site.js` | layout, charts drawn in SVG, and the tour engine |
| `assets/demo.json`, `assets/demo.js` | the demo company's results (same data, two formats; the `.js` copy lets the page work when opened from disk) |
| `assets/charts/*.png` | Meridian's own report charts, captured from the full app |
| `assets/story.html` | the seven-scene story shown before the tour |

The tour's text and the scripts that build this site live in the full app's repository, under [`scripts/site/`](https://github.com/alibb007/Simple-Meridian/tree/main/scripts/site): `tour_steps.py` (titles and captions), `build_site_data.py` (rebuilds `demo.json` / `demo.js`), `stamp_assets.py` and `publish.sh`.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

then go to <http://localhost:8000>.

## Updating it

The site is generated from the full app. In the `Simple-Meridian` repository, edit `docs/`, then copy that folder's contents here.

---

Built by Ali Barfi Bafghi on the open-source Google Meridian and Meridian GeoX libraries. Not affiliated with or endorsed by Google. Meridian is a trademark of Google LLC. Results shown are from made-up data.
