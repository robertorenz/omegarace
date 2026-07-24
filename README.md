# Omega Race

A full-browser remake of the classic 1981 vector-arcade game **Omega Race** — in two flavors, selectable from a start page:

- **Classic Vector** (`classic.html`) — the original look: pure glowing 2D vector lines, exactly the way the cabinet felt. Zero dependencies.
- **Modern 3D** (`modern.html`) — the same arena rebuilt with Three.js: neon bloom, 3D wireframe ships and droids, spinning mines, particle explosions and a tilted battle camera.

## Play

**▶ Play it in your browser: [robertorenz.github.io/omegarace](https://robertorenz.github.io/omegarace/)**

Or open `index.html` locally (or serve the folder with any static server) and pick your arena. Both games fill the entire window and adapt to resizing. The Modern 3D version loads Three.js from a CDN, so it needs an internet connection; the Classic version runs fully offline.

## Controls

| Key | Action |
|-----|--------|
| `←` / `A` &nbsp; `→` / `D` | Rotate ship |
| `↑` / `W` | Thrust |
| `Space` | Fire |
| `P` | Pause |
| `M` | Mute sound |
| `Enter` | Start / restart |

## Gameplay

- Your ship has inertia and **bounces off the outer walls and the central scoreboard** — use the ricochet to your advantage.
- Player shots bounce off walls once, arcade-style.
- **Droids** (amber diamonds) patrol the track and speed up as their numbers fall; the last survivors break formation and hunt you.
- **Command ships** (red hexagons) fire aimed shots and drop **photon mines** (gold pulsing diamonds).
- Clear a wave to advance; each wave is faster, angrier, and adds commanders.

## Scoring

| Target | Points |
|--------|--------|
| Photon mine | 350 |
| Droid | 1,000 |
| Command ship | 1,500 |
| Wave clear bonus | wave × 500 |

Extra ship every 40,000 points. High scores persist in `localStorage` (tracked separately per mode, both shown on the start page).

## Tech

- `index.html` — start page with animated mode previews (vanilla canvas).
- `classic.html` — single-file HTML5 canvas game, vanilla JavaScript, vector-glow rendering with device-pixel-ratio aware scaling.
- `modern.html` — Three.js (ES modules via CDN import map) with UnrealBloom post-processing, wireframe polyhedra enemies, additive-blended particle bursts and a gently ship-following perspective camera.
- WebAudio-synthesized sound effects in both modes (no audio assets).
- Modal overlays for start / pause / game-over — no browser alerts.

`omegarace.html` is an earlier 800×600 prototype kept for reference.
