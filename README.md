# Speed Reader

A distraction-free speed reading app using the RSVP (Rapid Serial Visual Presentation) technique. Words flash one at a time with the Optimal Recognition Point highlighted in red, so your eyes stay fixed and your brain does less work per word.

Black background, white words, red pivot letter. Installs as a standalone app on phone and desktop. Works offline.

**[Live demo →](https://hristiyanminev.github.io/Speed-Reading-Tool/)**

## Features

- **RSVP display** with optimal recognition point highlighting
- **Adjustable speed** from 100 to 1,000 words per minute
- **Adjustable font size** for comfortable reading at any distance
- **Fullscreen mode** with auto-hiding controls — mouse stops moving, UI fades away
- **Keyboard controls** — space to play/pause, arrows to step and adjust speed, F for fullscreen
- **Persistent state** — your text, speed, and reading position are remembered between sessions
- **Installable PWA** — add to home screen on mobile, install as app on desktop
- **Fully offline** after first visit

## How to use

1. Paste any text into the box — article, book chapter, notes, anything.
2. Hit **Play** (or press space).
3. Adjust speed with the slider or arrow keys.
4. Click the fullscreen icon (or press **F**) for distraction-free reading.

The red letter in each word is the Optimal Recognition Point — the spot your eyes naturally fixate on. Look there, and peripheral vision handles the rest. That's what makes RSVP faster than conventional reading: your eyes never have to move.

### Keyboard shortcuts

| Key | Action |
|---|---|
| `Space` | Play / pause |
| `← →` | Step one word back / forward |
| `↑ ↓` | Increase / decrease speed |
| `F` | Toggle fullscreen |
| `Esc` | Exit fullscreen |

### Speed guide

- **200–250 wpm** — average silent reading speed
- **300 wpm** — comfortable RSVP starting point
- **400–500 wpm** — sustainable with practice
- **600+ wpm** — requires training; comprehension varies

## Tech

Plain HTML, CSS, and vanilla JavaScript. No build step, no dependencies, no framework. Single-page PWA with a service worker for offline caching and a manifest for installability.

Files:

```
index.html       # the entire app
manifest.json    # PWA metadata (name, icons, display mode)
sw.js            # service worker — caches assets for offline use
icon-192.png     # app icon (home screen, etc.)
icon-512.png     # app icon (higher resolution)
```

## Running locally

Because the service worker requires a proper HTTP origin (not `file://`), you'll need to serve the folder rather than double-clicking `index.html`.

```bash
# Python 3 (comes preinstalled on most systems)
python3 -m http.server 8000

# or Node, if you have it
npx serve

# then open
http://localhost:8000
```
## Installing as an app

- **iPhone/iPad (Safari):** Share button → *Add to Home Screen*
- **Android (Chrome):** menu → *Install app*
- **Desktop (Chrome, Edge):** install icon in the address bar

Once installed, the app opens in its own window with no browser chrome, works offline, and remembers your last session.

## Browser support

Modern versions of Chrome, Edge, Safari, and Firefox. Service workers and the Fullscreen API are required for the full experience — both have been widely supported since 2018.

## A note on speed reading

RSVP genuinely works for faster *reading*, but comprehension at very high speeds depends heavily on the material and your familiarity with it. Dense academic or technical text is still best read at a pace that lets you stop and think. Treat the speed slider as a tool, not a competition.

## License

MIT — do what you like.
