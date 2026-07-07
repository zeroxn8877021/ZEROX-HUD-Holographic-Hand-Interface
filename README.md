# ZEROX HUD — Holographic Hand Interface

A real-time, browser-based AR effect that turns your webcam into a sci-fi holographic
control interface. Open your palm and a rotating holographic panel with a live "sync"
readout appears above your hand, tracked frame-by-frame using computer vision.

## Demo

🔗 **[Live Demo](https://roxn8877021.github.io/zerox-hud/)** *(update this link once hosted — see Hosting section below)*

## Features

- Real-time hand tracking (up to 2 hands) directly in the browser, no install needed
- Holographic HUD panel (spinning rings, energy core, data grid) that spawns from an open palm
- Live sync % readout that charges up/down based on hand gesture
- Cyan tech-skeleton overlay drawn on top of tracked hand landmarks
- Cyberpunk visual layer — scanlines, corner HUD brackets, tint overlay
- Front/back camera switch button, built for mobile use
- Zero build step — a single `index.html` file, works by just opening it in a browser

## How it works

- **MediaPipe Hands** (via CDN) detects 21 landmark points per hand from the live camera feed
- A simple open/closed-hand check drives a "power" value per hand, which fades the HUD panel in and out smoothly
- The HUD panel is positioned every frame using the wrist and knuckle landmark coordinates
- Camera access and front/back switching is handled manually via `getUserMedia`, so the view mirrors correctly depending on which camera is active

## Usage

1. Open `index.html` in a modern mobile or desktop browser (Chrome/Safari recommended)
2. Allow camera access when prompted
3. Open your hand(s) in front of the camera — the HUD will appear and track your palm
4. Tap the camera icon (top-right) to switch between front and back camera

No server, build tools, or dependencies to install — everything loads from CDN.

## Hosting the demo

Since this is a static single-file app, GitHub Pages works well:

1. Push this project to a GitHub repo
2. Enable GitHub Pages on the repo (Settings → Pages → deploy from main branch)
3. Replace the demo link above with your Pages URL

## Credits

Built by **Paras Sharma**, working under the creative and technical brand **Zerox** —
a multi-disciplinary practice spanning game development (Godot 4), web development,
UI/UX design, and prompt engineering.

Part of the wider Zerox ecosystem:
- **Zerox Nocturne** — music label
- **hoshinegai** — visual and aesthetic sub-brand, rooted in dark Japanese aesthetics

Hand tracking powered by [MediaPipe Hands](https://developers.google.com/mediapipe).

## License

Personal / brand project by Zerox. Feel free to remix for your own experiments —
credit appreciated but not required.

