# Cliploop

Turn a video into a GIF or WebM loop, entirely in the browser. Videos never leave the device.

**Live:** https://awokyaj.github.io/cliploop/

## Features

- Choose a file (MP4, WebM, MOV), drag and drop, film yourself with the webcam (3-2-1 countdown, mirrored self-view), or record your screen
- Trim with a timeline, crop with aspect presets (Free, 1:1, 16:9, 9:16, 4:3)
- Export GIF (per-frame palettes via [gifenc](https://github.com/mattdesl/gifenc)) or WebM (VP9/VP8 via WebCodecs + [webm-muxer](https://github.com/Vanilagy/webm-muxer))
- Side-by-side GIF vs WebM size estimate, presets for email, docs, web loops and sign language

WebM export needs WebCodecs (Chrome, Edge, Firefox). Camera and screen recording need HTTPS or localhost.

## Run locally

No build step. Serve the folder and open http://localhost:5173:

```bash
python3 -m http.server 5173
```

## Files

- `index.html`, `styles.css`: page and styles
- `app.js`: loading, recording, trim, crop, settings, estimates and export
- `encoders.js`: GIF and WebM frame encoders
