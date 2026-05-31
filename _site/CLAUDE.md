# CLAUDE.md

## Project Overview

Personal portfolio website for Amit Baranwal. Built with Jekyll and the Minimal Mistakes theme, deployed on GitHub Pages at https://amitbaranwal53.github.io.

## Tech Stack

- **Static site generator:** Jekyll
- **Theme:** Minimal Mistakes (via `remote_theme`)
- **Hosting:** GitHub Pages (deploys automatically on push to `main`)
- **Gems:** `github-pages`, `jekyll-include-cache`

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Site will be available at http://localhost:4000

## Project Structure

```
.
├── _config.yml          # Site configuration (theme, author, defaults)
├── _data/
│   └── navigation.yml   # Top nav menu items
├── _pages/
│   ├── about.md         # /about/
│   ├── blog.md          # /blog/ (lists posts)
│   └── projects.md      # /projects/
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── assets/images/       # Static images (avatar, post images)
├── index.md             # Home page
├── 404.md               # Custom 404
├── Gemfile              # Ruby dependencies
└── CLAUDE.md            # This file
```

## Key Conventions

- **Posts** go in `_posts/` with filename format `YYYY-MM-DD-slug.md`
- **Pages** go in `_pages/` with a `permalink` in front matter
- **Images** go in `assets/images/`
- All posts default to `layout: single`, `author_profile: true`, `read_time: true`, `toc: true`
- Theme skin is "dark"
- Navigation is defined in `_data/navigation.yml`

## Adding Content

### New blog post
Create `_posts/YYYY-MM-DD-title.md` with front matter:
```yaml
---
title: "Post Title"
date: YYYY-MM-DD
categories:
  - category-name
tags:
  - tag1
  - tag2
toc: true
---
```

### New project
Add a section to `_pages/projects.md`.

## Deployment

Push to `main` branch. GitHub Pages builds and deploys automatically. No CI/CD configuration needed — GitHub Pages handles Jekyll builds natively.

## Important Notes

- Do NOT use `theme:` in `_config.yml` — use `remote_theme:` for GitHub Pages compatibility
- The `github-pages` gem pins Jekyll and plugin versions to match GitHub's build environment
- Avatar image path is `/assets/images/avatar-placeholder.png` — replace with actual photo
