# Krigsvold — Astro starter

A **cloneable, content-neutral Astro project** extracted from the working [krigsvold.org](https://krigsvold.org/) design. Krigsvold retains blue, gold and white, with its distinctive navy, ice-blue, and paper compositions. The original site remains the visual and behavioral reference.

## Clone and run

```bash
git clone https://github.com/krigsvolddesign/astro-starter.git
cd astro-starter
npm ci
npm run dev
```

Edit `src/pages/`, `src/components/`, and `public/`. Then run:

```bash
npm run build
npm run preview
```

The static application builds to `dist/`. Cloudflare can use the ordinary **Build command** `npm run build`, **Root directory** `/`, and **Build output** `dist`. `wrangler.json` is included for optional static Workers hosting. No custom build/deploy scripts are needed.

## Scope

This is a **source-derived working baseline** with placeholder pages, not yet a feature-complete language distribution. Source CSS, the historical Astro/theme packages, and the original Bootstrap/Material Kit foundation are intentionally retained for direct comparison. The work ahead is to extract complete reusable behavior and presentation into Krigsvold Core and Astro, then make this site a clean published-package consumer.

The app currently has four sample routes: `/`, `/article/`, `/document/`, and `/search/`. Core must eventually support these and all the additional canonical examples, dashboards and workspaces without reference-only CSS.

The original source code is `basuhoward/krigsvold.org` at commit `007a4d379e9bd37dee55f86827df6e067ff27335`; see [EXTRACTION-MAP.md](EXTRACTION-MAP.md). Reference content is fictional; the approved Krigsvold ice-shelf panorama replaces the original site hero, with provenance in `public/assets/images/hero/provenance.json`. Retained Material Kit files carry their original license notices.

**Status:** development on `develop`. No release tags, production deployments, or npm publications. A reusable npm site initializer is a separate publication step, not falsely claimed here.

## Identity and imagery

The header, footer, homepage emblem and favicon use the design language's **faceted ice crystal** (`public/assets/mark.svg`), not James Howard's arms or personal `owner.svg`. The approved panoramic ice-shelf artwork comes from the existing Krigsvold Jekyll reference. The language retains blue, gold and white, with navy/ice dominant and gold selectively accented. Sites cloned from this template do not imply affiliation with James Howard or any personal institution.

## Repository roles

This repository was renamed from `site` to `astro-starter`; update existing remotes with `git remote set-url origin https://github.com/krigsvolddesign/astro-starter.git`. Your working directory can keep its existing name.

The full reference application lives at [`krigsvolddesign/astro/reference`](https://github.com/krigsvolddesign/astro/tree/develop/reference), alongside the npm component package. This starter remains an independent clonable application; it is not bundled in the Astro npm package. `website` remains the primary design website.

The starter currently depends on unreleased Core `site.css` via a pinned Git commit. Keep that pin until a Core release exports the extracted site grammar, then update the registry version and lockfile together. Switching to the currently published Core release would remove that required export.
