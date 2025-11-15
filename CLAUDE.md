# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal website for Kanaad Shetty, featuring a portfolio/about page and blog. Built with vanilla HTML and CSS—no build tools, frameworks, or dependencies.

## Architecture

### File Structure
- `index.html` - Main landing page with profile, about, skills, and contact sections
- `blogs.html` - Blog listing page with card grid layout
- `blog-post-[1-3].html` - Individual blog post pages
- `styles.css` - Single CSS file containing all styles (general, blog grid, and blog post styles)
- `profile.jpeg` - Profile image used in header

### Navigation System
Two-page navigation (`index.html` ↔ `blogs.html`) with active state styling via `.nav-link.active` class. Blog posts link back to `blogs.html`.

### Styling Architecture
All styles in `styles.css` organized in sections:
1. Base styles (reset, body, container)
2. Header and navigation
3. Typography (h1, h2, p, etc.)
4. Component styles (badges, lists, footer)
5. Blog-specific styles (grid, cards, post layout)
6. Responsive styles (@media queries)

**Design System:**
- Typography: Georgia serif for body, -apple-system sans-serif for headings/UI
- Color scheme: Neutral palette (#1f1f1d text, #fafaf9 background, #787670 muted)
- Max width: 620px centered container
- Spacing: Consistent use of 1rem, 1.5rem, 2rem increments

## Development Workflow

### Preview Changes
```bash
# Open in default browser
open index.html

# Or use Python simple server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### Adding New Blog Posts
1. Create new `blog-post-N.html` following the structure of existing posts
2. Include blog post header with title, meta, and back link
3. Add blog card entry to `blogs.html` blog-grid section
4. Use Unsplash images (w=800&h=400 for cards, w=1200&h=600 for post headers)
5. Update date in both card and post meta

### Styling Guidelines
- Maintain responsive breakpoint at 640px (see @media section)
- Use existing spacing scale (0.5rem, 0.75rem, 1rem, 1.5rem, 2rem)
- Header elements use sans-serif, body content uses Georgia serif
- All interactive elements should have hover states with transitions
- Border colors: #d9d9d6 for primary borders, #e0e0dd for secondary

### Content Updates
- Profile image: Replace `profile.jpeg` (maintain 1:1 aspect ratio)
- Contact links: Update in `index.html` lines 89-114
- Skills badges: Modify `.badge-container` in `index.html` lines 73-84
- About/bio sections: Edit corresponding `<section>` blocks in `index.html`
