# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Chinatown Civic Compass (CCC) - A trilingual civic education website helping residents understand their rights, find community resources, and engage with their government. Built with pure HTML/CSS/JavaScript with no dependencies.

## File Structure

```
/
├── index.html          # Home page with hero, module cards, progress tracking
├── rights.html         # Know Your Rights module
├── resources.html      # Local Resources + emergency contact card
├── voting.html         # Voting & Elections information
├── contact.html        # Contacting representatives
├── faq.html            # Searchable FAQ with accordion
├── css/
│   └── styles.css      # Full design system (variables, components, print styles)
└── js/
    ├── main.js         # Navbar, mobile menu, utilities
    ├── i18n.js         # Language switching (EN/简体/繁體)
    ├── progress.js     # localStorage module tracking
    ├── glossary.js     # Side panel legal term definitions
    ├── faq.js          # Search + accordion functionality
    └── print.js        # Print-related utilities
```

## Development

No build step required. Open any HTML file directly in a browser to preview.

To serve locally with live reload, use any static server:
```bash
npx serve .
# or
python -m http.server 8000
```

## Architecture

### Translations (i18n.js)
- All translatable text uses `data-i18n="key"` attributes
- Translations stored in `translations` object with keys: `en`, `zh-s`, `zh-t`
- Language preference persisted via cookie (`ccc_language`)
- First visit shows language selection modal

### Progress Tracking (progress.js)
- Stores visited modules in localStorage (`ccc_progress`)
- Updates progress bar and module card completion icons
- Modules: `rights`, `resources`, `voting`, `contact`

### Glossary (glossary.js)
- Legal terms marked with `class="glossary-term" data-term="term-key"`
- Click opens slide-out side panel with definition in all 3 languages
- Definitions stored in `glossary` object in glossary.js

### Design System (styles.css)
- CSS variables for colors, spacing, typography
- Mobile-first responsive design
- Print styles via `@media print`
- Rounded/friendly aesthetic with warm colors

## Key CSS Variables

```css
--color-primary: #c41e3a;    /* Red */
--color-secondary: #2a5f4a;  /* Green */
--color-accent: #f4a460;     /* Gold */
--font-heading: Georgia, serif;
--font-body: 'Segoe UI', system-ui, sans-serif;
```

## Adding Content

### New Glossary Term
1. Add term to `glossary` object in `js/glossary.js`
2. Mark term in HTML: `<span class="glossary-term" data-term="your-key">term</span>`

### New Translation
1. Add key to all three language objects in `js/i18n.js`
2. Use in HTML: `<span data-i18n="your.key">Fallback text</span>`

### New FAQ Question
Add to `faq.html` following the existing `.faq-item` structure.

## Accessibility

- WCAG 2.1 AA compliant
- Skip-to-content link
- Proper heading hierarchy
- Keyboard navigable
- ARIA labels on interactive elements
- High contrast colors
- Respects `prefers-reduced-motion`
