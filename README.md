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

`assets/background.png` is the AI-generated original. `assets/background.jpg` is the
compressed copy the page actually loads (2.3 MB -> 269 KB); regenerate it after replacing
the source. Framing is controlled by `background-position` on `.photo` — `center 58%`
keeps the stack of textbooks in frame along the bottom edge.

## Contributors

Name plus one line each, in the `.crew` list near the bottom of `index.html`. No photos —
the list is text only. `.crew ul` is capped at 1020px so the pills wrap into even rows
rather than leaving one stranded on its own line.

## Credits

Typefaces: Baloo 2, Barlow Semi Condensed, and Caveat, served from Google Fonts.