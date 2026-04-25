# Hermes CRT Terminal Themes

Two drop-in dashboard themes for [Hermes Agent](https://github.com/NousResearch/hermes-agent) that transform the web dashboard into an authentic CRT phosphor monitor experience.

## Themes

### 🟠 CRT Amber
Classic warm amber phosphor — modeled after the IBM 5151 monitor and DEC VT100 terminals. The original monochrome display color, warmer and easier on the eyes than green.

### 🟢 CRT Green  
Classic green phosphor — the iconic hacker terminal look (Apple II, early UNIX terminals, The Matrix). Brighter and more vivid than amber.

## What Makes These Different

These aren't simple color swaps. Each theme includes:

- **Horizontal scanlines** — Every-other-row darkening at 3px pitch via `body::after` pseudo-element with multiply blend mode
- **CRT vignette** — Radial gradient simulating the curved screen edge shadow of a real CRT
- **Phosphor text glow** — `text-shadow` on headings and interactive elements that mimics light bleeding into surrounding phosphor
- **Screen flicker** — Subtle CSS animation on `<html>` creating imperceptible micro-variation — the "breathing" quality of a real CRT
- **Monospace typography** — IBM Plex Mono for body, VT323 for display (pixel-perfect 80s terminal font)
- **Sharp corners** — `radius: 0`, `density: compact` — CRTs don't do rounded UI
- **Phosphor-colored scrollbars, caret, and text selection**

## How They Compare

| Feature | Built-in Cyberpunk | CRT Amber/Green |
|---------|-------------------|-----------------|
| Font | Share Tech Mono | IBM Plex Mono + VT323 |
| Color style | Neon green (#9bffcf) | Authentic phosphor (amber #ffb74d / green #6aff7e) |
| Scanlines | Cockpit-only | Always visible |
| CRT vignette | None | Radial gradient edge shadow |
| Flicker | None | Subtle 3s animation |
| Text glow | None | text-shadow phosphor bloom |
| Custom scrollbar | None | Phosphor-tinted thin scrollbar |

## Installation

```bash
# Copy theme files to your Hermes dashboard themes directory
mkdir -p ~/.hermes/dashboard-themes
cp crt-amber.yaml ~/.hermes/dashboard-themes/
cp crt-green.yaml ~/.hermes/dashboard-themes/

# Refresh the dashboard (or restart if needed)
hermes dashboard
```

Then open the dashboard, click the palette icon in the header bar, and select "CRT Amber" or "CRT Green" from the theme switcher.

## Requirements

- Hermes Agent with the web dashboard running (`hermes dashboard`)
- The dashboard auto-discovers `.yaml` files in `~/.hermes/dashboard-themes/`
- No build step, no npm, no dependencies — pure YAML + CSS

## License

MIT — use freely, modify, share. Built for the Hermes Dashboard Themes & Plugins hackathon.
