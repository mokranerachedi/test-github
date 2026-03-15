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

Single `index.html` with three sections:

- **Header** — fixed 64px bar with logo ("siteMe") and Login/Sign-in buttons
- **Main** — centered "Hello World!" hero content
- **Footer** — navigation links and copyright

**Design tokens (inline CSS):**
- Primary: `#845ec2` (purple) — header, footer backgrounds
- Secondary: `#2c73d2` (blue) — Sign in button
- Background: `#e7f3f8` (light cyan)
