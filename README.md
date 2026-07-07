# Khong Guan Biscuits — Landing Page

A responsive, single-page marketing site for the heritage biscuit brand **Khong Guan** ("Timeless Taste Since 1947"). Built with Bootstrap 5 and a custom CSS theme — no build tooling, no framework, just static HTML and CSS.

> Built as a front-end practice project. Not affiliated with or endorsed by Khong Guan; brand name and imagery are used for educational purposes only.

## Sections

- **Sticky navbar** — brand wordmark (Khong Guan 康元) with a collapsible mobile menu.
- **Hero carousel** — three auto-rotating full-width slides with a gradient overlay and headline copy.
- **Products** — three product cards (Assorted Biscuits, Wafers, Cream Crackers) with a hover-lift effect.
- **Our Story** — heritage copy paired with a stat row (Founded 1947 · 80+ years · 10+ countries).
- **Footer** — brand blurb and quick links.

## Tech stack

| Layer | Tools |
|-------|-------|
| Markup | HTML5 |
| Layout & components | [Bootstrap 5.0.2](https://getbootstrap.com/) (navbar, carousel, cards, grid) — loaded via CDN |
| Styling | Custom CSS with CSS custom properties |
| Fonts | [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) (headings) + [Poppins](https://fonts.google.com/specimen/Poppins) (body), via Google Fonts |

## Project structure

```
Agile-Frontend/
├── index.html        # Full page markup
├── style.css         # Theme, layout, and responsive rules
└── images/
    ├── hero-1.jpg     # Carousel slides
    ├── hero-2.jpg
    ├── hero-3.jpg
    ├── cat-assorted.jpg   # Product card images
    ├── cat-wafer.jpg
    └── cat-crackers.jpg
```

## Running it

No install or build required — it's fully static.

- **Quickest:** open `index.html` directly in a browser.
- **Recommended (avoids any relative-path quirks):** serve the folder, e.g.

  ```bash
  npx serve .
  # or
  python3 -m http.server
  ```

  then visit the printed local URL.

Bootstrap and the fonts load from CDNs, so an internet connection is needed for full styling.

## Design tokens

The theme is driven by CSS variables defined in `style.css`, so re-skinning is a matter of editing four values:

| Variable | Value | Use |
|----------|-------|-----|
| `--kg-red` | `#b5121b` | Brand accent — logo, titles, stats, card headings |
| `--kg-red-dark` | `#8c0e15` | Darker red variant |
| `--kg-cream` | `#f8f1e7` | Section background |
| `--kg-brown` | `#3b2a1f` | Body text and footer background |

Layout adapts at a `992px` breakpoint, scaling up hero height and heading sizes on desktop.

## Known limitations

- **Navigation is visual only.** The navbar and footer links are `<span>` elements rather than anchors, so they don't scroll to or link anywhere. To make them work, convert them to `<a href="#products">` etc. (the sections already have matching `id`s: `home`, `products`, `story`, `contact`).
- **Static content.** All copy and products are hardcoded in the markup; there's no CMS or data layer.
- **Contact section** is a footer only — there's no contact form.

## Possible next steps

- Wire up smooth-scroll navigation using the existing section IDs.
- Add a contact form and basic form handling.
- Self-host Bootstrap and fonts for offline use and faster loads.