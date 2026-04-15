# sarmadchandio.com

Static, single-page personal site. No build step — just HTML + CSS.

## Structure

```
.
├── index.html              single-page scroll layout
├── CNAME                   custom domain (sarmadchandio.com)
├── .nojekyll               tells GitHub Pages to skip Jekyll
├── files/CV.pdf
└── assets/
    ├── css/style.css       all styling (CSS variables for theming)
    ├── icons/03-star.svg   site favicon
    └── images/
        ├── profile.png
        └── papers/         one SVG per publication
```

## Local preview

```bash
python -m http.server 8000
# → http://localhost:8000
```

Or just open `index.html` in a browser.

## Editing

- **Bio / sections / publications** → edit `index.html` directly. Each section is wrapped in `<section id="...">` with semantic class names.
- **Colors / fonts / spacing** → tweak the CSS variables at the top of `assets/css/style.css` (`:root { --bg: ...; --accent: ...; }`).
- **Add a publication** → duplicate any `<article class="pub">` block in the Research section. Add a matching SVG to `assets/images/papers/` and a new `<a class="waterfall__item">` in the side rail.
- **Swap the portrait** → replace `assets/images/profile.png` (square crop, ~400×400 ideal).

## Deployment

Pushed to GitHub on `master`. **Settings → Pages → Source: `Deploy from a branch`, Branch: `master`, Folder: `/`.** The `CNAME` and `.nojekyll` files at the repo root do the rest.
