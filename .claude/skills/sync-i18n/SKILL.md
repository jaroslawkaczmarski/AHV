---
name: sync-i18n
description: Keep AHV's Polish and English whitepapers in sync — propagate substantive changes from the canonical PL whitepaper (index.html) into the EN one (whitepaper-en.html), and flag drift between them. Use when the user runs `/sync-i18n` or edits the AHV whitepaper content and wants both languages aligned.
disable-model-invocation: true
---

# /sync-i18n

AHV ships two whitepapers: **`index.html` (Polish, canonical)** and
**`whitepaper-en.html` (English)**. `pitch.html` is Polish-only. This skill keeps the EN
whitepaper aligned with the PL one when the substance changes.

## Args

```
/sync-i18n              # diff PL vs EN, report drift, then apply pending PL changes to EN
/sync-i18n check        # report drift only, don't edit
```

## Workflow

1. **Treat `index.html` (PL) as the source of truth.** Compare its section structure (headings,
   ordering, diagrams, numbers, links) against `whitepaper-en.html`.
2. **Report drift:** sections present in one language but not the other, changed figures/roadmap
   dates, or stale claims. List them before editing.
3. **Propagate** the pending substantive changes from PL into EN as a faithful **translation**
   (not a literal word swap) — match technical terms already used in the EN file. Keep markup,
   ids, and asset references identical so both render the same.
4. **Don't touch** content that is intentionally language-specific (e.g. PL-only legal/contact
   phrasing); call it out instead of forcing a mirror.
5. **Report** what was synced and any remaining manual decisions.
