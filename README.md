# ashishkamra.github.io

Source for the Ashish Kamra's github pages site (https://ashishkamra.github.io).
## Local development

```bash
bundle install
JEKYLL_GITHUB_TOKEN=<your-pat> bundle exec jekyll serve
# Visit http://localhost:4000
```

A personal access token may be required by the GitHub Metadata plugin during local builds.

## Adding content

All content is managed through YAML files in `_data/`. Push to `master` and the site redeploys within ~1 minute.

| File | Content |
|------|---------|
| `_data/blog_posts.yml` | Blog posts |
| `_data/talks.yml` | Conference talks (YouTube URLs are auto-embedded) |
| `_data/publications.yml` | Academic publications |
| `_data/repositories.yml` | Selected GitHub repositories |
| `_data/patents.yml` | Patents and applications |

See [CLAUDE.md](CLAUDE.md) for field definitions and examples.
