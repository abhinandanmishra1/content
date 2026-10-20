# Technical Content & Architecture Essays

The single source of truth for all technical articles, system design deep dives, and architectural research published on [abhinandanmishra.in](https://abhinandanmishra.in).

## Structure

```
content/
├── articles/
│   ├── system-design-approaching-problem.mdx
│   ├── understanding-databases-isolation.mdx
│   ├── system-design-caching.mdx
│   ├── segment-tree-lazy-propagation.mdx
│   ├── react-hooks-deep-dive.mdx
│   ├── building-my-blog.mdx
│   └── mdx-blog-guide.mdx
└── .github/
    └── workflows/
        └── sync-portfolio.yml
```

## How It Works

1. Any changes or new articles added to this repository trigger the `.github/workflows/sync-portfolio.yml` action.
2. The pipeline creates a pull request (or updates the submodule) in [`abhinandanmishra1/portfolio`](https://github.com/abhinandanmishra1/portfolio).
3. Once merged, Vercel automatically deploys the updated content to [abhinandanmishra.in/articles](https://abhinandanmishra.in/articles) with zero cold starts and sub-50ms static delivery.

## Writing Articles

Each article uses standard YAML frontmatter:

```yaml
---
title: "Article Title"
brief: "A concise summary for cards and search metadata"
publishedAt: "2026-10-20T10:00:00Z"
readTimeInMinutes: 10
tags:
  - name: "System Design"
    slug: "system-design"
series:
  name: "System Design"
  slug: "system-design"
author:
  name: "Abhinandan Mishra"
  profilePicture: "https://github.com/abhinandanmishra1.png"
---
```

Both standard Markdown (`.md`) and MDX (`.mdx`) are fully supported.
