# OpenJournal

[![GitHub Pages](https://github.com/frankstop/OpenJournal/actions/workflows/pages.yml/badge.svg)](https://github.com/frankstop/OpenJournal/actions/workflows/pages.yml)
[![pages-build-deployment](https://github.com/frankstop/OpenJournal/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/frankstop/OpenJournal/actions/workflows/pages/pages-build-deployment)
[![GitHub last commit](https://img.shields.io/github/last-commit/frankstop/OpenJournal)](https://github.com/frankstop/OpenJournal/commits/main)
[![GitHub repo size](https://img.shields.io/github/repo-size/frankstop/OpenJournal)](https://github.com/frankstop/OpenJournal)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

OpenJournal is a public journal site for accomplishments, experiments, practice, and work kept moving.

Live site: https://frankstop.github.io/OpenJournal/

## Purpose

OpenJournal is meant for public consumption, not private diary storage. It gives short entries a clear place to live, then lets those entries connect later when patterns show up.

Current direction:

- pastel storybook style
- tiny adventure map mood
- entries as public map stops
- badge table for filtering
- full entry pages with summary, two sentences, what happened, artifact, and post links

## Features

- Mobile-first static site.
- GitHub Pages deployment from `main`.
- Badge table with multi-select AND filtering.
- Add badge UI stored in `localStorage`.
- Three starter entries from current OpenJournal planning chat.
- Hash-routed entry pages, so links work on GitHub Pages.
- In-post link cards for related entries.
- No framework or build step.

## Repo Shape

```text
.
├── .github/workflows/pages.yml
├── index.html
├── LICENSE
├── README.md
└── .nojekyll
```

## Local Run

Open `index.html` directly, or run:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Deploy

Push to `main`. GitHub Actions deploys root static files to GitHub Pages.

Manual check:

```bash
gh run list --repo frankstop/OpenJournal --workflow pages.yml
gh api repos/frankstop/OpenJournal/pages
```

## Notes

This is intentionally static. Future entries can be added by editing the `entries` array in `index.html`.
