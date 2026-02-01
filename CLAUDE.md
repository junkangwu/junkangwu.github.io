# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal academic homepage for Junkang Wu, hosted on GitHub Pages. It's a static website consisting of a single-page HTML document that showcases academic publications, news, education, and professional experience.

## Architecture

**Single-page static site**: The entire website is contained in `index.html` at the root level.

**Content structure**:
- Personal profile with photo and contact information
- News section (right sidebar) - recent conference acceptances and academic updates
- Education section - PhD and undergraduate information
- Publications section - organized by year (2026, 2025, 2024, 2023, 2021) with links to PDFs, code repositories, and slides
- Experience section - research internships
- Honors section - scholarships and awards
- Useful links section

**Assets organization**:
- `/files/` - CSS styles (`donghd.css`) and icons (`pdf.gif`)
- `/images/` - profile photos and name image
- `/slides/` - PDF presentation files
- `/wujk.github.io/` - appears to be an older version of the site

**Styling**: Custom CSS in `files/donghd.css` provides the layout, with a floating news sidebar on the right and main content on the left.

## Development Commands

This is a static HTML site with no build process. To work with it:

**Preview locally**: Open `index.html` directly in a browser, or use a simple HTTP server:
```bash
python -m http.server 8000
# Then visit http://localhost:8000
```

**Deployment**: Changes pushed to the `main` branch are automatically deployed to GitHub Pages.

## Content Update Patterns

**Adding new publications**: Publications are organized in reverse chronological order by year. Each entry follows this structure:
- Table with PDF icon link on left
- Title, authors (with **bold** for Junkang Wu), conference name with color badge, acceptance rate, and resource links (PDF, Codes, Slides)
- Conference badges use the `.conference` CSS class for styling

**Adding news items**: News entries in the `#news` section follow the format:
```html
<b>DD MMM YYYY</b><br>
<span class="easylink">
  News content with <a> tags
</span><br><br>
```

**Resource links**: Use the pattern `[<a href="..." target="_blank" style="color: #c05b4d; text-decoration: none;">Label</a>]` for PDF/Code/Slides links.

## Git Workflow

The repository uses `main` as the primary branch. Current status shows modifications to `index.html`.
