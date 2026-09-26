# amerabdelrahman.github.io — redesign

A plain static rebuild of the personal site. No Jekyll, no build step, no dependencies —
three HTML files, one stylesheet, one small script.

```
index.html          About / landing (JMP featured, selected work, contact)
research.html       Working papers + work in progress
teaching.html       TA courses
assets/css/style.css
assets/js/main.js   Theme toggle, mobile nav, scroll reveal
assets/img/portrait.jpg
assets/pdf/         CV, JMP, ACV, AHT slides (pulled from the live site)
```

## Design

Palette and typography follow Anthropic's house style: warm ivory ground (`#faf9f5`),
near-black ink (`#141413`), clay accent (`#d97757`), Lora for text and Poppins for UI
labels. Light and dark themes; the toggle sits in the nav and persists in `localStorage`.

All content — abstracts, coauthors, links, course list — was taken verbatim from the
current live site.

## Viewing

Open `index.html` directly, or serve it:

```sh
python3 -m http.server 8000    # then http://localhost:8000
```

## If you want to deploy it later

Copy these files to the root of the `amerabdelrahman.github.io` repo, replacing the
al-folio Jekyll source. Two things to change first, since GitHub Pages serves the
old site at `/research/` and `/teaching/` (directories, not `.html` files):

- either keep the `.html` links as they are and accept the new URLs
  (`/research.html`), which breaks old inbound links, or
- move each page into its own directory (`research/index.html`, `teaching/index.html`)
  and rewrite the relative asset paths to `../assets/...` to preserve the old URLs.

Nothing has been deployed.
