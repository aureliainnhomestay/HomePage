These are the icon files currently wired into index.html — keep these exact
names (filenames are case-sensitive on GitHub Pages / Linux):

  wifi.png
  AC.png
  bed.png
  parking.png
  location.png
  Leaf.png          (used for "Peaceful Environment")
  group.png         (used for "Family Friendly")
  whatsapp.png
  food.png          (used for "Homely Food (on request)")

If you swap any of these for a new crop, just overwrite the file in place —
no HTML changes needed. If a file is ever missing, that icon slot just goes
blank rather than showing a broken image.

In dark mode, icons are auto-inverted to solid white so they stay visible
against the dark background. If you'd rather keep their original brown/gold
color in dark mode too, remove the ".icon-badge img" filter rule under
[data-theme="dark"] in index.html.
