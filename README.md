# Lotse — Jekyll Blog

A minimal, fast Jekyll blog theme for GitHub Pages. Dark monospace aesthetic, mobile-first, zero JavaScript on most pages.

## Local Development

**Prerequisites:** Ruby 3.x, Bundler

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## Deploy to GitHub Pages

1. Create a repo named `<your-username>.github.io` (for a user site) or any name (for a project site).
2. Push this folder's contents to the `main` branch.
3. In repo **Settings → Pages**, set source to **Deploy from a branch** → `main` → `/ (root)`.
4. GitHub Actions will build and publish automatically.

If using a **project site** (not `username.github.io`), update `_config.yml`:

```yaml
baseurl: "/your-repo-name"
url: "https://your-username.github.io"
```

## Writing Posts

Create files in `_posts/` following the naming convention:

```
_posts/YYYY-MM-DD-your-post-slug.md
```

**Front matter:**

```yaml
---
layout: post
title: "Your Post Title"
date: 2025-01-15
slug: your-post-slug       # used for the URL
read_time: 4               # optional, minutes
has_math: true             # set to true to load MathJax for LaTeX
---
```

## Math / LaTeX

Add `has_math: true` to any post's front matter. Then use standard LaTeX syntax:

- Inline: `$E = mc^2$` or `\( E = mc^2 \)`
- Display: `$$...$$` or `\[ ... \]`

## Customizing

- **Site name / description:** edit `_config.yml`
- **Colors / fonts:** edit `assets/css/main.css` (CSS variables at the top)
- **Layouts:** `_layouts/default.html` and `_layouts/post.html`

## Structure

```
.
├── _config.yml          # Site config
├── _layouts/
│   ├── default.html     # Base layout
│   └── post.html        # Post layout
├── _posts/              # Your blog posts (.md)
├── assets/
│   └── css/
│       └── main.css     # All styles
├── index.html           # Home page (year-grouped post list)
└── Gemfile
```
