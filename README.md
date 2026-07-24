# Omega Race

A modern, full-browser remake of the classic 1981 vector-arcade game **Omega Race**, built as a single self-contained HTML file — no dependencies, no build step.

## Play

**▶ Play it in your browser: [robertorenz.github.io/omegarace](https://robertorenz.github.io/omegarace/)**

Or open `index.html` locally in any modern browser (or serve the folder with any static server). The game fills the entire window and adapts to resizing.

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

Extra ship every 40,000 points. High score persists in `localStorage`.

## Tech

- Single-file HTML5 canvas game (`index.html`), vanilla JavaScript.
- Vector-glow rendering with device-pixel-ratio aware scaling.
- WebAudio-synthesized sound effects (no audio assets).
- Modal overlays for start / pause / game-over.

`omegarace.html` is an earlier 800×600 prototype kept for reference.
