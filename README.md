# Charis CSS Documentation

Charis is Mira Is Away's opinionated CSS framework designed for crafting elegant and modern web interfaces with ease. It combines reusable components with a powerful set of utility classes, enabling rapid development without sacrificing style.

## Table of Contents
- [Setup](#setup)
- [Theming](#theming)
  - [Customization](#customization)
- [Layout](#layout)
- [Components](#components)
  - [Buttons](#buttons)
  - [Cards](#cards)
  - [Panels](#panels)
  - [Dock](#dock)
  - [Search Bar](#search-bar)
- [Utility Classes](#utility-classes)
  - [Spacing](#spacing)
  - [Flexbox](#flexbox)
  - [Grid](#grid)
  - [Sizing](#sizing)
  - [Typography](#typography)
  - [Display & Style](#display--style)

---

## Setup
To get started, link the `charis.css` file in the `<head>` of your HTML document.  
Charis also requires specific fonts from Google Fonts, which are imported at the top of the CSS file.

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Awesome Site</title>
  <link rel="stylesheet" href="path/to/charis.css">
</head>
<body>
  <!-- Your content here -->
</body>
</html>
````

---

## Theming

Charis is built with CSS variables, making it easy to customize. It includes a default dark theme and a pre-configured light theme.

To activate the light theme, add the `.light` class to the `<body>` element:

```html
<body class="light">
  <!-- Content will now use the light theme -->
</body>
```

### Customization

Override the default color palette, fonts, and other properties by redefining the CSS variables in your own stylesheet:

```css
/* In your custom CSS file */
:root {
  --charis-primary: #5A9A47; /* Change primary color to green */
  --charis-primary-hover: #7AC265;
  --charis-radius: 0.5rem; /* Make corners sharper */
}
```

---

## Layout

**`.container`** — A responsive, max-width wrapper that centers your content.

```html
<div class="container">
  <p>This content is centered and has a maximum width.</p>
</div>
```

---

## Components

### Buttons

Use the `.button` class for actions. Add `.hollow` for an outline-style button.

```html
<!-- Standard Button -->
<button class="button">Click Me</button>

<!-- Hollow Button -->
<button class="button hollow">Learn More</button>

<!-- Button as a Link -->
<a href="#" class="button">Get Started</a>
```

---

### Cards

**`.card`** — Standard content container
**`.navcard`** — Behaves like a card with a link and hover effect.

```html
<!-- Standard Card -->
<div class="card">
  <h3>Card Title</h3>
  <p>Some content inside the card.</p>
</div>

<!-- Navigational Card -->
<a href="#" class="navcard">
  <h3>Clickable Card</h3>
  <p>This whole card is a link.</p>
</a>
```

---

### Panels

* **`.flex-panel`** — Arranges children in a row using Flexbox.
* **`.grid-panel`** — Arranges children in a responsive grid.

```html
<!-- Flex Panel -->
<div class="flex-panel p-2">
  <div class="card">Item 1</div>
  <div class="card">Item 2</div>
</div>

<!-- Grid Panel -->
<div class="grid-panel p-2">
  <div class="card">Item A</div>
  <div class="card">Item B</div>
  <div class="card">Item C</div>
</div>
```

---

### Dock

A fixed-position navigation bar at the bottom of the viewport.

```html
<div class="dock">
  <a href="#" class="dock-item" title="Home">🏠</a>
  <a href="#" class="dock-item" title="Profile">👤</a>
  <a href="#" class="dock-item" title="Settings">⚙️</a>
</div>
```

---

### Search Bar

A stylish, fixed-position search bar with animated glow on focus.

```html
<div class="search-wrapper">
  <input type="search" placeholder="Search...">
</div>
```

---

## Utility Classes

### Spacing

**Margin:** `.m-0`, `.m-1`, `.m-2`, `.m-3`, `.mx-auto`
**Padding:** `.p-0`, `.p-1`, `.p-2`, `.p-3`

```html
<div class="card m-2 p-3">...</div>
```

---

### Flexbox

* `.flex` — Main flex container
* `.flex-center` — Center horizontally and vertically
* Direction: `.flex-column`
* Wrapping: `.flex-wrap`
* Justify Content: `.justify-center`, `.justify-between`
* Align Items: `.items-center`
* Growth: `.flex-grow`

```html
<div class="flex justify-between items-center">
  <div>Left</div>
  <div>Right</div>
</div>
```

---

### Grid

* Container: `.grid`
* Columns: `.grid-cols-1`, `.grid-cols-2`, `.grid-cols-3`, `.grid-cols-auto`
* Gap: `.grid-gap-0`, `.grid-gap-1`, `.grid-gap-2`, `.grid-gap-3`
* Spanning: `.grid-span-1`, `.grid-span-2`, `.grid-span-3`
* Alignment: `.grid-justify-*`, `.grid-align-*` (`start`, `center`, `end`)

```html
<div class="grid grid-cols-3 grid-gap-2">
  <div class="grid-span-2">Takes up two columns</div>
  <div>Takes up one column</div>
</div>
```

---

### Sizing

* `.w-full` — `width: 100%`
* `.h-full` — `height: 100%`
* `.max-w-sm` — `max-width: 24rem`
* `.max-w-md` — `max-width: 28rem`

---

### Typography

* Alignment: `.text-left`, `.text-center`, `.text-right`
* Transform: `.text-uppercase`, `.text-lowercase`
* Whitespace: `.text-nowrap`

---

### Display & Style

* Display: `.hidden`, `.block`, `.inline`, `.inline-block`
* Cursor: `.cursor-pointer`
* Borders: `.border`, `.rounded`
* Effects: `.shadow`, `.glow`, `.transparent`, `.frosted`
* Positioning: `.fullscreen-center`

```