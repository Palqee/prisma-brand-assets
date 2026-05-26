# Palqee Prisma Brand Assets

Public, hot-linkable banners and logos for the [Palqee Prisma](https://docs.palqee.com) Python packages.

## Why this repo exists

The main Prisma repository (`Palqee/prisma-ai`) is private, so image URLs hosted there return 403 when rendered on PyPI, docs sites, or third-party tools. Brand assets live here so they can be referenced from public surfaces (PyPI READMEs, documentation, blog posts) without leaking the source repo.

## Usage

Reference assets via jsDelivr's GitHub CDN. Pin to a tag for stability.

**Prefer SVG** — sharper at any size, no DPR juggling. PyPI and GitHub both render external SVGs via `<img>`.

```markdown
![Palqee Prisma](https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v3.0/prisma/palqee_prisma_banner_dark.svg)
```

PNG is kept as a fallback for tooling that doesn't handle SVG (some doc generators, older renderers).

For light/dark mode support in GitHub-flavored Markdown:

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v3.0/prisma/palqee_prisma_banner_dark.svg">
  <img src="https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v3.0/prisma/palqee_prisma_banner_light.svg" alt="Palqee Prisma" width="1280">
</picture>
```

Always set `width` on the `<img>` — PyPI's `readme-renderer` respects it; SVGs without an explicit width will render at the container width and look oversized.

## Available assets

Each banner ships in both formats (`.svg` preferred, `.png` fallback) and in dark/light variants.

| File (omit extension) | Use |
|---|---|
| `prisma/palqee_prisma_banner_dark` | Main Prisma banner — dark backgrounds |
| `prisma/palqee_prisma_banner_light` | Main Prisma banner — light backgrounds |
| `prisma/palqee_prisma_client_banner_dark` | `palqee-prisma-client` banner — dark |
| `prisma/palqee_prisma_client_banner_light` | `palqee-prisma-client` banner — light |
| `prisma/palqee_prisma_otel_banner_dark` | `palqee-prisma-otel` banner — dark |
| `prisma/palqee_prisma_otel_banner_light` | `palqee-prisma-otel` banner — light |

Canonical aspect ratio: 4:1 (1280×320 viewBox).

## Versioning

URLs should pin a tag (`@v3.0`) rather than `@main`. When assets change in a breaking way (rename, removal), cut a new major tag and update consumers.

| Tag | Notes |
|---|---|
| `@v1` | Initial PNG release (2560×640 / 2560×840) — rendered oversized on PyPI |
| `@v2` | Regenerated PNGs at 1280×320, tighter content |
| `@v3.0` | Added SVG variants alongside PNGs |

## License

© Palqee Ltd. All rights reserved. Assets in this repository are Palqee trademarks and may not be used to identify or promote products that are not affiliated with Palqee.
