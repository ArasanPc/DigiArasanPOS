# DIGI ARASAN POS

A single-file mobile POS/billing web app, installable as a PWA with the
DIGI ARASAN logo as its app icon.

## Files
```
digiarasan-pos/
├── index.html        ← the app
├── manifest.json      ← PWA config (name, icons, colors)
├── favicon.ico
├── icons/              (16px → 512px logo icons, auto-generated)
└── .nojekyll           (tells GitHub Pages to serve files as-is)
```

Keep this folder structure intact — index.html links to `manifest.json`,
`favicon.ico`, and `icons/...` using relative paths.

## Why GitHub / GitHub Pages
Chrome will only let you properly **install this as an app with the logo
showing** when it's served over `http://` or `https://` — not when opened
directly as a local file (`file://...`). GitHub Pages gives you a free
`https://` link, which fixes this.

## 1. Push this repo to GitHub

From inside this `digiarasan-pos` folder:

```bash
git init
git add .
git commit -m "DIGI ARASAN POS"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

(Create the empty repo on GitHub first at https://github.com/new — don't
initialize it with a README there, to avoid a merge conflict.)

## 2. Turn on GitHub Pages

1. On GitHub, open your repo → **Settings** → **Pages**.
2. Under "Build and deployment" → **Source**, choose **Deploy from a
   branch**.
3. Branch: `main`, folder: `/ (root)` → **Save**.
4. Wait ~1 minute. Your live URL will appear at the top of that page:
   ```
   https://<your-username>.github.io/<your-repo>/
   ```

## 3. Install it as an app (this is what shows your logo)

1. Open your live `https://...github.io/...` link in **Chrome**.
2. Click the **install icon (⊕)** in the address bar
   — or ⋮ menu → **Save and share** → **Install page as app**.
3. Click **Install**.

Chrome will create a desktop/home-screen shortcut named **DIGI ARASAN**
using the logo from `manifest.json` / `icons/`, and it'll open in its own
app window instead of a browser tab.

## Updating later
Edit `index.html` (or any file), then:
```bash
git add .
git commit -m "update"
git push
```
GitHub Pages redeploys automatically in under a minute.
