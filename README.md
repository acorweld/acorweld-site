# ACorWeld site — deployment status & full file set

## Status
GitHub Pages and the acorweld.com domain (DNS at Hostinger) are already connected and were confirmed working earlier — that part is done. What's in this folder now is a **full update** on top of whatever is currently live in the `acorweld/acorweld-site` repo (still an early, Polish, placeholder version). Every file below should be uploaded, overwriting what's already there.

## Full file list
Root of the repo:
- `index.html` — full rewrite (English, new sections, SEO tags)
- `style.css` — full rewrite (matches the new HTML structure)
- `script.js` — unchanged since the very first version, but confirm it's actually in the repo
- `CNAME` — unchanged (`acorweld.com`)
- `robots.txt` — new
- `sitemap.xml` — new

`assets/` subfolder:
- `assets/logo.png`
- `assets/hero-photo.jpg`
- `assets/favicon.png`

## How to upload (overwriting the existing repo)
1. On your computer, create a folder, e.g. `acorweld-site`, and inside it a subfolder named exactly `assets`.
2. Put the 6 root-level files into `acorweld-site`, and the 3 images into `acorweld-site/assets`.
3. Go to `github.com/acorweld/acorweld-site` → **Add file → Upload files**.
4. Drag in everything from your local `acorweld-site` folder (including the `assets` subfolder — GitHub preserves the folder structure when you drop a folder in).
5. GitHub will show which files are being **replaced** (same filename as what's already in the repo) versus **added** (new, like `robots.txt`, `sitemap.xml`, and everything in `assets/`) — that's expected and correct.
6. Scroll down, add a short commit message (e.g. "English rewrite + real assets + SEO"), click **Commit changes**.
7. Check the **Actions** tab — wait for the green checkmark, then visit acorweld.com to confirm.

## Still needs your input before this is fully finished
- **CV** — buttons link to `cv-maciej-kochel.pdf`, which doesn't exist yet in the repo. Upload it (same filename, repo root) once ready.
- **LinkedIn URL** — still a placeholder (`PODMIEN-LINK`) in two spots in `index.html`: the Contact section and the structured-data block in `<head>`.
- **EN 1090 EXC3 vs EXC4** for the HD Iceland entry — sources disagreed, so the site currently just says "EN 1090" without the class number. Confirm the correct one and I'll add it back.
