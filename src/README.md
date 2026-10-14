# Base palettes

The two base palettes of the theme:

- `palette-dark.json` — BitTheCat Dark
- `palette-light.json` — BitTheCat Light

Each file lists every color of the theme, grouped by area:

| Key | Content |
|---|---|
| `ui` | interface colors (backgrounds, borders, text, tabs, editor chrome, scrollbars…) |
| `terminal` | `terminal.*` (background/foreground + the 16 ANSI colors, normal/bright/dim) |
| `syntax` | `syntax.*` token → color |
| `status` | git/status colors (`created`, `modified`, `deleted`, `error`, `warning`…) |
| `accents` | the 10-element accents array (git graph + collaboration order) |
| `players` | the 10 collaborative cursors |

They are meant to be read and copied: change the hex values to build new
themes or variants.
