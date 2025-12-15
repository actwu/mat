# Material CSS

A small experimental **HTML + CSS material-style UI** built without JavaScript, frameworks, or build tools.  
This project focuses on **attribute-based theming**, **explicit colors**, and **duo-tone design** inspired by Material UI, but simplified and raw.

# Test, Click [```Here```](https://github.com/actwu/mat)

## What this is

Material CSS is **not a framework**.  
It’s a **demo-driven UI system** you can copy, tweak, and extend.

It uses:
- Custom elements like `cont` and `btn`
- Attribute selectors for themes
- Hard-coded hex colors instead of variables
- CSS filters for emoji and icon recoloring
- Dark-mode-first design

## Design philosophy

The core idea is **clarity over abstraction**.

- No CSS variables
- No `currentColor`
- No class-based theming
- No JavaScript
- No build step

Every color is explicit.  
Every theme is predictable.  
Every component adapts based on its parent theme.

## Theming system

Themes are applied using **attributes**, not classes.

### Light themes

- `r` – red  
- `b` – blue  
- `y` – yellow  
- `g` – green  

Light background with dark content.

### Dark / inverted themes

- `r2`
- `b2`
- `y2`
- `g2`

Dark background with light content.  
Each `2` theme is the **inverse of its base color**, not a new palette.

### Container themes

Applied to `cont` elements:

- `rt`
- `bt`
- `yt`
- `gt`

Container themes automatically style:
- textareas
- range sliders
- nested buttons
- background surfaces

## Components

### Buttons

`btn` is the only button primitive.

```html
<btn r>Submit</btn>
<btn b2>Cancel</btn>
``` 
Icons and emojis are recolored using CSS filters, not SVGs or images.

### Textareas

`Textareas` adapt automatically when placed inside themed containers.

```html
<cont rt>
  <textarea placeholder="Red theme textarea..."></textarea>
</cont>
```

### Range sliders

Sliders follow a material-flat style:

- No borders
- Theme-colored track

They adapt automatically based on the container theme (rt, bt, yt, gt).

```html
<cont bt>
  <input type="range" min="0" max="100">
</cont>
```

Why no CSS variables?

This project intentionally avoids:

- CSS custom properties.
- currentColor
- computed color logic

The goal is visual certainty.
You always know exactly which color is applied and where.

Browser support

- Modern Chromium-based browsers recommended
- WebKit-first slider styling
- Desktop-focused layout


Intended use

- UI experiments
- Material-style mockups
- Dashboards
- Personal tools
- Visual prototyping


Status

This is a living demo, not a finished library.
Styles evolve, filters are tuned visually, and structure may change.

Use it as a base, not a dependency.
