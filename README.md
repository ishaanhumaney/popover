# Popover

CSS-only directional tooltips powered by HTML data attributes and pseudo-elements. No JavaScript engine overhead, no external dependencies, and zero setup required.

---

## Overview

Most modern tooltip libraries bring heavy JavaScript bundles, event listeners, and DOM-calculating scripts just to show a small text box on hover. `Popover` takes a different approach. By leaning entirely on native CSS rendering (`::before` and `::after` pseudo-elements) and reading text directly from inline `data-tooltip` HTML attributes, you get smooth, directional speech bubbles with minimal browser paint penalty.

---

## How It Works

The magic comes down to two CSS concepts working in tandem:

1. **`attr(data-tooltip)`:** The `::before` pseudo-element pulls its text content straight from the host tag's HTML attribute, keeping content inline without extra DOM nodes.
2. **Directional Classes & Transforms:** Classes like `.top`, `.bottom`, `.left`, and `.right` handle absolute positioning and hardware-accelerated transforms to slide the bubbles smoothly into place when hovered.

---

## Key Features

* **Zero JS Overhead:** Everything runs off the CSS render thread—no event listeners or runtime calculations.
* **4-Way Directional Support:** Fully configured positioning logic for top, bottom, left, and right popovers.
* **Custom Data Attribute Bindings:** Define tooltip text inline directly within your markup using `data-tooltip="..."`.
* **Smooth Micro-Animations:** Built-in transition offsets give a subtle floating effect on hover.
* **Lightweight Footprint:** Standard CSS properties with no external setup or preprocessors required.

---

## Tech Stack Breakdown

* **HTML5:** Semantic element structures with custom `data-*` attributes.
* **CSS3:** Pseudo-elements (`::before`, `::after`), absolute positioning, CSS transitions, and hardware-accelerated CSS `transform`.

---

## Prerequisites & Web-Based Quick Start

You don't need to clone this repo or run a local terminal server to work on it.

### Option A: Edit directly in GitHub Web UI
1. Press `.` (the period key) while viewing this repository to open VS Code in your browser via **github.dev**.
2. Make your edits to `index.html` or `style.css`.
3. Commit your changes directly from the browser sidebar.

### Option B: Local Setup
If you prefer running it locally, clone the repository and open `index.html` in any browser:
```bash
git clone [https://github.com/your-username/popover.git](https://github.com/your-username/popover.git)
cd popover
# Open index.html directly in your browser
```

## Project Structure

```text
popover/
├── .github/
│   └── workflows/
│       └── validate.yml  # Automated HTML & CSS validation pipeline
├── .gitignore            # Ignores local editor settings and temporary files
├── index.html            # Demo markup showing directional tooltips
├── style.css            # Core tooltip styles and positional logic
└── LICENSE               # MIT License file
```

## Roadmap

[ ] Add dynamic fallback positioning when elements sit near screen edges.

[ ] Support dark/light mode CSS variables for easy theme overrides.

[ ] Include subtle entry/exit spring physics animations.
