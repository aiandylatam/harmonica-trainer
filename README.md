# Harmonica Trainer

Practice tool for chromatic harmonica players (Hohner-style 12 / 14 / 16 hole, key of C, Solo tuning).

**Live demo:** https://aiandylatam.github.io/harmonica-trainer/

## What it does

Three things on one page:

1. **Scales mode** — pick a key + scale and see exactly which holes / blow-draw / slider combinations belong to it on the harmonica diagram, plus the same notes on a treble-clef staff.
2. **Tabs mode** — click holes on the harmonica to build a tab sequence, edit/play/step through it, save it, and parse text-format tabs like `1B 2D 3B* 4D`.
3. **Live pitch detection** — microphone "Listen" mode highlights the currently-played note in real time on both the harmonica and the staff (cents-accurate tuner included).

## Features

- **12 / 14 / 16 hole layouts** — Hohner 270, Chrometta 14, Super 64, etc.
- **Adjustable A4 reference pitch** (415–466 Hz, presets at 440–444 for orchestral tuning)
- **Scale degrees** shown on every in-scale note (1, ♭3, ♯4, etc.)
- **13 scales** — Major, natural/harmonic/melodic minor, pentatonics, blues, all church modes, chromatic
- **Save & load tabs** to localStorage
- **Light theme** with adjustable accent color and density
- **Persistent preferences** across sessions

## Tech

Single standalone `index.html`. Vanilla JS, no build step. Web Audio API for synthesis and microphone pitch detection (autocorrelation, ACF2+). SVG for the staff. Google Fonts for Space Grotesk + JetBrains Mono + Noto Music.

## Local dev

Just open `index.html` in a browser. For microphone access you need HTTPS or `localhost` — `file://` is blocked by some browsers.

```bash
# quick local server
python -m http.server 8000
# → http://localhost:8000
```

## Credits

Visual design by Anthropic Claude Design (April 2026 release).
