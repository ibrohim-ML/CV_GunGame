# CV GunGame — Hand Tracking Aim Trainer

A browser-based aim trainer where you shoot targets using nothing but your index finger. No mouse, no keyboard — just your hand and a webcam.

Built with MediaPipe Hands for real-time finger tracking, this game turns your index finger into a crosshair and a quick upward flick into a shot.

---

## Gameplay

- **Move** — point your index finger anywhere on screen
- **Shoot** — flick your finger upward quickly
- **Score** — hit targets to gain points and increase game speed
- **Speed scales with score** — every 5 points, the multiplier goes up by 0.1x (max 3.0x)

Each missed target that escapes off-screen costs nothing, but the pace keeps accelerating as you score.

---

## Target System

Targets come in 5 visual variants with randomized palettes:

- Holographic rings
- Bullseye with concentric circles
- Dashed reticle patterns
- Multi-layer glow targets
- Aura-ring hybrids

Each target has a pulsing animation, particle burst on hit, shockwave ripple, and optional screen shake feedback.

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Hand tracking | [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) |
| Rendering | HTML5 Canvas |
| Camera | Direct getUserMedia + requestVideoFrameCallback |
| Styling | CSS with custom properties |
| Logic | Vanilla JavaScript (ES6) |

---

## Controls

| Action | Gesture |
|--------|---------|
| Aim | Move index finger |
| Shoot | Quick upward flick |
| Cooldown | 185ms between shots |

The flick detector uses a timestamp-based history buffer with velocity calculation. A pinch gesture (thumb + index) serves as a fallback trigger.

---

## Getting Started

```bash
git clone https://github.com/ibrohim-ML/CV_GunGame.git
cd CV_GunGame
python -m http.server 8000
```

Open **http://localhost:8000** in your browser. Camera permission will be requested on page load.

> Camera access requires localhost or HTTPS. Serve via the local server — do not open the file directly.

---

## Visual Effects

- **Particle burst** — 22+ particles on hit, with gravity and drag
- **Shockwave ring** — expanding ring from impact point
- **Screen shake** — brief camera shake on successful hit
- **Crosshair** — dynamic ring with cross lines, color shifts when flick-armed
- **Background grid** — subtle scrolling grid for depth perception

---

## Project Structure

```
CV_GunGame/
├── test13.html    # Complete game (logic, rendering, styles)
├── README.md
└── .gitignore
```

Single-file design — no build tools or frameworks.

---

## License

MIT
