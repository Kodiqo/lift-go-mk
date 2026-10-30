# LiftGoMK

[![Deploy](https://github.com/Kodiqo/lift-go-mk/actions/workflows/deploy-pages.yml/badge.svg)](https://github.com/Kodiqo/lift-go-mk/actions/workflows/deploy-pages.yml)
![Astro](https://img.shields.io/badge/Astro-5-BC52EE?logo=astro&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-06B6D4?logo=tailwindcss&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-strict-3178C6?logo=typescript&logoColor=white)

Macedonian landing site for LiftGoMK, an outdoor lift service for furniture, appliances, moves and renovation materials in Skopje. Built by [Kodiqo](https://github.com/Kodiqo).

## Features

- Static Astro site with Tailwind CSS 4 and strict TypeScript
- Mobile-first layout with iPhone/Safari compatibility work (see `docs/iphone-compatibility.md`)
- Project gallery with a fullscreen media viewer
- Contact and price-request pages with form delivery (see `docs/contact-form.md`)
- SEO: sitemap, `robots.txt`, `llms.txt`, structured metadata (see `docs/seo-audit.md`)
- Non-technical content editing through [Pages CMS](https://pagescms.org/) (see [CMS.md](CMS.md))

## Development

Requires Node.js 22 or newer.

```sh
npm ci
npm run dev        # local dev server
npm run build      # validate content, type check, build to dist/
npm run preview    # serve the production build
```

Content lives in `src/content/site.json`; copy is Macedonian.

## Quality checks

```sh
npm run lint
npm run format:check
npm run test:responsive
npm run test:seo
npm run test:contact
npm run test:viewer
npm run test:performance
npm run test:iphone
```

Most `test:*` scripts use Python 3 and a local Chromium; see `scripts/` and `docs/`.

## Project structure

```
src/
  components/  layouts/  pages/  styles/  scripts/
  content/     editable site content (site.json)
  data/        derived site data
  assets/      optimized images
public/        static files, CMS admin page, uploads
docs/          audits and engineering notes
scripts/       validation and QA scripts
```

## Deployment

`.github/workflows/deploy-pages.yml` builds and publishes the site to GitHub Pages. `astro.config.mjs` reads `SITE_URL` and `BASE_PATH` to override the hosting location.

## Contributing and security

See [CONTRIBUTING.md](CONTRIBUTING.md) and [SECURITY.md](SECURITY.md).
