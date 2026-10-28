# Simple Meridian · live demo

A static website that shows what [Google Meridian](https://developers.google.com/meridian) can tell a business, with an auto-playing guided tour of a made-up company's results. Nothing to install: it runs in the browser, sets no cookies and sends no data.

The full app (your own data, model fits, budget plans, GeoX lift tests) lives in [alibb007/Simple-Meridian](https://github.com/alibb007/Simple-Meridian) and runs on your computer with Docker.

## What is in here

| Path | What it is |
|---|---|
| `index.html` | the page |
| `assets/site.css`, `assets/site.js` | layout, charts drawn in SVG, and the tour |
| `assets/demo.json`, `assets/demo.js` | the demo company's results (same data, two formats; the `.js` copy lets the page work when opened from disk) |
| `assets/charts/*.png` | Meridian's own report charts, captured from the full app |
| `assets/how-it-works.html` | the 16-second motion graphic |
| `build_demo_json.py` | rebuilds `demo.json` / `demo.js`; run it inside the full app's repository, where `data/demo/` lives |

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
