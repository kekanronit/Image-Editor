# Image-Editor

A lightweight, browser-based image editor that lets you quickly apply common adjustments and presets to an image and export the result. The UI is split into a left-side control panel for filters and presets, and a right-side canvas for a live preview. Core features include choosing an image, resetting adjustments, and downloading the edited image.

## Features

- Upload / choose an image from your device
- Live preview on a canvas (right side)
- Filter controls (left panel):
  - Saturation
  - Exposure
  - Blur
  - Hue
  - Invert
- Presets (one-click combinations of filters) for quick looks
- Reset edits to original image
- Download edited image as a PNG/JPEG

## Visual layout (overview)

- Left column: controls and presets
  - Sliders / inputs for Saturation, Exposure, Blur, Hue, Invert toggle
  - Preset buttons (e.g., Vintage, B&W, Bright, High Contrast)
  - Reset and Download buttons
- Right column: single canvas that shows the current edited image in real time

## Getting started

Prerequisites
- Modern web browser (Chrome, Firefox, Edge, Safari)
- Project is static — no build step required in most cases

Quick start
1. Clone the repository or download the project files.
2. Open `index.html` in your browser. If the app uses modules or fetches assets, run a simple static server instead:

```bash
# using Python 3 (serve current dir at http://localhost:8000)
python -m http.server 8000

# or using npm package http-server (if you have Node.js)
npx http-server -p 8000
```

3. Visit http://localhost:8000 (or open the file directly) and use the UI:
   - Click "Choose image" to load a photo.
   - Adjust sliders on the left to change saturation, exposure, blur, hue, or toggle invert.
   - Click a preset to apply predefined settings instantly.
   - Use "Reset" to return to the original image.
   - Click "Download" to save the edited image.

## Usage details

- Choose Image: Loads an image into the editor. Supported formats: JPEG, PNG, GIF (depending on browser support).
- Saturation: Increase or decrease color intensity.
- Exposure: Lighten or darken the image (acts like brightness).
- Blur: Apply Gaussian or canvas blur to soften the image.
- Hue: Rotate colors around the color wheel.
- Invert: Toggle color inversion for a negative effect.
- Presets: Pre-configured combinations of the above settings for quick styles.
- Reset: Clears all adjustments and restores the original image.
- Download: Exports the current canvas contents; typical formats are PNG or JPEG.

Tips
- For best results use reasonably sized images (e.g., under a few megapixels) to keep the UI responsive.
- If preview looks pixelated, try increasing canvas resolution or using higher-quality export settings (if implemented).

## File structure (example)

- index.html — main UI
- css/ — stylesheets
- js/ — application logic (image loading, filter application, canvas handling)
- assets/ — icons, default images, etc.
- README.md — this file

(Adjust to match the repository's actual structure.)

## Extending / Development

- Add more filters (contrast, highlights/shadows, temperature, vignette).
- Add slider value presets and a custom preset save/load feature.
- Implement non-destructive editing (history stack / undo-redo).
- Optimize performance for large images (offscreen canvas, web workers).

If you'd like help adding a specific feature, tell me which one and I can propose code changes or a plan.

## Contributing

Contributions are welcome! Please open an issue to discuss proposed changes or submit a pull request with:
- A clear description of the change
- Related issue number (if any)
- Screenshots or GIFs for visual changes (if applicable)

Be sure to follow any existing code style and test your changes locally.

## License

This project is provided under the MIT License. See LICENSE file for details (or add one if missing).

## Acknowledgements

- Built with plain web technologies (HTML, CSS, JavaScript) — no heavy frameworks required.
- Inspired by simple, fast image-editing UIs and web canvas-based editors.
- 
