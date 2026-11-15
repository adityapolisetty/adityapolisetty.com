# CLAUDE.md

Personal academic website for Aditya Polisetty (https://adityapolisetty.com), built with Jekyll using the **Academic Pages** theme. `master` holds the full site.

## Current status: site inactive
- Since 2026-11-15 GitHub Pages serves the `coming-soon` branch (a standalone placeholder: `index.html`, identical `404.html`, `CNAME`, `.nojekyll`). `master` is NOT live.
- To reactivate the full site: `gh api -X PUT repos/adityapolisetty/adityapolisetty.com/pages -f "source[branch]=master" -f "source[path]=/"`

## Workflow
- **Always commit and push after making edits.** Pushing to `master` deploys the live site only while Pages serves `master` (see status above).
- Group related edits into a single commit with a clear message.
- Leave the stray leading-whitespace change on line 1 of `_config.yml` alone (pre-existing, unrelated) unless asked to address it.

## Project notes
- Homepage / main content: `_pages/about.md` — sections in order: Work in Progress, Other Research Work, Teaching, Research Assistance, Other Experience, Education.
- Header navigation: `_data/navigation.yml`.
- Publications collection: `_publications/` (rendered at `/publications/`).
- Fonts and colors: `_sass/_themes.scss` (font variables; site uses **Source Sans Pro** loaded via Google Fonts in `_includes/head.html`) and the theme skins `_sass/theme/_default_light.scss` / `_sass/theme/_default_dark.scss` (link/accent colors — currently **Oxford Navy**). Active theme is "default" (set in `_config.yml`).
- No local Ruby/Jekyll on this machine — rely on GitHub Pages to build (or Docker via `docker-compose.yaml`). SCSS under `_sass/` is compiled server-side at build time.
