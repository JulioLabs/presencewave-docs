# PresenceWave Docs

User documentation for PresenceWave, published at **https://docs.presencewave.com**.

A Hugo site with its own small layout (no theme). Every push to `main` builds it and deploys it to GitHub Pages (`.github/workflows/hugo.yml`); `static/CNAME` holds the custom domain.

## Writing pages

- One folder per section under `content/` (`getting-started`, `billing`, `domains`, `widgets`, `services`, `reference`). The sidebar lists the sections from `[[menu.main]]` in `hugo.toml` and the pages inside each section by `weight`.
- A page is a markdown file with `title`, `description` and `weight` in its front matter. Add `draft: true` until it's ready: drafts are not published.
- One task per page: what it is, when you'd use it, the steps (with screenshots in the page's folder), limits and billing impact, then troubleshooting.
- Link to the pricing page instead of repeating prices.

## Running it locally

```bash
hugo server -D        # http://localhost:1313, drafts included
hugo --minify         # build into public/
```

## Search engines

`noindex = true` in `hugo.toml` keeps the site out of search results while it's a skeleton. Set it to `false` when the first real pages are published.
