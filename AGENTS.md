# BitTheCat — agent guide

This repository hosts the **BitTheCat** theme for multiple applications, all built
from a single shared palette.

## Source of truth

Every color comes from the base palettes:

- `src/palette-dark.json`
- `src/palette-light.json`

Each file groups colors by area: `ui`, `terminal`, `syntax`, `status`,
`accents`, `players`.

## Rules

- **Use only palette colors.** Do not invent new hex values — pick the closest
  existing token. If a new color is genuinely needed, add it to both palettes
  first.
- **One folder per application** (`zed/`, `sublime/`, …). Each folder is
  self-contained and follows that application's format.
- **Keep dark and light in sync**: the same roles must exist in both palettes.
- **Map by role, not by value.** Examples:
  - `ui.background` / `ui.editor.background` → text area background
  - `ui.text` / `ui.text.muted` → foreground / muted text
  - `ui.text.accent` → accent (caret, active tab, links)
  - `syntax.*` → syntax scopes (keyword, string, function, type, comment…)
  - `terminal.ansi.*` → terminal ANSI colors
  - `status.*` → git / status colors (added, modified, deleted, error…)
  - `accents` / `players` → git graph and collaborative cursors
- **Don't hardcode** a color that already exists as a palette token.

## Adding a new application

1. Read `src/palette-dark.json` and `src/palette-light.json`.
2. Create `<application>/` and translate the palette into that application's theme format.
3. Reuse the same role names so the palettes stay the reference.

## Application formats

- `zed/` — Zed extension (`extension.toml`, `themes/bitthecat.json`).
- `sublime/` — Sublime Text color schemes (`.sublime-color-scheme`).
