# Simple Maths Tools

Educational math tools designed for children learning fractions.

**Live site:** https://simple-maths-tools.adelindiac.site

## Tech Stack

- **Static HTML/CSS/JS** - No build tools, no frameworks
- **Fonts:** Fredoka (headings), Nunito (body) via Google Fonts
- **No dependencies** - All files are self-contained

## Design System

### Colors (CSS Variables)
```css
--bg-cream: #FFF8F0        /* Page background */
--primary-coral: #FF6B6B   /* Tools section accent */
--primary-mint: #4ECDC4    /* Practice section accent */
--primary-lavender: #A29BFE /* Focus states, buttons */
--primary-sunny: #FFE66D   /* Highlights */
--text-dark: #2D3436       /* Primary text */
--text-soft: #636E72       /* Secondary text */
```

### UI Patterns
- Light cream solid background using `--bg-cream`
- Rounded cards with soft shadows (`border-radius: 24px`)
- Large touch targets (minimum 44px) for tablet use
- Viewport locked to 100vh with `overflow: hidden`

## File Structure

```
simple-maths-tools/
├── index.html              # Home page with Tools/Practice sections
├── fraction-visualizer.html # Compare fractions with pie charts
├── simplify-fractions.html  # Practice simplifying fractions
└── CLAUDE.md
```

## Conventions

### Adding New Tools
1. Create a new `.html` file in this directory
2. Copy the CSS variables from existing files
3. Set body background to `var(--bg-cream)` for light cream background
4. Add a "← Home" button linking to `index.html`
5. Add entry to `index.html` in the appropriate section (Tools or Practice)

### Input Behavior (Practice Pages)
- Google Sheets-like input: no cursor, typing replaces on first keystroke
- Arrow keys navigate between inputs
- Enter to submit, Backspace clears entire field

### Responsive Design
- Must fit on horizontal tablet (100vh, no scrolling)
- Use `clamp()` for fluid typography
- Media queries at 800px and 500px breakpoints
