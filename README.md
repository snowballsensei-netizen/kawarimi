# Kawarimi

変わり身の術: the substitution technique.

A pixel-art puzzle platformer about a tanuki ninja and one kunai. Throw the kunai into wood and stand on it. Throw it through paper screens and swap places with it. Free the caged kits in all 16 levels of a haunted shrine.

The whole game is one HTML file with no build step and no dependencies. Open `index.html` in a browser to play. The pixel font loads from Google Fonts when you're online and falls back to a system monospace font offline.

## Controls

| Key | Action |
| --- | --- |
| ← → (or A D) | Run |
| ↑ (or W, Z) | Jump |
| Space (or X) | Throw the kunai. Press again to call it back |
| Shift (or C) | Swap places with the kunai |
| R | Restart the level |
| M | Sound on/off |
| Esc | Back to the title screen |

Phones get on-screen buttons.

## The shrine

The game has four chapters of four levels. Each chapter adds one new thing:

1. **Wood**: throwing, standing on the kunai, climbing, rotten wood
2. **Paper and swaps**: swapping through walls and in mid-flight
3. **Spirits**: drifting and circling wisps that the kunai can banish
4. **Spirit lamps**: lamps that switch the blue and ember gates

Progress, deaths and time are saved in the browser.

## Under the hood

- Canvas 2D at 320×192, scaled up with pixel-perfect rendering
- Sprites are drawn from palette strings in the source and outlined at load time. Tiles, lighting and the background are generated procedurally.
- Fixed 60 Hz simulation
- Sound effects and a looping taiko/shamisen/koto/flute soundtrack are synthesized live with the Web Audio API. There are no audio files.
