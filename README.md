# Clean Horizon website: developer handoff

> **Résumé (FR).** Dossier de passage de relais pour le nouveau site Clean Horizon (Astro + Sanity). Il contient le brief et les décisions, le plan du site, les tokens de design, la spec de la page d'accueil bloc par bloc, le contenu en JSON, les schémas Sanity, un squelette Astro qui compile, les assets et les fichiers sources du design. Les points à trancher avant la mise en ligne sont dans `docs/05-open-items.md`. **Gardez ce dépôt privé** : il contient 54 logos clients non validés pour un usage public.

New website for **Clean Horizon**, repositioned as *the intelligence company for energy storage investments*. The site is a sales funnel: lead generation plus proof of expertise.

**Stack:** Astro (static) + Sanity (headless CMS).
**Language:** English.
**Design (hosted, view only):** https://claude.ai/artifact/HKvRtUFPeVbti6sdHemKPk (check the sharing setting before circulating it)

> **Keep this repository private.** `assets/logos` holds 54 client logos that have **not** been cleared for public use, and `docs/05-open-items.md` lists unresolved claims.

## Where to start
1. `docs/00-brief-and-decisions.md`: why the site exists and what is already decided.
2. `docs/03-home-page-spec.md`: the home page, block by block, with its Sanity source and build status.
3. `docs/01-sitemap.md`: all pages, proposed URLs, versions and lots.
4. `docs/04-architecture.md`: Astro and Sanity setup, content model, redirects.
5. `docs/05-open-items.md`: what must be settled before launch.

## Repository layout
```
docs/        brief, sitemap, design system, home spec, architecture, open items
content/     home.json (source of the copy) and home.md (readable)
design/      design source files + asset map
assets/      brand files, images, logos (with manifest)
studio/      Sanity Studio: schemas, desk structure, seed script
web/         Astro site: reference components and data loader
```

## Quick start
```bash
cd web && cp .env.example .env && npm install && npm run dev      # runs on ../content/home.json
cd studio && cp .env.example .env && npm install && npm run dev   # needs a Sanity project id
```
Details in `docs/04-architecture.md`.

## Status
| Area | State |
|---|---|
| Copy for the home page | Final, except square-bracket placeholders listed in `docs/05-open-items.md` |
| Design | Home page (desktop and mobile) and both menus. Other pages not designed. No tablet design |
| Sanity schemas | Home page and shared documents. Type-checked, **not run in a browser** |
| Seed script | Written, **not run against a real project** |
| Astro site | Builds. 5 of 16 home blocks implemented as reference (Hero, LogoMarquee, StoryCards, Pillars, FAQ). The rest are to build from the design |

## Contacts
Marketing director: owner of copy, positioning and sign-offs. (Add names and e-mails here.)
