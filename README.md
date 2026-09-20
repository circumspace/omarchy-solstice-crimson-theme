# Solstice — Crimson

An Omarchy theme built on the **original Solaris CDE "Crimson" palette**
(`Crimson.dp`): grey-lavender chrome, warm cream canvas, rose selection
accent, and Crimson's signature **steel blue** for troughs, recessed
surfaces, and inactive borders.

Every core color is byte-exact from the 48-bit original palette. The
distinguishing steel slot (`#718BA5`) is the only place the original CDE
`Crimson.dp` differs from `Solyaris.dp` — this theme is that difference.
See [Solstice Daylight](https://github.com/circumspace/omarchy-solstice-daylight-theme)
for the `Solyaris.dp` skeleton and
[Solstice Nightwatch](https://github.com/circumspace/omarchy-solstice-nightwatch-theme)
for the dark companion.

## Preview

![Solstice Crimson](screenshots/crimson.png)

## Install

```bash
omarchy theme install https://github.com/circumspace/omarchy-solstice-crimson-theme
```

Then select **Solstice Crimson** from the Omarchy theme picker.

Or manually:

```bash
git clone https://github.com/circumspace/omarchy-solstice-crimson-theme \
  ~/.config/omarchy/themes/solstice-crimson
```

## Palette

| Role | Hex | Source |
|------|-----|--------|
| Chrome (panels, bars) | `#AEB2C3` | `Crimson.dp` slot 2, exact |
| Canvas (terminal, docs) | `#FFF7E9` | `Crimson.dp` slot 4, exact |
| Steel (troughs, recessed) | `#718BA5` | `Crimson.dp` slot 3, exact |
| Rose (selection, active) | `#B24D7A` | `Crimson.dp` slot 1, exact |
| Ink (foreground) | `#000000` | Motif fg on chrome |

Full provenance in [`palette.txt`](palette.txt).

## What's themed

- **Hyprland** — rose active border (`#B24D7A`), steel inactive border.
- **GTK 3 / GTK 4** — chrome + rose selection overrides; sharp CDE corners
  (`border-radius: 0`). GTK loads user CSS once at startup, so **restart** GTK
  apps after switching *into or out of* this theme for colors to take.
- **Terminal** — Ghostty / Alacritty / Kitty / foot palettes generated from
  `colors.toml`; terminals sit on the cream canvas with WCAG-checked accents.
- **Browser chrome** — `chromium.theme` tints Brave/Chromium/Edge frame color
  (light tones are handled via Chromium's MD3 palette; expect subtle results).
- **Neovim** — self-contained `neovim.lua` colorscheme (no plugin dependency).
- **btop, Zed/VS Code, Helix** — generated from `colors.toml`.

## Wallpapers

Fourteen procedurally-generated backdrops in `backgrounds/` (6K, downscale
cleanly), rendered from [NsCDE](https://github.com/NsCDE/NsCDE) XPM tile
patterns with the Motif colorset derived from this palette's chrome
(`bg #AEB2C3`, `ts #DDDEE6`, `bs #5E606A`, `sel #9497A6`): **Solyaris, Dimple,
Dune, Swirl, Squares, Marble, Toronto, SandLight, CircuitBoards, Lattice,
Concave, Convex, PinStripe, Bark**. Regenerate with
[circumspace/scripts `gen-cde-wallpapers`](https://github.com/circumspace/scripts).

## License

MIT — see [LICENSE](LICENSE).
