# 西格莉卡 / Sigrika Codex Pet

Codex-compatible animated pet package for 西格莉卡 (Sigrika).

## Files

- `pet.json` - Codex pet metadata.
- `spritesheet.webp` - Final 1536x1872 animated pet atlas.
- `qa/contact-sheet.png` - Visual contact sheet for all animation rows.
- `qa/validation.json` - Atlas validation output.
- `qa/review.json` - Frame inspection output.
- `qa/previews/*.gif` - Per-state animation previews.

## Install

Copy this folder to:

```text
%USERPROFILE%\.codex\pets\sigrika
```

The required runtime files are:

```text
pet.json
spritesheet.webp
```

## QA

Generated with the hatch-pet workflow.

- `validation.json`: ok
- `review.json`: ok
- Atlas size: 1536x1872
- Cell size: 192x208
- States: idle, running-right, running-left, waving, jumping, failed, waiting, running, review
