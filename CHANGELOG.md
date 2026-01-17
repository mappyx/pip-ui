# Changelog

All notable changes to the Pip UI Library will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.1.0] - 2026-01-16

### Added
- **Advanced Table System**: Complete table enhancement with professional features
  - **Sortable Columns**: Click headers to sort ascending/descending with visual indicators
  - **Pagination Controls**: Client-side pagination with customizable items per page
  - **Search/Filter**: Real-time table filtering with search input
  - **Table Variants**: `.pip-table-striped`, `.pip-table-bordered`, `.pip-table-compact`, `.pip-table-hover`
- **PipTable JavaScript Library**: `demo/pip-table.js` for advanced table functionality
  - Automatic sorting (numeric and alphabetic)
  - Live search filtering
  - Dynamic pagination with page controls
  - Configurable options (itemsPerPage, sortable, searchable, paginated)
- **Enhanced Demo**: Updated INV screen with 20-item inventory showcasing all table features
- **Comprehensive Documentation**: Complete table usage guide in README with examples

### Changed
- Table headers now support `.sortable` class for interactive sorting
- Pagination controls are now fully styled and responsive
- Search inputs have dedicated `.pip-table-search` styling
- Demo inventory expanded from 3 to 20 items for better pagination demonstration

### Fixed
- Table responsiveness on mobile devices with horizontal scrolling
- Pagination button states (active, disabled, hover)

## [3.0.1] - 2026-01-16

### Added
- **Comprehensive Documentation**: Complete README.md with usage examples for all components
- **Tooltip Component**: `.pip-tooltip` for contextual help text with hover effects
- **Accordion Component**: `.pip-accordion` for collapsible content sections
- **Enhanced Demo**: Added DATA screen showcasing tooltips and accordions
- **CHANGELOG.md**: Project changelog following Keep a Changelog format

### Changed
- Improved demo navigation with cleaner tab names (STAT, INV, DATA, SET)
- Enhanced mobile menu with better positioning and z-index management
- Updated demo footer with copyright notice

### Fixed
- Accordion toggle animation now works smoothly
- Modal overlay click-to-close functionality
- Mobile menu state management

## [3.0.0] - 2026-01-16

### Added
- **Mobile-First Responsive Design**: Complete media query integration
- **12-Column Grid System**: `.pip-row` and `.pip-col-{1-12}` with responsive modifiers
- **Modal Component**: `.pip-modal` and `.pip-modal-overlay` for dialogs
- **Card Component**: `.pip-card` with hover effects
- **Custom Form Controls**: Themed checkboxes (`.pip-checkbox-container`) and radio buttons (`.pip-radio-container`)
- **Global Box-Sizing**: Added `box-sizing: border-box` reset for consistent spacing
- **Responsive Tables**: `.pip-table-responsive` wrapper for horizontal scrolling on mobile

### Changed
- Refactored `web-base.scss` for better organization and maintainability
- Improved button padding and typography
- Enhanced progress bar animations
- Optimized CRT scanline effect z-index

### Fixed
- Grid column spacing inconsistencies
- Panel header indentation issues
- Mobile navigation toggle behavior

## [2.0.0] - 2026-01-16

### Added
- **Table Component**: `.pip-table` with striped rows and hover effects
- **Tab System**: `.pip-tabs` and `.pip-tab` for navigation
- **Select Dropdown**: `.pip-select` with custom styling
- **Badge Component**: `.pip-badge` with color variants (success, warning, error, info)
- **Progress Bars**: `.pip-progress-bar` with optional animated scanline effect
- **Enhanced Demo**: Interactive demo page with tab switching and progress animations

### Changed
- Expanded `web-base.scss` with new UI components
- Updated demo to showcase all new components

## [1.0.0] - 2026-01-16

### Added
- **SCSS Migration**: Converted all LESS files to SCSS
- **Web-Friendly Base Classes**: 
  - `.pip-body` for page styling
  - `.pip-panel` for content containers
  - `.pip-btn` for buttons with variants
  - `.pip-input` for form inputs
  - `.pip-text` with color modifiers
  - `.pip-container` for max-width layouts
- **CRT Effect**: `.pip-crt` class for authentic scanline overlay
- **Build System**: npm scripts for SCSS compilation
- **Demo Page**: Initial `demo/index.html` showcasing the theme

### Changed
- Migrated from LESS to SCSS syntax
- Updated variable syntax from `@` to `$`
- Converted mixins to SCSS `@mixin` and `@include`
- Fixed Sass deprecation warnings for division operations

### Fixed
- Mixin definition order in `buttons.scss`, `progress.scss`, and `text.scss`
- Sass division deprecation warnings using `calc()`

---

## Legend

- **Added**: New features
- **Changed**: Changes in existing functionality
- **Deprecated**: Soon-to-be removed features
- **Removed**: Removed features
- **Fixed**: Bug fixes
- **Security**: Vulnerability fixes
