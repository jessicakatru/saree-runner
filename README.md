# Saree Runner

A 3D endless runner game built with **Three.js**, using 3D models generated through **[Vi3W](https://app.vi3w.in)**.

**Play it live:** https://warm-taiyaki-4a1e43.netlify.app

## About the Game

You play as a girl in a green saree running down a path. Dodge the wooden crates, jump over obstacles and collect coins to score points. The game gets faster the longer you survive.

## Controls

| Action | Desktop | Mobile |
|---|---|---|
| Move left / right | Arrow keys or A / D | Swipe left / right |
| Jump | Space, Up arrow or W | Tap or swipe up |

## How I Used Vi3W

All three 3D assets were generated in Vi3W using its Sketch → Image → 3D workflow:

1. **Player:** cartoon girl in a green saree (low poly)
2. **Obstacle:** wooden crate
3. **Collectible:** golden coin

Each model was exported as `.glb` and loaded into the game with Three.js `GLTFLoader`. The game automatically scales each model to the right size and places it on the ground.

## Tech Stack

- Three.js (loaded from CDN)
- Plain HTML + JavaScript (no build step)
- Netlify for hosting

## Project Structure

```
saree-runner/
├── index.html        # Game code
├── models/
│   ├── player.glb
│   ├── obstacle.glb
│   └── coin.glb
└── README.md
```

## Run Locally

Models are loaded over HTTP, so run a local server instead of opening the file directly:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## Author

Jessica Katru
