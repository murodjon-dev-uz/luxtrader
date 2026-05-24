# LuxTrader

English · **[Русский](README.md)**

A responsive single-page landing for a luxury goods auction platform — static frontend only, no build step or backend.

| | |
|---|---|
| **Live demo** | [murodjon-dev-uz.github.io/luxtrader](https://murodjon-dev-uz.github.io/luxtrader) |
| **Repository** | [github.com/murodjon-dev-uz/luxtrader](https://github.com/murodjon-dev-uz/luxtrader) |
| **Author** | Murodjon Nuritdinov |
| **Year** | 2023 |

---

## About

**LuxTrader** is an educational portfolio project: the visual layer of a premium auction service. A single HTML page showcases typical marketplace UX — from the hero block through lot listings, categories, services, and editorial sections.

Content targets the luxury segment: watches, jewelry, vehicles, real estate, art, and related categories. All interactive flows (bidding, account, region picker) are **static mockups** — links use `#`, lot data and countdown timers are fixed in markup.

The repository ships production artifacts only (`*.min.css`, `*.min.js`); unminified SCSS/JS sources are not included.

---

## Implementation highlights

- **Three Swiper carousels** — hero (2 slides), featured lots, quotes block with custom controls and decor.
- **Lot cards** — auction timer, current bid in ₽, view and bidder counts, “Raise bid” CTA.
- **Nine-category grid** — icon, background image, SVG decor; followed by copy on the luxury auction market.
- **Services block** — expert appraisal, parts sourcing, repair and restoration.
- **In-page navigation** — `data-goto` / `data-goto-header` with header offset; active section tracking via `data-watch="navigator"`.
- **Responsive layout** — burger menu, user dropdown (region, account, bids, lots), footer copyright repositioned with `data-da` at 767px.
- **Image delivery** — `<picture>` (WebP + PNG/JPG), lazy loading via `data-src` / `data-srcset` with placeholders.
- **Consistent section chrome** — shared `title`, `block-header`, and `block-decor` patterns.
- **SEO & sharing** — meta description, Open Graph, Twitter Card; page language `lang="ru"`.
- **Static asset caching** — version query strings on CSS/JS (`?_v=...`) and favicon (`?v=...`); bump the number in `index.html` when you update a file.

---

## Stack

| Layer | Technologies |
|-------|----------------|
| Markup | HTML5, semantic landmarks |
| Styles | CSS3, BEM-style naming, mobile-first |
| Scripts | Vanilla JS in `app.min.js` (menu, scroll, Swiper, lazy-load, dynamic adapt) |
| Fonts | Self-hosted: BravoRG, Ceremonious One, PF DIN Text Condensed Pro |
| Hosting | GitHub Pages |

No bundler (npm, Vite, Webpack).

---

## Structure

```
luxtrader/
├── index.html
├── css/style.min.css
├── js/app.min.js
├── fonts/
├── img/
├── favicon.ico
└── .github/workflows/cache.yml
```

---

## Quick start

```bash
git clone https://github.com/murodjon-dev-uz/luxtrader.git
cd luxtrader
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Alternative: `npx --yes serve .`

---

## Deployment

Published on **GitHub Pages**:

**https://murodjon-dev-uz.github.io/luxtrader**

Source: [murodjon-dev-uz/luxtrader](https://github.com/murodjon-dev-uz/luxtrader), `main` branch, site root `/`. Bump `?_v=` after CSS/JS changes and `?v=` after favicon changes in `index.html`.

---

## Page sections

| Section | Content |
|---------|---------|
| Header | Logo, anchor nav, region, user menu |
| Hero | Full-width slider, headline, CTA |
| Lots | Lot carousel with timer and metrics |
| Categories | 9 categories + descriptive text |
| Services | Three ancillary service cards |
| Quotes | Quote slider (Mark Twain) |
| Info | News and events columns |
| Footer | Extended links, phone, contact CTA |

---

## Limitations

- No backend, API, or real authentication.
- Links and buttons are placeholders (`href="#"`).
- Layout edits go into minified files or an external source project.

---

## License

© 2023 **Murodjon Nuritdinov**. All rights reserved. Copying, distribution, and commercial use without the author’s permission are prohibited.
