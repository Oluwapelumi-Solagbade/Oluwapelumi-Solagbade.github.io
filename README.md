# Oluwapelumi Solagbade — Personal Academic Website

Personal academic website for **Oluwapelumi Samuel Solagbade**, aspiring physician-scientist and computational neuroscientist.

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme, hosted on GitHub Pages.

🌐 **Live site:** https://vulcan-spark.github.io

---

## Quick Start

### Option A — Deploy Directly (Recommended)

1. Fork or clone this repo to your GitHub account
2. Rename the repo to `<your-github-username>.github.io`
3. Go to **Settings → Pages → Source → GitHub Actions**
4. Push any change to `main` — your site will build automatically

### Option B — Run Locally

**Requirements:** Ruby ≥ 3.1, Bundler, Node.js

```bash
# 1. Clone the repo
git clone https://github.com/Vulcan-Spark/Vulcan-Spark.github.io.git
cd Vulcan-Spark.github.io

# 2. Install dependencies
bundle install

# 3. Serve locally
bundle exec jekyll serve --livereload
# → Open http://localhost:4000
```

---

## Project Structure

```
.
├── _bibliography/
│   └── papers.bib          # All publications (BibTeX)
├── _data/
│   └── cv.yml              # Structured CV data
├── _news/                  # News/update posts (one .md per item)
├── _pages/
│   ├── about.md            # Home / About page
│   ├── publications.md     # Publications page
│   └── cv.md               # CV page
├── assets/
│   └── img/
│       └── profile.jpeg    # Profile photo
├── _config.yml             # Site configuration
├── Gemfile                 # Ruby dependencies
└── index.html              # Standalone HTML version (no Jekyll needed)
```

---

## Customizing

### Update personal info
Edit `_config.yml` — change name, email, GitHub username, description, etc.

### Add a publication
Add a BibTeX entry to `_bibliography/papers.bib`. Fields supported:
- `abbr` — venue badge (e.g., `Nature`)
- `selected = {true}` — shows on home page
- `doi`, `url`, `code`, `pdf`, `poster`, `slides`

### Add a news item
Create a new `.md` file in `_news/`:
```markdown
---
layout: post
date: 2026-03-01
inline: true
---
Your news text here. Markdown supported.
```

### Add a project
Create a `.md` file in `_projects/`:
```markdown
---
layout: page
title: Project Title
description: Short description
img: assets/img/project_thumb.jpg
importance: 1
category: research
---
Project details...
```

### Change profile photo
Replace `assets/img/profile.jpeg` with your photo. Keep the filename the same,
or update `profile.image` in `_pages/about.md`.

---

## Standalone HTML Version

`index.html` in the root is a **fully self-contained** version of the site —
no Jekyll, no build step, no dependencies. Just open it in a browser.

This is useful for:
- Previewing the site instantly
- Sharing as a single file
- Hosting on any static host (Netlify drag-and-drop, etc.)

> **Note:** The standalone version uses your profile photo from `assets/img/profile.jpeg`.
> Make sure that file is present when deploying.

---

## Deploying to GitHub Pages (Full Jekyll Setup)

After forking/cloning:

```bash
# Make sure you're on the main branch
git checkout main

# Copy the al-folio base theme files (if starting fresh)
# See: https://github.com/alshedivat/al-folio#getting-started

# Push your changes
git add .
git commit -m "Initial site setup"
git push origin main
```

GitHub Actions will automatically build and deploy your site. Check the
**Actions** tab in your repo for build status.

---

## License

MIT — feel free to use and adapt.

---

*Built with ❤️ from Ile Ife, Nigeria*
