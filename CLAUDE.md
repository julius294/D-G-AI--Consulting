# CLAUDE.md - AI Assistant Guide for D&G AI-Consulting Website

## Project Overview

**Project Name**: D&G AI-Consulting Website
**Type**: Single-page marketing website
**Language**: German (de)
**Technology Stack**: Pure HTML5, CSS3, Vanilla JavaScript
**Purpose**: Marketing website for AI automation consulting services
**Founders**: Julius Dönnebrink & Nils Gerz
**Location**: Bonn, Germany region
**Founded**: 2025

## Repository Structure

```
D-G-AI--Consulting/
├── index.html          # Main website file (single-page application)
├── CLAUDE.md          # This file - AI assistant guide
└── .git/              # Git repository data
```

### File Architecture

This is a **single-file website** with all components embedded:
- HTML structure
- CSS styling (embedded in `<style>` tags)
- JavaScript functionality (embedded in `<script>` tags)
- No external dependencies except Google Fonts

## Technology Stack

### Core Technologies
- **HTML5**: Semantic markup, responsive meta tags
- **CSS3**: Custom properties (CSS variables), Grid, Flexbox, animations
- **Vanilla JavaScript**: No frameworks, pure DOM manipulation
- **Google Fonts**:
  - `Outfit` (weights: 300, 400, 500, 600, 700)
  - `Space Grotesk` (weights: 400, 500, 600, 700)

### No Build Process
- No package managers (npm, yarn)
- No bundlers (webpack, vite)
- No preprocessors (Sass, Less)
- No frameworks (React, Vue, etc.)
- Direct deployment ready

## Website Sections

The single-page website consists of these sections (in order):

1. **Navigation** (`#nav`) - Fixed header with scroll effect
2. **Hero Section** (`.hero`) - Landing area with CTA
3. **Stats Section** (`.stats`) - Key metrics display
4. **Services Section** (`#services`) - 6 service cards
5. **Benefits Section** (`#benefits`) - Value propositions
6. **About Section** (`#about`) - Company information
7. **CTA Section** (`.cta`) - Call-to-action banner
8. **Contact Section** (`#contact`) - Contact form and info
9. **Footer** (`.footer`) - Links and copyright

## Design System

### Color Palette (CSS Variables in `:root`)

```css
--primary: #0a0a0a;              /* Near black */
--secondary: #1a1a2e;            /* Dark blue-black */
--accent: #00d4ff;               /* Cyan/Turquoise accent */
--accent-glow: #00d4ff40;        /* Accent with transparency */
--accent-secondary: #7b2cbf;     /* Purple accent */

--text-primary: #ffffff;         /* White */
--text-secondary: #a0a0a0;       /* Gray */
--text-muted: #666666;           /* Darker gray */

--bg-dark: #0a0a0a;              /* Dark background */
--bg-card: #111111;              /* Card background */
--bg-card-hover: #1a1a1a;        /* Card hover state */
```

### Spacing System

```css
--section-padding: 120px;        /* Standard section padding */
--container-width: 1200px;       /* Max content width */
```

### Transitions

```css
--transition-fast: 0.2s ease;
--transition-medium: 0.4s ease;
--transition-slow: 0.6s ease;
```

## Key Features

### Visual Effects
- **Animated grid background**: Subtle cyan grid overlay
- **Gradient glows**: Floating gradient orbs for ambiance
- **Scroll-based animations**: Intersection Observer for fade-in effects
- **Smooth scrolling**: Native smooth scroll behavior
- **Hover effects**: Interactive cards and buttons
- **Gradient text**: Cyan to purple gradients on headings

### Interactive Elements
- Sticky navigation with backdrop blur on scroll
- Smooth anchor link scrolling
- Scroll-triggered animations (fade-in, translate)
- Floating card animations
- Rotating visual circles in hero section

### Responsive Design

Breakpoints:
- **Desktop**: Default (1024px+)
- **Tablet**: 768px - 1024px (2-column grids)
- **Mobile**: 480px - 768px (single column, mobile menu)
- **Small Mobile**: < 480px (further optimizations)

## Development Guidelines for AI Assistants

### When Making Changes

#### DO:
- ✅ **Preserve the single-file structure** - Keep everything in index.html
- ✅ **Maintain German language** - All user-facing text must be in German
- ✅ **Follow existing naming conventions** - BEM-like class naming
- ✅ **Keep color scheme consistent** - Use CSS variables
- ✅ **Test responsiveness** - Ensure changes work on all breakpoints
- ✅ **Preserve animations** - Maintain smooth UX transitions
- ✅ **Use semantic HTML** - Keep accessibility in mind
- ✅ **Maintain brand voice** - Professional yet approachable German tone

#### DON'T:
- ❌ **Split into multiple files** - Unless explicitly requested
- ❌ **Add build tools** - Keep it simple and deployment-ready
- ❌ **Add frameworks** - Vanilla JS only
- ❌ **Change brand colors** - Without explicit approval
- ❌ **Remove accessibility features** - aria-labels, semantic tags
- ❌ **Break mobile responsiveness** - Test all breakpoints
- ❌ **Add external dependencies** - Except fonts if needed

### Code Style Conventions

#### HTML
- Use semantic HTML5 elements (`<section>`, `<nav>`, `<footer>`)
- Maintain clear section structure with comments
- Use meaningful IDs for navigation anchors
- Include ARIA labels where appropriate

#### CSS
- Use CSS custom properties for theme values
- Group related styles with clear comment headers
- Mobile-first approach in media queries (max-width)
- Prefer `rem` and `clamp()` for responsive typography
- Use `gap` instead of margins in flex/grid layouts

#### JavaScript
- Use modern ES6+ syntax
- Prefer `const` and `let` over `var`
- Use arrow functions for callbacks
- Comment complex logic clearly
- Keep functionality modular and readable

### Common Tasks

#### Adding a New Section
```html
<!-- Add before footer, follow this pattern -->
<section class="new-section section" id="new-section">
    <div class="container">
        <div class="section-header">
            <span class="section-label">LABEL TEXT</span>
            <h2 class="section-title">Section Title</h2>
            <p class="section-subtitle">Subtitle text</p>
        </div>
        <!-- Section content -->
    </div>
</section>
```

#### Modifying Colors
- Always use CSS variables in `:root`
- Update the variable, not individual instances
- Consider gradient combinations (accent + accent-secondary)

#### Adding New Services
- Follow the `.service-card` structure
- Maintain 3-column grid on desktop (adjusts to 2/1 on smaller screens)
- Use emoji icons consistently
- Include feature list with checkmarks

### Contact Form Integration

The contact form currently uses a placeholder Formspree URL:
```html
<form action="https://formspree.io/f/your-form-id" method="POST">
```

**To activate the form:**
1. Create a Formspree account
2. Replace `your-form-id` with actual Formspree ID
3. Or integrate with alternative form backend (Netlify Forms, etc.)

### Email Configuration

Primary contact email: `julius@doennebrink-ai.de`
Update in multiple locations:
- index.html:1422 - CTA section email link
- index.html:1445 - Contact section email display

## Git Workflow

### Branch Strategy
- **Main branch**: Production-ready code
- **Feature branches**: Use `claude/` prefix for AI assistant work
- Current branch: `claude/claude-md-mkisiidnfvemee0d-10gPS`

### Commit Guidelines
- Write clear, descriptive commit messages in English
- Use conventional commit format when possible:
  - `feat:` for new features
  - `fix:` for bug fixes
  - `docs:` for documentation
  - `style:` for formatting changes
  - `refactor:` for code refactoring

### Deployment Notes
- No build step required
- Direct deployment: Simply upload `index.html` to web server
- Compatible with: GitHub Pages, Netlify, Vercel, any static hosting

## SEO and Meta Information

### Current Meta Tags
```html
<title>D&G AI-Consulting | KI-Automatisierung für Ihr Unternehmen</title>
<meta name="description" content="D&G AI-Consulting - Ihre Experten für KI-Automatisierung aus der Region Bonn. Wir entlasten Ihr Unternehmen mit intelligenten Lösungen.">
```

### Missing SEO Elements (Consider Adding)
- Open Graph tags for social sharing
- Twitter Card meta tags
- Favicon link
- Canonical URL
- Structured data (JSON-LD) for local business
- robots.txt reference
- sitemap.xml (if site expands)

## Accessibility Considerations

### Current Accessibility Features
- Semantic HTML structure
- ARIA labels on interactive elements (mobile menu button)
- Sufficient color contrast (light on dark theme)
- Smooth scroll with `prefers-reduced-motion` consideration needed
- Keyboard-navigable links and buttons

### Accessibility Improvements Needed
- Add `alt` attributes if images are added
- Ensure form inputs have associated labels (✓ currently implemented)
- Test keyboard navigation flow
- Add skip-to-content link
- Add `prefers-reduced-motion` media query to disable animations
- Improve focus indicators

## Performance Optimization

### Current Optimizations
- Single file = minimal HTTP requests
- Font preconnect to Google Fonts CDN
- No external JavaScript libraries
- Efficient CSS animations (transform, opacity)
- Intersection Observer for scroll animations

### Potential Improvements
- Add lazy loading for form (if it's below fold)
- Minify CSS and JavaScript for production
- Add resource hints (`preload`, `prefetch`)
- Consider inline critical CSS
- Add service worker for offline capability

## Testing Checklist

Before deploying changes, verify:

- [ ] **Visual Testing**
  - [ ] Desktop view (1920px, 1440px, 1280px)
  - [ ] Tablet view (768px, 1024px)
  - [ ] Mobile view (375px, 414px, 360px)
  - [ ] Small mobile (320px)

- [ ] **Functionality**
  - [ ] Navigation links scroll to correct sections
  - [ ] Scroll effect on navigation works
  - [ ] All buttons have hover states
  - [ ] Form submission works (if configured)
  - [ ] Animations trigger on scroll
  - [ ] No console errors

- [ ] **Content**
  - [ ] All text is in German
  - [ ] No spelling errors
  - [ ] Email addresses are correct
  - [ ] All links work
  - [ ] Brand consistency maintained

- [ ] **Browser Compatibility**
  - [ ] Chrome/Edge (Chromium)
  - [ ] Firefox
  - [ ] Safari
  - [ ] Mobile browsers

## Quick Reference

### Key Statistics Displayed
- **85%** - Possible time savings
- **24/7** - Automated processes
- **100%** - Individual solutions
- **0€** - Initial consultation
- **15+ hours** - Average time savings per week
- **500+** - Automated tasks per month possible
- **3-6 months** - Typical ROI amortization time

### Services Offered
1. KI-Chatbots (AI Chatbots)
2. Prozessautomatisierung (Process Automation)
3. Datenanalyse & Reports (Data Analysis & Reports)
4. E-Mail-Automatisierung (Email Automation)
5. System-Integration (System Integration)
6. KI-Beratung (AI Consulting)

### Navigation Menu Items
- Leistungen (Services) → #services
- Vorteile (Benefits) → #benefits
- Über uns (About) → #about
- Kontakt (Contact) → #contact

## Future Enhancement Ideas

Consider these for future iterations:

1. **Blog Section**: Add AI automation tips and case studies
2. **Portfolio/Case Studies**: Showcase completed projects
3. **Testimonials**: Client reviews and success stories
4. **FAQ Section**: Common questions about AI automation
5. **Pricing Calculator**: Interactive ROI calculator
6. **Chatbot Integration**: Live AI chatbot demo
7. **Multi-language Support**: English version for international clients
8. **Legal Pages**: Impressum (required in Germany), Privacy Policy (GDPR)
9. **Analytics Integration**: Google Analytics or privacy-friendly alternative
10. **Newsletter Signup**: Email list building

## Important Notes

### Legal Requirements (Germany)
- ⚠️ **Missing Impressum**: Required by German law (§5 TMG)
- ⚠️ **Missing Privacy Policy**: Required by GDPR
- ⚠️ **Cookie Notice**: May be needed if analytics are added

### Brand Identity
- **Company Name**: D&G AI-Consulting
- **Logo**: "D&G" in gradient box + "AI-Consulting" text
- **Tagline**: "KI-Automatisierung für Ihr Unternehmen"
- **USP**: Young entrepreneurs (18 years old), digital natives, modern AI solutions
- **Target Audience**: German businesses seeking AI automation

### Contact Information
- **Email**: julius@doennebrink-ai.de
- **Location**: Region Bonn, Deutschland
- **Response Time**: Within 24 hours
- **Founders**: Julius Dönnebrink (JD) & Nils Gerz (NG)

## Version History

- **v1.0** (2025-01-XX): Initial website launch
- **Current**: Single-page website with embedded styles and scripts

## Support and Maintenance

### When Issues Arise
1. **Broken links**: Check all anchor links and email addresses
2. **Styling issues**: Verify CSS variable values and responsive breakpoints
3. **JavaScript errors**: Check browser console, test Intersection Observer compatibility
4. **Form not working**: Verify Formspree configuration or alternative backend
5. **Font loading issues**: Check Google Fonts CDN, consider self-hosting

### Browser Support
- Modern browsers with ES6+ support
- CSS Grid and Flexbox support required
- Intersection Observer API support (polyfill may be needed for older browsers)

---

## For AI Assistants: Summary

This is a **simple, well-structured single-page marketing website** for a German AI consulting startup. When working on this project:

1. **Keep it simple** - No build tools, frameworks, or complex dependencies
2. **Maintain German language** - All user-facing content
3. **Follow the design system** - Use CSS variables consistently
4. **Test responsiveness** - Changes must work on all screen sizes
5. **Preserve the brand** - Young, modern, professional AI consulting image
6. **Ask before major changes** - Especially architecture or tech stack changes

The codebase is intentionally minimal and accessible for easy maintenance and quick deployment. Respect this simplicity while making improvements.
