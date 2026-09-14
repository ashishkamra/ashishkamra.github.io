# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is Ashish Kamra's public profile, served at `https://ashishkamra.github.io`. It is built with Jekyll and GitHub Actions deploys pushes to `master`.

## Local Development

```bash
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

Set `JEKYLL_GITHUB_TOKEN` to a GitHub personal access token if required by the GitHub Metadata plugin during local builds.

## Architecture

Static Jekyll site with no theme — all HTML/CSS is custom. Structure:

- `_layouts/default.html` — single base layout used by all pages
- `_includes/*.html` — one partial per profile section
- `_data/*.yml` — maintainer-edited content files (see below)
- `assets/css/style.css` — all site styles and responsive behavior
- `index.md` — home page; just pulls in all the includes in order

The selected repositories and patents are maintained in `_data/repositories.yml` and `_data/patents.yml`.

## Adding Content

Edit the relevant `_data/` YAML file and push to `master`. The site redeploys within ~1 minute.

### `_data/blog_posts.yml`
```yaml
- title: "Post Title"
  url: https://link-to-post
  date: "2025-01-15"       # YYYY-MM-DD
  summary: "One sentence." # optional
```

### `_data/talks.yml`
YouTube URLs are auto-detected and embedded; all other URLs render as linked cards.
```yaml
- title: "Talk Title"
  url: https://www.youtube.com/watch?v=VIDEO_ID   # or any URL
  speakers: "Name (Org), Name (Org)"
  event: "Conference Name Year"
  date: "2025-11-11"
```

### `_data/repositories.yml`
```yaml
- name: "ProjectName"
  url: https://github.com/org/repo
  description: "One sentence."
  language: "Python"
  focus: "Applied AI"
```
