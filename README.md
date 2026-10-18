# Color Palette Generator

A simple, browser-based tool for generating random color palettes with copy-to-clipboard functionality.

## Features

- Generate a random 5-color palette with one click
- Instantly copy any color's hex value to the clipboard
- Visual feedback when copying succeeds
- Fully responsive grid layout
- Modern styling with smooth hover animations

## Project Structure

```
Color-Palete-Generator/
├── index.html      # HTML structure and page markup
├── index.css       # Styling and layout
├── index.js        # Palette generation and copy logic
└── README.md       # Project documentation
```

## Files

### index.html

Defines the page structure:
- Header with the generator title
- "Generate Palette" button with a sync icon
- Container holding five color boxes, each with:
  - A colored swatch
  - The hex value
  - A copy-to-clipboard button

Font Awesome (v6.7.2) is loaded from a CDN for icons, and `index.css` is linked for styling.

### index.css

Provides the visual design:
- Poppins font imported from Google Fonts
- Linear gradient page background
- White card container with rounded corners and shadow
- Responsive grid that adapts from 5 columns to fewer on smaller screens
- Hover lift animation on color boxes
- Copy button hover color transition

### index.js

Contains the application logic:

- `generatePalette()` — Creates 5 random hex colors and updates the display
- `generateRandomColor()` — Generates a single random hex color string
- `updatePaletteDisplay(colors)` — Applies colors and hex labels to each color box
- Copy handler — Listens for clicks on copy buttons and color swatches to copy hex values via the Clipboard API, showing a checkmark icon for 1.5 seconds on success

## Usage

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. Click **Generate Palette** to produce a new random 5-color palette.
4. Click any color box or its copy button to copy the hex value to your clipboard.

No build step, installation, or dependencies are required — it runs entirely in the browser.

## How It Works

The generator creates five random hex colors (`#RRGGBB`) on each button click and applies them to the five swatch boxes. Clicking a swatch or its copy icon invokes `navigator.clipboard.writeText()` to copy the hex value, with a brief visual confirmation via Font Awesome icon swap.

## Customization

- **Number of colors:** Edit the loop limit in `generatePalette()` in `index.js` (currently `5`).
- **Color range:** Modify `generateRandomColor()` in `index.js` to use different character sets or constrained palettes.
- **Styling:** Adjust colors, spacing, and breakpoints in `index.css`.
- **Layout:** Change the grid template columns in `.palette-container` in `index.css`.

## Browser Support

Works in all modern browsers that support:
- CSS Grid and custom properties
- ES6 JavaScript (arrow functions, template literals)
- The Clipboard API (`navigator.clipboard`)

## License

This project is open source and free to use.
