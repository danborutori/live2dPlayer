# Live2D Player

A lightweight, browser-based viewer for VTube Studio Live2D models with gesture controls, audio triggers, and animation support. Supports drag & drop of model directories or ZIP files. Works offline after initial load and is mobile-friendly.

## Features

- **Model Loading**: Drag & drop folders/ZIP files or tap to select (includes VTube Studio .vtube.json support).

- **Gestures**:
  - **Desktop**: Left drag to pan, right drag to rotate, mouse wheel to zoom.
  - **Mobile**: 1-finger drag to pan, pinch to zoom & rotate.

- **Interactions**: Tap model parts (hit areas) to trigger animations.

- **Audio Triggers**: Automatic sound playback based on parameter thresholds (from Setting.txt in Sound/ folder).

- **Fullscreen Mode**: Click the fullscreen button to enter/exit fullscreen.

- **Smooth Effects**: Blinking, mouse tracking.

## Quick Start

1. **Download & Serve Locally**: Clone or download this repo. Open index.html directly in a browser may fail due to CORS restrictions—serve via a local server (e.g., Python: python -m http.server 8000, Node: npx serve ., or VS Code Live Server extension). Recommended: Chrome/Firefox.

2. **Load Model**:
   - Drag a VTube Studio model folder or ZIP file onto the canvas.
   - On mobile: Tap the info text to select a ZIP.

3. **Interact**:
   - Tap parts to start/stop animations.
   - Use gestures to pan/rotate/zoom.
   - Click fullscreen button for immersive view.

## Requirements

- Modern browser with WebGL support (no install needed).

- Model files: VTube Studio .model3.json, .vtube.json, and optional Sound/ folder with .wav and Setting.txt.

## Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Pan | Left drag | 1-finger drag |
| Rotate | Right drag | Pinch-rotate |
| Zoom | Mouse wheel | Pinch-spread |
| Trigger Animation | Click model part | Tap model part |
| Fullscreen | Button | Button |

## Customization

- **Hit Areas/Animations**: Edit `player.config.json` for hit areas, param IDs, and thrusting ranges.

- **Audio**: Add `Setting.txt` (JSON) and .wav files in Sound/ for triggers (e.g., play sound when param > threshold).

- **Gestures**: Adjust sensitivity in code (e.g., scaleSmoothing = 0.05 for slower zoom).

## Dependencies

- PIXI.js v6.5.2 (rendering).

- JSZip v3.10.1 (ZIP support).

- Live2D Cubism SDK (model rendering).

## Credits

- Based on pixi-live2d-display for Live2D integration.

- Audio/Web Audio API for sound triggers.

- Thanks to VTube Studio community for model format.

## License

MIT License. Feel free to fork/modify.

Questions? Open an issue!

## Change Log
- Changes v1.4:
   - Mask resolution increased from 256 to 1024