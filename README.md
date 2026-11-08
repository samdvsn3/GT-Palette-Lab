# GT Palette Lab — Growtopia Color Finder

A static, browser-based Growtopia item finder that ranks items by the dominant hues in their inventory sprites. Includes color-name / HEX search, optional item-name narrowing, category filters, sprite previews, item IDs, and Growtopia Wiki links.

## Run locally

Open `index.html` in a modern browser while online. The item catalog and sprite sheets are fetched from the public Growtopia Explorer GitHub repository at runtime.

If your browser blocks local-file requests, run a tiny local server in this folder:

```bash
python -m http.server 8080
```

Then open <http://localhost:8080>.

## Publish it online for free

1. Create a new public or private GitHub repository.
2. Upload `index.html` (and this README if desired) to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. GitHub Pages will show the public URL when deployment is ready. A private repo can require a paid GitHub plan for private Pages access; use a public repo for free public hosting.

Alternatively, upload the folder to a static host such as Netlify or Vercel.

## Data and image sources

- Item index and sprite coordinate manifest: [araeys/growtopia-explorer](https://github.com/araeys/growtopia-explorer), `public/items_db.json` and `public/tilesheets_info.json`.
- Sprite atlases are loaded from that repository's `public/tilesheets/` folder.
- The upstream project describes its item catalog as 16,304+ records extracted from Proton `items.dat` v26. The app does not claim this is an official Ubisoft API or a guaranteed complete live snapshot of every item in the 2026 client.
- Original game art and Growtopia intellectual property remain with Ubisoft / Robinson Technologies. This is an unofficial fan-made utility.

The app does not bundle or copy the upstream project's application code. It fetches the public item index and image atlases directly from the repository when opened.
