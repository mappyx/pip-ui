# Pip UI Library

A comprehensive, mobile-first UI library with a retro terminal aesthetic. Built with pure SCSS, no dependencies required.

![Version](https://img.shields.io/badge/version-1.1.0-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## ✨ Features

- 🎨 **Retro Terminal Aesthetic**: Classic phosphor green terminal styling with customizable CRT effects
- 📱 **Mobile-First**: Fully responsive with breakpoints optimized for all devices
- 🎯 **Advanced Layout**: 12-column grid and **CSS Grid Areas** support
- ✨ **Atmospheric Animations**: Built-in typewriter, ghosting, and flicker effects
- 🚀 **Zero Dependencies**: Pure CSS, no JavaScript required
- 🔧 **Customizable**: CSS Custom Properties for runtime theming
- ♿ **Semantic HTML**: Accessible markup structure

## 🚀 Quick Start
...
### Usage

Include the compiled CSS in your HTML:

```html
<link rel="stylesheet" href="dist/pipboy.css">
```

Apply the base class to your body for the full experience:

```html
<body class="pip-body pip-crt">
    <div class="pip-container">
        <!-- Your content here -->
    </div>
</body>
```

## 📦 Components

### Grid & Layout

**Flexible Grid:**
Standard 12-column row/col system.

**Named Grid Areas:**
Use `pip-grid-areas` for complex terminal layouts:
```html
<div class="pip-grid-areas" style="grid-template-areas: 'header header' 'nav main' 'footer footer';">
    <header style="grid-area: header">...</header>
    <nav style="grid-area: nav">...</nav>
    <main style="grid-area: main">...</main>
    <footer style="grid-area: footer">...</footer>
</div>
```

**Spacing Utilities:**
Standardized padding and margin classes:
- `pip-m-[0-5]`: Margin
- `pip-p-[0-5]`: Padding
- `pip-mt-[0-5]`, `pip-pb-[0-5]`, etc.

### Panels & Cards
...

### Alerts [NEW]

Thematic notification boxes for warnings and errors.

```html
<div class="pip-alert warning">
    <span class="pip-alert-title">Hazard Warning</span>
    <p>Environmental interference detected.</p>
</div>

<div class="pip-alert error">
    <span class="pip-alert-title">Critical Failure</span>
    <p>System reboot required.</p>
</div>
```

### Loaders [NEW]

Terminal-style loading animations.

```html
<!-- Inline loader with text -->
<div class="pip-loader">Connecting to Terminal...</div>

<!-- Block loader -->
<div class="pip-loader block">Processing</div>
```

### Buttons
...

### Sidebar

A vertical navigation component for terminal interfaces.

```html
<aside class="pip-sidebar">
    <div class="pip-sidebar-header">
        <div class="pip-logo">LOGO</div>
    </div>
    <nav class="pip-sidebar-nav">
        <a href="#" class="pip-sidebar-link active">LINK 1</a>
        <a href="#" class="pip-sidebar-link">LINK 2</a>
    </nav>
</aside>
```

### Forms

#### Input
```html
<input type="text" class="pip-input" placeholder="Enter text...">
```

#### Select
```html
<div class="pip-select-container">
    <select class="pip-select">
        <option>Option 1</option>
        <option>Option 2</option>
    </select>
</div>
```

#### Checkbox
```html
<label class="pip-checkbox-container">
    Enable Feature
    <input type="checkbox" checked>
    <span class="checkmark"></span>
</label>
```

#### Radio
```html
<label class="pip-radio-container">
    Option A
    <input type="radio" name="group" checked>
    <span class="checkmark"></span>
</label>
```

### Data Display

#### Table

**Basic Table:**
```html
<div class="pip-table-responsive">
    <table class="pip-table">
        <thead>
            <tr>
                <th>Item</th>
                <th>Value</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Data 1</td>
                <td>100</td>
            </tr>
        </tbody>
    </table>
</div>
```

**Advanced Table with Sorting & Pagination:**
```html
<!-- Search Bar -->
<div class="pip-table-search">
    <span class="pip-search-icon">⌕</span>
    <input type="text" placeholder="Search..." id="my-search">
</div>

<!-- Table -->
<div class="pip-table-responsive">
    <table class="pip-table pip-table-hover" id="my-table">
        <thead>
            <tr>
                <th class="sortable">Name</th>
                <th class="sortable">Value</th>
            </tr>
        </thead>
        <tbody>
            <tr><td>Item 1</td><td>100</td></tr>
            <tr><td>Item 2</td><td>200</td></tr>
        </tbody>
    </table>
</div>

<!-- Pagination -->
<div class="pip-table-pagination">
    <div class="pip-pagination-info">Showing 1-10 of 20</div>
    <div class="pip-pagination-controls">
        <button>‹</button>
        <button class="active">1</button>
        <button>2</button>
        <button>›</button>
    </div>
</div>

<!-- JavaScript Initialization -->
<script src="pip-table.js"></script>
<script>
    new PipTable('my-table', {
        itemsPerPage: 10,
        sortable: true,
        searchable: true,
        paginated: true
    });
</script>
```

**Table Variants:**
```html
<!-- Striped rows -->
<table class="pip-table pip-table-striped">...</table>

<!-- Bordered cells -->
<table class="pip-table pip-table-bordered">...</table>

<!-- Compact spacing -->
<table class="pip-table pip-table-compact">...</table>

<!-- Hover effect -->
<table class="pip-table pip-table-hover">...</table>

<!-- Combine variants -->
<table class="pip-table pip-table-striped pip-table-hover">...</table>
```

**Sortable Columns:**
Add `class="sortable"` to `<th>` elements to enable sorting:
```html
<th class="sortable">Column Name</th>
```

Click headers to sort. The `pip-table.js` library handles:
- Ascending/descending toggle
- Numeric vs. alphabetic sorting
- Visual indicators (▲/▼)

#### Tabs
```html
<div class="pip-tabs">
    <button class="pip-tab active" data-target="tab1">Tab 1</button>
    <button class="pip-tab" data-target="tab2">Tab 2</button>
</div>

<div id="tab1" class="pip-tab-content active">Content 1</div>
<div id="tab2" class="pip-tab-content">Content 2</div>
```

#### Badge
```html
<span class="pip-badge">Default</span>
<span class="pip-badge success">Active</span>
<span class="pip-badge warning">Warning</span>
<span class="pip-badge error">Critical</span>
<span class="pip-badge info">Info</span>
```

#### Progress Bar
```html
<div class="pip-progress-container">
    <div class="pip-progress-bar" style="width: 75%;"></div>
</div>

<!-- Animated variant -->
<div class="pip-progress-container">
    <div class="pip-progress-bar animated" style="width: 50%;"></div>
</div>
```

### Modal

```html
<div id="myModal" class="pip-modal-overlay">
    <div class="pip-modal">
        <div class="pip-modal-header">
            <h2>Modal Title</h2>
        </div>
        <p class="pip-text">Modal content here.</p>
        <div class="pip-modal-footer">
            <button class="pip-btn primary" onclick="closeModal()">OK</button>
        </div>
    </div>
</div>

<script>
function closeModal() {
    document.getElementById('myModal').classList.remove('active');
}
</script>
```

### Typography

```html
<p class="pip-text">Default text</p>
<p class="pip-text subtle">Subtle text</p>
<p class="pip-text highlight">Highlighted text</p>
<p class="pip-text selected">Selected text</p>
<p class="pip-text success">Success message</p>
<p class="pip-text warning">Warning message</p>
<p class="pip-text error">Error message</p>
```

### Effects

#### CRT Scanline Effect
```html
<body class="pip-body pip-crt">
    <!-- Adds authentic CRT monitor scanlines -->
</body>
```

#### Atmospheric Animations [NEW]

Retro effects for realistic terminal feedback.

**Typewriter:**
```html
<p class="pip-typewriter">Initializing system components...</p>
```

**Ghosting (Phosphor Persistence):**
```html
<div class="pip-ghosting" data-text="CRITICAL ERROR">CRITICAL ERROR</div>
```

**Fade-in & Delay:**
```html
<div class="pip-anim-fade-in pip-delay-2">Deferred content</div>
<div class="pip-anim-fade-in pip-delay-4">Next sequence</div>
```

## 🎨 Customization

Edit `styles/ui-variables.scss` to customize colors and spacing:

```scss
// Base Colors
$text-color: #0c833d;
$text-color-selected: #1cfa80;
$base-background-color: #052308;
$base-border-color: #0c833d;

// Component Spacing
$component-padding: 15px;
$component-border-radius: 3px;
```

## 📱 Responsive Breakpoints

- **Mobile**: < 768px (single column layout)
- **Desktop**: ≥ 769px (multi-column grid support)

## 🛠️ Development

```bash
# Install dependencies
npm install

# Build CSS once
npm run build:sass

# Watch for changes
npm run watch:sass
```

## 📄 Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 License

MIT License - see LICENSE file for details

## 🎮 Credits

Inspired by retro terminal interfaces and classic computer displays.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

**Built with ❤️ for Pip UI Terminal Systems**
