# Palqee Prisma Brand Assets

Public, hot-linkable banners and logos for the [Palqee Prisma](https://docs.palqee.com) Python packages.

## Why this repo exists

The main Prisma repository (`Palqee/prisma-ai`) is private, so image URLs hosted there return 403 when rendered on PyPI, docs sites, or third-party tools. Brand assets live here so they can be referenced from public surfaces (PyPI READMEs, documentation, blog posts) without leaking the source repo.

## Usage

Reference assets via jsDelivr's GitHub CDN. Pin to a tag for stability.

```markdown
![Palqee Prisma](https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v2/prisma/palqee_prisma_banner_dark.png)
```

For light/dark mode support in GitHub-flavored Markdown:

```markdown
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v2/prisma/palqee_prisma_banner_dark.png">
  <img src="https://cdn.jsdelivr.net/gh/Palqee/prisma-brand-assets@v2/prisma/palqee_prisma_banner_light.png" alt="Palqee Prisma">
</picture>
```

## Available assets

| File | Use |
|---|---|
| `prisma/palqee_prisma_banner_dark.png` | Main Prisma banner — dark backgrounds |
| `prisma/palqee_prisma_banner_light.png` | Main Prisma banner — light backgrounds |
| `prisma/palqee_prisma_client_banner_dark.png` | `palqee-prisma-client` banner — dark |
| `prisma/palqee_prisma_client_banner_light.png` | `palqee-prisma-client` banner — light |
| `prisma/palqee_prisma_otel_banner_dark.png` | `palqee-prisma-otel` banner — dark |
| `prisma/palqee_prisma_otel_banner_light.png` | `palqee-prisma-otel` banner — light |

## Versioning

URLs should pin a tag (`@v2`) rather than `@main`. When assets change in a breaking way (rename, removal), cut a new major tag and update consumers.

## License

© Palqee Ltd. All rights reserved. Assets in this repository are Palqee trademarks and may not be used to identify or promote products that are not affiliated with Palqee.
