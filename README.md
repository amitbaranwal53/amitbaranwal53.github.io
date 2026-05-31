# amitbaranwal53.github.io

Personal portfolio and blog. Built with [Jekyll](https://jekyllrb.com/) + [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme.

**Live sites:**
- https://amitbaranwal53.github.io (GitHub Pages)
- https://amitbaranwal.edgeone.cool/ (EdgeOne Pages)

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000

## Structure

| Path | Purpose |
|------|---------|
| `_posts/` | Blog posts |
| `_pages/` | Static pages (About, Blog, Projects) |
| `_data/navigation.yml` | Top navigation menu |
| `_config.yml` | Site configuration |
| `assets/images/` | Images |

## Deployment

Push to `main` — both GitHub Pages and EdgeOne Pages deploy automatically.

For EdgeOne, rebuild locally before pushing:
```bash
bundle exec jekyll build
```
