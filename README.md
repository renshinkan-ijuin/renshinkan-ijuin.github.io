# 錬心舘 伊集院支部 — website

Static site: `index.html` + `img/`. No build step.

## Publish on GitHub Pages
1. Create a repo (e.g. `renshinkan-ijuin`) and upload `index.html`, `README.md` and the `img/` folder.
2. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)` → Save.
3. After ~1 minute the site is live at `https://<your-username>.github.io/renshinkan-ijuin/`.

## Editing
- **News (お知らせ):** in `index.html`, find `<script type="application/json" id="news-data">` and add an item:
  `{"date":"2026-12-01","ja":"日本語のタイトル","en":"English title"}` (comma between items). Newest shows first; 8 are shown.
- **Phone / email:** the phone number is in the `.contact` block near the bottom of index.html. No email is shown yet; add a `<span>` line there when you have one.
- **Student voices:** the page is live (`#voices`). Each card is an `<article class="voice">` in `view-voices`; photos are square crops in `img/voice-*.jpg`. To hide the page, comment out the nav link and set `VOICES_ON=false` in the script.
- **Photos:** put new photos in `img/` (resize to ~1400px wide first) and change the `src="img/..."` paths.
- Every text appears twice: `<span class="ja">…</span><span class="en">…</span>` — edit both.
