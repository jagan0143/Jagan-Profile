# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page portfolio website for Jaganath N (NodeJS Developer & Solution Analyst). The site is hosted on GitHub Pages with a custom domain.

## Repository Structure

- `index.html` - Single-page portfolio with all HTML, CSS (embedded in `<style>`), and JavaScript (embedded in `<script>`)
- `Profile Photo.jpg` - Profile image used in the hero section
- `resume.pdf` - Downloadable resume
- `CNAME` - Custom domain configuration for GitHub Pages (jagan.dordie.in)

## Architecture

The entire website is contained within a single HTML file with:
- **Embedded CSS** (lines 9-1107): Custom CSS variables, responsive design, animations, and component styles
- **Inline JavaScript** (lines 1491-1562): Smooth scroll navigation, scroll animations via IntersectionObserver, and form submission handling
- **Sections**: Hero, About, Skills, Experience, Education, Projects, Contact

## Working with This Site

### Making Style Changes
All styles are embedded in the `<style>` tag (lines 9-1107). CSS custom properties are defined in `:root` (lines 10-24) for consistent theming.

### Modifying Content
Content is directly in the HTML. Key sections are marked with semantic IDs: `#about`, `#skills`, `#experience`, `#education`, `#projects`, `#contact`.

### Testing Changes
Open `index.html` directly in a browser - no build process required. For live testing, use a simple HTTP server like `python -m http.server` or VS Code's Live Server extension.

### Deployment
Changes pushed to the `master` branch are automatically deployed to GitHub Pages at the custom domain configured in CNAME.

## Design System

- **Color Scheme**: Dark theme with accent colors (teal primary, orange secondary, purple tertiary)
- **Typography**:
  - Playfair Display (headings)
  - Source Code Pro (code/monospace elements)
  - DM Sans (body text)
- **Responsive**: Mobile-first approach with breakpoints at 768px, 992px, and 1200px

## Contact Form

The form submission (lines 1529-1562) currently shows a client-side success message without sending data to a backend. To enable actual email delivery, integrate with a service like FormSubmit, Formspree, or a custom API endpoint.
