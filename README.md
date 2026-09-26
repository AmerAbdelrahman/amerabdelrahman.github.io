# amerabdelrahman.github.io

Personal site of Abdelrahman Amer. Plain static HTML — no Jekyll, no build step, no
dependencies: three pages, one stylesheet, one small script.

Live at https://amerabdelrahman.github.io, served by GitHub Pages from `main` at the
repository root.

```
index.html              About / landing         published at /
research/index.html     Working papers + WIP    published at /research/
teaching/index.html     Courses                 published at /teaching/
assets/css/style.css
assets/js/main.js       Theme toggle, mobile nav
assets/img/portrait.jpg
assets/pdf/             CV, JMP, ACV, AHT slides
.nojekyll               serve files as-is, skip the Jekyll build
```

Each page sits in its own directory so the published URLs match the ones the previous
site served. Inside `research/` and `teaching/` every relative path is prefixed with
`../` — keep that in mind when adding links or assets to those two files.

## Design

Warm ivory ground (`#faf9f5`), near-black ink (`#141413`), clay accent (`#d97757`),
Lora for text and Poppins for UI labels. Light and dark themes; the toggle sits in the
nav and persists in `localStorage`.

## Viewing locally

Serve it — don't open the files from Finder. Over `file://` a nav link to `research/`
opens a directory listing instead of the page:

```sh
python3 -m http.server 8000    # then http://localhost:8000
```

## Publishing

```sh
git add -A && git commit -m "describe the change"
git push
```

Pages rebuilds in a minute or two. The CDN caches for ten minutes, so hard-refresh
(Cmd-Shift-R) before concluding that something did not deploy.

## History

This replaced an al-folio Jekyll site in September 2026. Two notes from that migration:

- the CV is published as `assets/pdf/AmerAbdelrahman_CV.pdf`. The old site served it as
  `AmerAbdelrahman_CV2.pdf`, which now returns 404; restore that filename if an old
  application link needs to keep working;
- the portrait is a 675x900 resize at `assets/img/portrait.jpg`. The old 3024x4032
  original lived at `assets/img/my_photo4.jpg` and is no longer published.

The complete old repository — both branches, all 54 commits, plus those two dropped
files — is backed up outside this repo in `~/Projects/site-backup/`.
