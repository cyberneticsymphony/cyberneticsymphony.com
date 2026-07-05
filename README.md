# Cybernetic Symphony

A minimal personal blog built with Jekyll and hosted on GitHub Pages. Write
Markdown, push, done — GitHub builds the site for you. No local build step.

## Writing a post

Add a Markdown file to `_posts/` named `YYYY-MM-DD-title.md`. The date and slug
come from the filename. Start it with front matter:

```
---
layout: post
title: My Thoughts
---
Body text in Markdown...
```

Commit and push. GitHub Pages rebuilds automatically within a minute or so.

## How the homepage works

Posts appear newest-first down the page. A post whose text is under 500
characters is shown in full; a longer post shows a preview with a "Read more"
link. Every post always has its own page at `/posts/title/`.

The 500-character threshold and preview length live in `_config.yml`
(`preview_limit`, `preview_chars`).

## Layout & styling

- `_layouts/default.html` — page chrome (centered title, top menu)
- `_layouts/post.html` — a single full post
- `index.html` — the homepage feed with the preview logic
- `style.css` — all styling (Pixelify Sans, colors, spacing)
- Top menu is the `nav:` list in `_config.yml`

## Previewing locally (optional)

Requires Ruby. Once:

```
bundle install
```

Then:

```
bundle exec jekyll serve
```

Open http://localhost:4000

## Publishing

Push to the branch GitHub Pages is set to build from (Settings → Pages → Build
and deployment → Source: "Deploy from a branch"). The `CNAME` file points the
site at `cyberneticsymphony.com`.
