# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This is a static HTML/Markdown self-introduction site for Yutaro Koyanagi, published via GitHub Pages at `https://phyu08094.github.io/yutaro/`.

There is no build step, package manager, or test suite — all files are served as-is.

## Structure

```
profiles/
├── index.html          # GitHub Pages homepage (single-page scrollable site)
├── yutaro.md/
│   ├── yutaro.md       # Source Markdown for the self-introduction content
│   └── slideshow.html  # Standalone presentation-style version of the same content
└── README.md
```

`index.html` is the canonical public page. `yutaro.md` is the source of truth for content; when updating personal information, update both `yutaro.md` and reflect the changes in `index.html`.

## Design system

Both HTML files share the same visual language:

- **Colors**: `--gold: #c9a84c`, `--gold-light: #f0d080`, `--gold-dark: #7a5c1e`, `--bg-dark: #0a0a12`
- **Fonts**: Noto Serif JP (headings, display) + Noto Sans JP (body), loaded from Google Fonts
- **Motifs**: animated star background, gold shimmer top bar, corner bracket frames, gradient gold text via `-webkit-background-clip: text`

`index.html` uses IntersectionObserver-based scroll-reveal (`.reveal` → `.visible` class toggle). `slideshow.html` uses a slide deck with keyboard/dot navigation.

## Deployment

Push to `main` — GitHub Pages deploys automatically from the repository root. No CI configuration exists.
