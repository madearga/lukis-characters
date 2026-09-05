# Contributing a character pack

A pack is one folder, `packs/<name>/`, holding exactly:

- `character.md` — the spec. Required sections: `## Locked design`,
  `## Prompt spec` (one blockquoted paragraph for lukis's CHARACTER prompt
  slot), `## Value rules`. Required metadata lines after `Style:`:
  **`Cutout chroma: green|magenta`** — the pack's cutout screen color
  (`green` for forged/wrought-metal silhouettes, `magenta` otherwise).
  Recommended: `## Personality` and a `Credit: **<Name> by <author>**`
  line near the top. Optional `Aliases:` line (comma-separated subject
  synonyms) so users can say "use gecko" for a pack named `ciko`.
- `reference.png` — the model sheet: one clean, front-facing, full-body
  render on plain paper. This is what the skill passes as `--ref`.
- `preview.png` — one *scene* render where the character performs an idea
  (load-bearing, not posing). Render it conditioned on `reference.png` —
  pass the model sheet as the engine's `--ref`.

Images must be **real PNGs** (convert with `sips -s format png` or
`magick` before committing). Catalog packs must use a **bundled** look —
a custom style can't ship in a pack.

## Steps

1. Fork this repo, create a branch `add-<name>`.
2. Add `packs/<name>/` with the three files above.
3. Append an entry to `index.json` (`name`, `author`, `version`,
   `description`, `style`, optional `aliases`, `cutout_chroma`).
4. Add a row to the README catalog table (copy the Ciko row's format).
5. Open a PR. The preview render is the review artifact.
