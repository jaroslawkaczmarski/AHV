# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**AHV — Anonymous Human Verification.** A concept/whitepaper project for a privacy-preserving
"proof of humanity" system that issues anonymous humanity credentials by leveraging existing
government (mObywatel) and bank KYC infrastructure, with a BLIK-style code UX. This repo is
**documentation only** — there is no application code yet. Stage: Proof of Concept (roadmap
starts Q1 2026; EU expansion via eIDAS 2.0 later).

## Contents & commands

Three standalone HTML documents, no build step, no JS, no dependencies:

- `index.html` — Whitepaper (Polish), the GitHub Pages root
- `whitepaper-en.html` — Whitepaper (English)
- `pitch.html` — Pitch deck / one-pager with contact info

```bash
# Preview locally
python3 -m http.server 8000        # → http://localhost:8000  (or open the .html directly)
```

**Hosting:** GitHub Pages at `https://jaroslawkaczmarski.github.io/AHV/`. Pushing to the default
branch publishes; there is no CI or build.

## Conventions

- **Bilingual (PL + EN)** — the PL whitepaper (`index.html`) is the canonical source; keep
  `whitepaper-en.html` in sync when the substance changes.
- All content is self-contained HTML (styles inline / in-file). Edits are prose/markup only.
- License: **MIT** (`LICENSE`). Contact in the docs: `jaroslaw.kaczmarski@outlook.com` — note this
  differs from the `hi@8cells.com` address used by the consultancy site.

## Notes

This is the **least active** repo in the workspace (last substantive change Jan 2026). Treat it
as a living design doc, not a codebase — if real implementation begins, it should likely become a
new project rather than growing inside this docs repo.
