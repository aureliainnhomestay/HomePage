# Aurelia Inn HomeStay — Website

A single-page website for Aurelia Inn HomeStay, Varanasi. Static HTML/CSS/JS,
no build step, no dependencies — ready to deploy on GitHub Pages.

## Structure

```
index.html
assets/
  logo.png              Header/footer logo
  hero-banner.jpg        Hero image (Kashi banner)
  camping-bg.jpg          Camping & Campfire section background
  icons/                 Amenity + contact icons (see icons/README.txt)
  decor/                 Decorative brand marks (lotus, calligraphy, skyline watermark)
  rooms/                 Room and lounge photos
```

## Deploying to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Upload `index.html` and the whole `assets/` folder, keeping the same
   folder structure — the page loads everything with relative paths
   (`assets/...`), so nothing else needs configuring.
3. In the repo, go to **Settings → Pages**, set **Source** to the branch
   you pushed to (usually `main`) and folder `/ (root)`, then save.
4. GitHub gives you a URL like `https://<username>.github.io/<repo>/` —
   that's the live site. It can take a minute or two to go live after
   the first push.

## Editing content

Everything is in `index.html` — text, links, and section order are plain
HTML, so any text edit is a direct find-and-replace in the file. A few
things worth knowing:

- **Booking form** — the Google Form is embedded directly (`<iframe>`) in
  the Booking section, with a fallback "open in a new tab" link right
  below it. To point it at a different form, replace both the `src=` on
  the iframe and the `href=` on the fallback link.
- **Map** — the embed and "Get Directions" link both use the property's
  coordinates directly. To move the pin, replace the two coordinate
  numbers in those two `src=`/`href=` attributes.
- **Icons** — see `assets/icons/README.txt`. Filenames are case-sensitive
  on GitHub Pages, so keep exact casing (e.g. `AC.png`, not `ac.png`).
- **Light/dark mode** — the toggle in the header switches a
  `data-theme` attribute; all colors are defined once as CSS variables
  near the top of the `<style>` block, so a color-scheme tweak is a
  one-place edit.
- **Rooms & gallery photos** — swap files in `assets/rooms/` in place
  (same filename) to update a photo without touching the HTML.

## Notes

- No build tools, npm, or server required — it's a static file, so it
  also works by just double-clicking `index.html` to preview locally
  before pushing.
- Total asset weight is a few MB, well within GitHub Pages' limits.
