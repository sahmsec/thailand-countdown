# thailand-countdown

A one-page countdown to the Thailand trip. Static HTML — no build step, no dependencies.

Counts hours / minutes / seconds / milliseconds down to the departure moment
(`2027-04-09T00:00:00+07:00`, Bangkok time). The target is set in one place, in the
`TARGET` constant at the top of the script block in `index.html`.

## Local preview

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Background

Two crops of the same scene, chosen by media query at 560px:

| Screen | Loads | Source |
|---|---|---|
| Wide | `background.jpg` (269 KB) | `background.png` |
| Narrow | `background-phone.jpg` (274 KB) | `background-phone.png` |

The `.png` files are the AI-generated originals; the `.jpg` files are what the page
actually serves, and each `<link rel="preload">` carries a matching `media` attribute so a
phone never downloads the wide one.

A portrait crop exists because scaling the wide image to fill a phone screen crops it on
the horizontal axis only — `background-position`'s Y value is inert there, so no amount of
tuning could bring the whole group into frame.

## Contributors

Name plus one line each, in the `.crew` list near the bottom of `index.html`. No photos —
the list is text only. `.crew ul` is capped at 1020px so the pills wrap into even rows
rather than leaving one stranded on its own line.

## Credits

Typefaces: Baloo 2, Barlow Semi Condensed, and Caveat, served from Google Fonts.