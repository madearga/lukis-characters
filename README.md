# lukis-characters

Community **character packs** for [lukis](https://github.com/madearga/lukis-skill/tree/main/skills/lukis) —
the editorial-illustration agent skill. A pack is a recurring mascot: a
written spec (`character.md`) plus a canonical model sheet (`reference.png`)
that keeps the character on-model across every image the skill generates.

The skill ships with **Ciko** (a deadpan house gecko) built in — no pack
needed. This repo is for *additional* characters: install one, set it as
your default, or switch per run.

## Packs

| Pack | In action | Look | Author | What it is |
|---|---|---|---|---|
| [`ciko`](packs/ciko/) | <img src="packs/ciko/preview.png" width="280"> | sablon | I Made Arga Swarsa | A small house gecko (cicak): the quiet regular on the wall. Deadpan patience, showing up, and the work that gets done without announcement. _aka `cicak`, `gecko`, `house-gecko`, `lizard`._ ([model sheet](packs/ciko/reference.png)) |

## Install a pack

```bash
python3 "$SKILL_DIR/scripts/lukis.py" packs list
python3 "$SKILL_DIR/scripts/lukis.py" packs install ciko
```

Installs land in `~/.config/lukis/characters/<name>/`. See the skill's
`references/pack-sharing.md` for the full install, update, and publish flow.

## Contribute a pack

See [CONTRIBUTING.md](CONTRIBUTING.md). A pack is `packs/<name>/` with
`character.md`, `reference.png`, and `preview.png`, plus an `index.json`
entry and a README table row. Open a PR.
