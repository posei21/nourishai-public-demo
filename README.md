# NourishAI Public Demo Package

This directory is a release-safe static bundle for a public GitHub Pages demo.

## Contents

- `index.html` and `styles.css` for the public demo page
- Curated screenshot assets (`*.png`) from seeded/demo iOS flows
- `aurora/` theme screenshot pack
- `themes/` cross-theme screenshots for Matcha, Ocean, and TUI
- `.nojekyll` for direct static serving

## Public Safety Boundary

This package is intentionally limited to visual product walkthrough content.

Included:
- Screenshot assets and feature-level product descriptions
- Static HTML/CSS only

Excluded:
- App source code and backend logic
- Secrets, credentials, and internal endpoints
- Internal runbooks, analytics exports, and private docs

## Deploy To GitHub Pages

1. Push this repo with `.github/workflows/public-demo-pages.yml` included.
2. In GitHub repo settings, set **Pages** source to **GitHub Actions**.
3. Run the **Public Demo Pages** workflow (or push changes in this folder to `main`/`master`).
4. Open the published Pages URL from the workflow run summary.

## Optional: Publish From A Separate Public Repo

If you want stronger separation from this private codebase, copy only this folder's contents into a dedicated public repository root and enable GitHub Pages there.

## Preflight Check

Before publishing, confirm this folder has only static/public assets:

```bash
find docs/demo/public_repo -type f | sort
```

Review the output and verify you are only shipping expected `html`, `css`, `md`, `png`, and optional media assets.
