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

Two crops of the same illustration, chosen by media query at 560px:

| Screen | Serves | Source art |
|---|---|---|
| Wide | `bg-desktop.jpg` (431 KB) | `bg-desktop.png` |
| Narrow | `bg-mobile.jpg` (409 KB) | `bg-mobile.png` |

`og.jpg` is cropped from `bg-desktop.png` to the 1.91:1 that Facebook and WhatsApp
expect, weighted to keep the standing pair's heads rather than centring the trim.
Re-encode all three whenever the source art changes.

A separate portrait crop exists because scaling the wide art to fill a phone screen
crops it on the horizontal axis only — `background-position`'s Y value is inert there,
so no amount of tuning brings the whole group into frame.

## Motion

- **Flocks of birds** cross the sky — three groups, each a loose V with jitter, drifting
  at different speeds. Silhouettes are near-black with a warm `drop-shadow` halo so they
  stay visible over both the bright sunset and the dark treeline.
- **Stars orbit the sleepers.** `.zzz--a` / `.zzz--b` are absolutely positioned over the
  two passed-out figures, and the coordinates differ per breakpoint because the two crops
  frame them differently. Reposition both if the art changes.
## Contributors

Name plus one line each, in the `.crew` list near the bottom of `index.html`. No photos —
the list is text only. `.crew ul` is capped at 1020px so the pills wrap into even rows
rather than leaving one stranded on its own line.

## Credits

Typefaces: Baloo 2, Barlow Semi Condensed, and Caveat, served from Google Fonts.