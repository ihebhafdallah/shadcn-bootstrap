<p align="center">
  <h1 align="center">Shadcn Bootstrap</h1>
  <p align="center">
    A drop-in CSS theme that restyles Bootstrap components to visually resemble <a href="https://ui.shadcn.com/">shadcn/ui</a>.
  </p>
</p>

# Shadcn Bootstrap

**Shadcn Bootstrap** is a lightweight CSS override layer for **Bootstrap** that brings the clean, modern visual style of [shadcn/ui](https://ui.shadcn.com/) to existing Bootstrap projects.

It does not replace Bootstrap or require React. Instead, it builds on top of Bootstrap's existing components and utilities, remapping Bootstrap design tokens and component styles to closely match the shadcn/ui aesthetic.

The stylesheet is designed to be loaded **after Bootstrap** so that your existing Bootstrap HTML and JavaScript components continue to work while receiving a modern shadcn-inspired appearance.

## Features

* **Shadcn-inspired Design**: Restyles Bootstrap components using the familiar shadcn/ui visual language.
* **Bootstrap Compatible**: Designed to work on top of Bootstrap without modifying Bootstrap itself.
* **Drop-in CSS**: Add one stylesheet after Bootstrap and existing Bootstrap components are automatically restyled.
* **Light & Dark Mode**: Supports Bootstrap's `data-bs-theme="dark"` attribute for dark mode.
* **Design Tokens**: Centralized CSS custom properties make colors, spacing, borders, radius, typography, and shadows easy to customize.
* **Modern Buttons**: Primary, secondary, outline, link, and destructive button styles inspired by shadcn/ui.
* **Styled Forms**: Inputs, selects, checkboxes, switches, labels, and input groups receive a consistent shadcn-style appearance.
* **Cards**: Bootstrap cards are redesigned with subtle borders, rounded corners, and modern spacing.
* **Navigation**: Navbar, nav links, tabs, and pills receive shadcn-inspired styling.
* **Dropdowns & Popovers**: Cleaner menus with rounded corners, borders, and subtle shadows.
* **Modals**: Modernized modal dialogs with shadcn-style spacing, borders, and shadows.
* **Tables**: Minimal table styling with subtle borders and muted headers.
* **Alerts & Badges**: Updated semantic components with a cleaner visual appearance.
* **Accordions**: Restyled Bootstrap accordion components with modern typography and spacing.
* **Pagination**: Updated pagination controls with shadcn-inspired borders and states.
* **Toasts**: Modern toast notifications with consistent borders and shadows.
* **Focus States**: Consistent accessible focus rings across interactive elements.
* **Custom Utilities**: Additional shadow and border-radius utility classes are included.
* **No JavaScript Required**: This project is purely CSS and does not introduce additional JavaScript dependencies.

## Requirements

* [Bootstrap](https://getbootstrap.com/)
* A modern browser with support for CSS custom properties.

## Installation

### 1. Include Bootstrap

Add Bootstrap to your project as you normally would:

```html
<link rel="stylesheet" href="bootstrap.min.css">
```

### 2. Include Shadcn Bootstrap

Load `shadcn-bootstrap.css` **after** Bootstrap:

```html
<link rel="stylesheet" href="bootstrap.min.css">
<link rel="stylesheet" href="shadcn-bootstrap.css">
```

The order is important because `shadcn-bootstrap.css` overrides Bootstrap's default component styles.

## Usage

Once the stylesheet is loaded, you can continue using standard Bootstrap markup.

For example:

```html
<button class="btn btn-primary">
    Primary Button
</button>

<button class="btn btn-secondary">
    Secondary Button
</button>

<button class="btn btn-outline-primary">
    Outline Button
</button>

<button class="btn btn-danger">
    Delete
</button>
```

No changes to your existing Bootstrap JavaScript are required.

### Cards

Standard Bootstrap cards automatically receive the shadcn-inspired styling:

```html
<div class="card">
    <div class="card-header">
        Account Settings
    </div>

    <div class="card-body">
        <h5 class="card-title">Profile</h5>
        <p class="card-text text-muted">
            Update your profile information.
        </p>

        <button class="btn btn-primary">
            Save Changes
        </button>
    </div>
</div>
```

### Forms

Bootstrap form components are automatically restyled:

```html
<div class="mb-3">
    <label for="email" class="form-label">Email address</label>

    <input
        type="email"
        class="form-control"
        id="email"
        placeholder="you@example.com"
    >

    <div class="form-text">
        We'll never share your email address.
    </div>
</div>
```

## Dark Mode

Dark mode is supported through Bootstrap 5.3's `data-bs-theme` attribute.

Add `data-bs-theme="dark"` to the `<html>` element:

```html
<html lang="en" data-bs-theme="dark">
```

Or dynamically toggle it with JavaScript:

```js
document.documentElement.setAttribute("data-bs-theme", "dark");
```

To return to light mode:

```js
document.documentElement.setAttribute("data-bs-theme", "light");
```

The stylesheet automatically updates the shadcn design tokens and Bootstrap variables when dark mode is enabled.

## Design Tokens

The theme is built around CSS custom properties prefixed with `--sc-`.

For example:

```css
:root {
    --sc-background: #ffffff;
    --sc-foreground: #09090b;
    --sc-primary: #18181b;
    --sc-secondary: #f4f4f5;
    --sc-muted: #f4f4f5;
    --sc-muted-foreground: #71717a;
    --sc-border: #e4e4e7;
    --sc-input: #e4e4e7;
    --sc-ring: #a1a1aa;
}
```

This makes it easy to customize the overall appearance without having to rewrite every component.

### Customizing Colors

For example, you can change the primary color:

```css
:root {
    --sc-primary: #2563eb;
    --sc-primary-foreground: #ffffff;
}
```

All components using the primary token will automatically use the new color.

### Customizing Border Radius

The default radius is:

```css
--sc-radius: 0.5rem;
```

You can change it globally:

```css
:root {
    --sc-radius: 0.75rem;
}
```

The related radius tokens will automatically update:

```css
--sc-radius-sm
--sc-radius-md
--sc-radius-lg
```

## Components

The stylesheet provides styling for the following Bootstrap components:

| Component     | Supported |
| ------------- | :-------: |
| Buttons       |     ✅     |
| Forms         |     ✅     |
| Form Controls |     ✅     |
| Selects       |     ✅     |
| Checkboxes    |     ✅     |
| Switches      |     ✅     |
| Input Groups  |     ✅     |
| Cards         |     ✅     |
| Badges        |     ✅     |
| Alerts        |     ✅     |
| Navbar        |     ✅     |
| Navigation    |     ✅     |
| Tabs          |     ✅     |
| Pills         |     ✅     |
| Dropdowns     |     ✅     |
| Popovers      |     ✅     |
| Tooltips      |     ✅     |
| Modals        |     ✅     |
| Tables        |     ✅     |
| List Groups   |     ✅     |
| Progress Bars |     ✅     |
| Spinners      |     ✅     |
| Pagination    |     ✅     |
| Toasts        |     ✅     |
| Accordions    |     ✅     |

## Custom Utility Classes

In addition to restyling Bootstrap, the stylesheet provides several shadcn-inspired utility classes.

### Shadows

```html
<div class="shadow-sc-sm"></div>
<div class="shadow-sc"></div>
<div class="shadow-sc-md"></div>
<div class="shadow-sc-lg"></div>
```

Available classes:

* `shadow-sc-sm`
* `shadow-sc`
* `shadow-sc-md`
* `shadow-sc-lg`

### Border Radius

```html
<div class="rounded-sc-sm"></div>
<div class="rounded-sc-md"></div>
<div class="rounded-sc-lg"></div>
```

Available classes:

* `rounded-sc-sm`
* `rounded-sc-md`
* `rounded-sc-lg`

## Focus States

Interactive elements receive a consistent shadcn-inspired focus ring.

The focus style is applied to components such as:

* Buttons
* Form controls
* Selects
* Checkboxes
* Navigation links
* Keyboard-focused links

The default focus ring is controlled by:

```css
--sc-ring: #a1a1aa;
```

You can customize it globally:

```css
:root {
    --sc-ring: #2563eb;
}
```

## Typography

The default font stack is based around Inter:

```css
--sc-font-sans:
    "Inter",
    ui-sans-serif,
    system-ui,
    -apple-system,
    "Segoe UI",
    Roboto,
    "Helvetica Neue",
    Arial,
    sans-serif;
```

If Inter is available in your project, it will be used automatically.

You can also override the font stack:

```css
:root {
    --sc-font-sans: "Inter", sans-serif;
}
```

## Project Structure

A minimal project can look like this:

```text
your-project/
├── index.html
├── css/
│   ├── bootstrap.min.css
│   └── shadcn-bootstrap.css
└── js/
    └── bootstrap.bundle.min.js
```

Your HTML only needs to load the stylesheets in the correct order:

```html
<head>
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <link rel="stylesheet" href="css/shadcn-bootstrap.css">
</head>
```

## Why Use This?

If you already have a Bootstrap project but prefer the visual style of shadcn/ui, migrating the entire project to React or replacing Bootstrap components is often unnecessary.

This project allows you to keep:

* Bootstrap's responsive grid
* Bootstrap's utility classes
* Bootstrap's JavaScript components
* Existing Bootstrap markup
* Existing Bootstrap integrations

while giving your application a cleaner, more modern visual style.

## Compatibility

This stylesheet is intended for:

* Bootstrap **5.x.x**
* Modern browsers supporting CSS custom properties

It is recommended to use the same Bootstrap version the stylesheet was designed against to minimize visual differences caused by changes in Bootstrap's CSS variables or component implementation.

## Customization

The recommended way to customize the theme is to override the `--sc-*` variables rather than modifying individual component rules.

For example:

```css
:root {
    --sc-background: #ffffff;
    --sc-foreground: #111827;

    --sc-primary: #2563eb;
    --sc-primary-foreground: #ffffff;

    --sc-secondary: #f3f4f6;
    --sc-secondary-foreground: #111827;

    --sc-muted: #f3f4f6;
    --sc-muted-foreground: #6b7280;

    --sc-border: #e5e7eb;
    --sc-input: #d1d5db;
    --sc-ring: #2563eb;

    --sc-radius: 0.625rem;
}
```

This allows you to create your own theme while keeping the component styles intact.

## Credits

Inspired by the design system and component styling of [shadcn/ui](https://ui.shadcn.com/).

Built on top of [Bootstrap](https://getbootstrap.com/).

## License

This project is provided as a CSS customization layer for Bootstrap.

Check the project's repository for the applicable license and contribution guidelines.
