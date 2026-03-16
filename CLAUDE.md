# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page website called "siteMe" — no build step, no dependencies, no framework. The single `index.html` contains all HTML and inline CSS.

## Development

Open `index.html` directly in a browser, or serve with any static file server:

```bash
python -m http.server 8080
```

## Architecture

Single `index.html` with five sections:

- **Header** — sticky 68px bar with logo ("siteMe") and Login/Sign-in buttons
- **Hero** — two-column grid: editorial headline + hero graphic with badge
- **Features** — three-column grid (Design / Publish / Grow)
- **Footer** — logo, tagline, nav links, copyright

**Fonts (Google Fonts — external dependency):**
- `Bebas Neue` — display/headings
- `Lora` — body text, buttons (italic variant used)

**Design tokens (CSS custom properties in `:root`):**
- `--ink: #1a1714` — dark near-black; header, footer backgrounds, body text
- `--cream: #faf7f2` — off-white; page background, text on dark
- `--vermillion: #e8462a` — accent red; CTAs, highlights
- `--yellow: #f5c842` — secondary accent; graphic tag

**Gotchas:**
- Buttons use `clip-path: polygon(...)` for the parallelogram shape — don't use `border-radius` on them
- Responsive breakpoint at `860px` flips hero to single-column and features to stacked
