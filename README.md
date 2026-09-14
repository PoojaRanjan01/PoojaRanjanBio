# Pooja Ranjan — Portfolio Website

A single-page, self-contained portfolio for **Pooja Ranjan — Data Science & AI Leader**.
No build step, no framework, no dependencies (only Google Fonts over CDN). Just static
files you can host anywhere.

> Live site: _add your URL here once deployed_

---

## Repository structure

```
pooja-ranjan-portfolio/
├── index.html                 # The entire site (HTML + CSS + JS in one file)
├── assets/
│   ├── headshot.jpg           # Hero photo  ← REPLACE with your real photo
│   └── favicon.png            # Browser tab icon
├── robots.txt                 # Search-engine indexing rules
├── .nojekyll                  # Tells GitHub Pages to serve files as-is
├── .gitignore
├── LICENSE
├── .github/
│   └── workflows/
│       └── deploy.yml         # Auto-deploys to GitHub Pages on push to main
└── README.md
```

---

## Quick start (view locally)

Just open `index.html` in a browser. Or serve it:

```bash
# Python 3
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Customize

### 1. Replace the headshot  (do this first)
`assets/headshot.jpg` is currently a placeholder monogram. Replace it with your real
photo, **keeping the same filename** (`assets/headshot.jpg`). Crop it roughly square —
the hero displays it as a circle.

### 2. Edit the content
All copy lives in `index.html`, grouped by section (`Summary`, `Selected work`,
`Leadership`, `Speaking & recognition`, `Experience`, `Contact`). Search for the section
name and edit the text between the tags.

### 3. Change the accent colors
Near the top of `index.html`, in the `:root { ... }` CSS block:
- `--cyan` — the network / links / highlight color
- `--gold` — reserved for awards
- `--ink`  — the background

### 4. (Optional) Add a "Download résumé" button
Drop your PDF at `assets/resume.pdf`, then paste this inside the hero `.actions` div in
`index.html`:

```html
<a class="btn" href="assets/resume.pdf" target="_blank" rel="noopener">Download résumé</a>
```

---

## Deploy

### Option A — GitHub Pages (recommended)
1. Create a new GitHub repo and push these files to the `main` branch.
2. In the repo: **Settings → Pages → Build and deployment → Source = GitHub Actions.**
3. The included workflow (`.github/workflows/deploy.yml`) publishes the site
   automatically on every push. Your URL will be
   `https://<your-username>.github.io/<repo-name>/`.

_(Alternative: Settings → Pages → Source = "Deploy from a branch" → `main` / `root`.
The `.nojekyll` file is already included so everything serves correctly.)_

### Option B — Netlify (fastest)
Go to **app.netlify.com/drop** and drag this whole folder in. Instant URL.

### Option C — Vercel / Cloudflare Pages
Import the repo (framework preset: **Other / static**) or drag-and-drop the folder.

### Custom domain
Add a file named `CNAME` (no extension) at the repo root containing just your domain,
e.g. `poojaranjan.com`, then point your domain's DNS at your host per their docs.

---

## Privacy note (please read)

This site is **public and indexable by search engines**, including your current employer.
Every metric on the page is deliberately **generalized** ("multi-million-dollar",
"the majority of platform revenue", "a significant margin improvement") — do **not** add
exact revenue, margin, or investor figures to a public page. Keep specifics for interviews.

To keep the site out of search results entirely, edit `robots.txt` and change
`Allow: /` to `Disallow: /`.

---

© 2026 Pooja Ranjan. Content all rights reserved. See `LICENSE.txt`.
