# FretFlash — Guitar Fretboard Trainer

A single-page, mobile-friendly guitar fretboard flashcard trainer. Pick a target
string and pitch, get auto-flashing prompts on a metronome cadence, and check
your answers against an interactive 15-fret fretboard with real audio.

No build step, no dependencies to install — just open it in a browser.

## Run it

Option 1 — open directly:

```text
index.html
```

Option 2 — serve locally (recommended, avoids `file://` quirks):

```bash
# Python 3
python -m http.server 8080
# then visit http://localhost:8080
```

## Features

- **3 training modes** — Continuous flash, Recall & Reveal (answer hidden for the
  first half of each interval), Manual advance
- **Flash interval control** — 0.4s–6.0s slider with presets + live BPM readout
- **String isolation** — filter any combination of the 6 strings, with
  Roots E/A, Treble 1–3, and Middle D/G presets
- **Pitch palette** — all 12 chromatic notes, naturals-only, or accidentals-only
- **Sharps / flats toggle** (♯/♭) with enharmonic hints
- **Interactive 15-fret fretboard** — every fret is clickable and plays its true
  pitch via WebAudio; the answer position lights up on the target string
- **Peek / hide answer** (button or `R`), flash-trail history (last 6, clickable
  to review), streak + total counters persisted in `localStorage`
- **Fully responsive** — fluid typography, 44px+ touch targets, swipeable
  fretboard on phones

## Keyboard shortcuts

| Key     | Action          |
| ------- | --------------- |
| `Space` | Next flashcard  |
| `P`     | Start / pause   |
| `R`     | Peek / hide answer |

## Project structure

```text
FretFlash/
├── index.html    # Entire app: markup, Tailwind styling, trainer engine
├── favicon.svg   # Tab icon
└── README.md
```

Styling is [Tailwind CSS](https://tailwindcss.com/) via CDN; fonts are
Inter + JetBrains Mono from Google Fonts. Everything else is vanilla HTML/JS.

## Deploy

Any static host works — drag the folder (or push this repo) to
[GitHub Pages](https://pages.github.com/), Netlify, Vercel, or Cloudflare Pages.
