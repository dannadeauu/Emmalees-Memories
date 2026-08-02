# Emmalee's Memories — ems-mems

Static HTML conversion of the [ems-mems Figma design](https://www.figma.com/design/MXpv71B6v3Mu2KnrKzt9W9/ems-mems) (the 1728px "MacBook Pro 16" frame), built for GitHub Pages hosting.

## What's preserved from the Figma prototype

- **Layout** — exact 1728×8778 canvas, every element at its Figma coordinates, scaled to the viewport width via CSS zoom.
- **Fonts** — Instrument Serif, Playfair Display, Source Serif Pro (with Source Serif 4 fallback), and Inter, loaded from Google Fonts. The signature/script lettering is the original Canva-exported artwork, kept as images exactly as in the design.
- **Blend modes** — multiply / darken / lighten / screen / overlay on the script images and overlays, matching each layer's Figma blend mode.
- **Glass CSS** — the sticky top nav uses `backdrop-filter: blur(53px)` with `mix-blend-mode: overlay` (Figma glass effect, radius 53); the Step-card overlays use glass blurs of 20 and 29.
- **Animations / interactions**
  - Top nav links: smart-animate 200ms ease-out color change to `#91576D` on hover.
  - BOOK now! button: 300ms ease-out dissolve to `#F4D7DB` on hover.
  - Step cards: 300ms ease-out dissolve of both overlay layers on hover.
  - Pill buttons (CHARACTER LIST, VIEW PACKAGES, SCHEDULE HERE, LEAVE A REVIEW): 300ms dissolve to `#F8ECEE` on hover.
  - Sticky glass nav bar (sticks to the top of the viewport once the pink header scrolls away).
- **Video** — the "A message from Emmalee" placeholder is a real `<video>` player (`video/emmalee-message.mp4`, 1080p, extracted from emmaleesmemories.com) with the Figma frame as its poster.

## Hosting

Push to GitHub and enable **Settings → Pages → Deploy from branch** (root). `index.html` is self-contained; all assets are local except Google Fonts.
