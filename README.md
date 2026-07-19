# minturn-financial

Public **demo** template sources for [Paperglyph](https://paperglyph.com). Minturn Financial is a
fictional bank whose customer-facing deposit documents are authored here in git and governed on the
platform — the story the live demo at [paperglyph.com/demo](https://paperglyph.com/demo) tells.

This repo is the **source of truth** for its templates, fixtures, and assets. Merges to `main` sync to
DRAFT versions on the platform via native git sync (Business plan); review, approval, and publishing stay
human steps in the dashboard. Sync is one-way — git to platform.

## Layout

```
paperglyph.toml     # manifest: [[templates]] key→file + [[assets]] key→file
templates/          # Handlebars sources, one file per template key
fixtures/<key>/     # named sample datasets per template (Default.json)
assets/             # referenced files; keys declared in the manifest
```

Each template renders a paged document — a deposit rate sheet, a multi-page portfolio statement, a
compliance handbook with a cover and table of contents, and a full-bleed certificate — through
Paperglyph's paged-CSS rendering engine.
