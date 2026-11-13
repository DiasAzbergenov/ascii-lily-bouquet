# Luminous ASCII Lily Bouquet

A real-time, zero-dependency procedural ASCII art animation of a blooming lily bouquet built with vanilla JavaScript and HTML5 `<canvas>`.

Every frame renders stems, leaves, multi-layered lily petals, baby's breath sprigs, and a satin ribbon into a custom **Z-buffer character grid** (` .·:-=+*#%@`), layered over an offscreen bloom pass for a soft bioluminescent glow.

## Features

- **Procedural Growth & Blooming:** Stems grow along quadratic Bézier curves, leaves unfurl with central veins, and 9 lilies (plus 2 side buds) gradually open inner and outer petals with botanical speckles and stamens.
- **Custom Z-Buffer ASCII Renderer:** Depth-sorted character plotting ensures petals, stamens, stems, and ribbon overlap accurately in space.
- **Luminous Bloom & Rim Lighting:** Combines 9 multi-stop color palettes, glowing petal edges, and a blurred offscreen `<canvas>` pass (`globalCompositeOperation = "screen"`).
- **Rich Bouquet Details:** Includes delicate baby's breath (*gypsophila*) accents, a tied satin bow at the base, drifting petals, and multi-colored twinkling pollen particles.
- **Interactive Wind & Replay:** Responds smoothly to cursor movement and restarts the growth sequence on click.
- **Single-File & Zero Dependencies:** Runs natively in any modern browser—no frameworks, bundlers, or external assets required.

## Controls

| Input | Action |
| :--- | :--- |
| **Move Cursor** | Creates a gentle breeze swaying the bouquet and floating petals |
| **Left Click** | Restarts the growth and blooming animation from the beginning |

## Quick Start

1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/ascii-lily-bouquet.git](https://github.com/your-username/ascii-lily-bouquet.git)
   ```
2. Open `index.html` directly in any browser (or launch it with VS Code Live Server).

## Customization

- **ASCII Grid Density:** Adjust the divisor in `resize()` (`baseDim / 155`) for finer or chunkier characters.
- **Flower Palettes:** Edit the RGB color stops and `rim` highlights inside the `PALETTES` array.
- **Glow Intensity:** Tweak `ctx.globalAlpha` (`0.52`) and `ctx.filter = "blur(14px)"` in `render()`.
- **Animation Speed:** Change the `1.65` second duration constants in `render()` to speed up or slow down stem growth and blooming.

## License

MIT
