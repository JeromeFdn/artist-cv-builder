ARTIST CV BUILDER
Created by Jerome Foundation
https://www.jeromefdn.org
Hosted at: https://jeromefdn.github.io/artist-cv-builder
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ABOUT THIS TOOL

The Artist CV Builder is a free, browser-based tool that helps
artists create a polished, print-ready CV. It supports a wide
range of artistic fields and multidisciplinary practices, with
sections grouped by discipline: performing arts, film,
literature, and visual and tech-centered art. Artists turn on
only the sections that apply to their work.

The tool is a single self-contained HTML file (index.html) with
no backend, no database, and no external dependencies beyond
web fonts. It runs entirely in the user's browser.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PRIVACY

This tool does not collect, transmit, or store any user data.
Everything an artist enters into the form stays on their own
device, saved in their browser's local storage. Jerome
Foundation has no access to any information entered into the
tool, and nothing an artist types is sent to GitHub or any
other server.

Two limits worth knowing. The page loads fonts from Google
Fonts, so the browser makes a request to Google when the tool
opens. That request carries no CV content, but it does reveal
the visitor's IP address to Google, as any embedded web font
would. And because saved progress lives in one browser on one
device, it does not follow the artist to another computer or
another browser. Clearing browser data, or working in a private
or incognito window, will discard saved progress.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
HOW TO USE

1. Visit the live tool URL:
   https://jeromefdn.github.io/artist-cv-builder

2. Fill in the form on the left. The CV preview on the right
   updates in real time as you type. Work saves automatically;
   the "Saved" indicator in the top bar confirms it.

3. Use the section navigation to move between sections.
   Sections with a green dot are included in the CV output.
   Toggle sections on or off using the checkbox at the top
   of each section form.

4. Within a section, use "+ Add Entry" for additional entries,
   and the up and down arrows on each entry to reorder them.

5. Choose a sans-serif or serif CV font in the Contact section.
   The *B* button in the top bar explains the simple formatting
   marks available for italics and bold.

6. When ready, click "Print / Save PDF" and follow the
   on-screen instructions to save a clean PDF. "Copy Text"
   copies a plain-text version of the CV to the clipboard for
   pasting into an application form or email.

7. "Clear Form" erases everything and cannot be undone.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ACCESSIBILITY

This tool is built to meet WCAG 2.0 AA accessibility standards,
including:

  - All form inputs have explicit label associations
  - All text meets minimum contrast ratios
  - Font sizes scale with browser text zoom settings
  - Keyboard navigation is fully supported
  - Screen reader announcements for live CV preview updates
  - Focus is managed after dynamic form changes
  - Skip link provided for keyboard users

Example text shown in gray inside a field is a sample, not
saved content, and it disappears as soon as the artist types.
Guidance that matters is printed below each field, where it
stays visible.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
UPDATING THE TOOL

The tool is maintained as a single file: index.html

To update it:

1. Go to the repository on GitHub
2. Click "Add file" then "Upload files"
3. Upload the new index.html (GitHub will overwrite the
   existing file automatically)
4. Scroll down and click "Commit changes"
5. GitHub Pages will rebuild within about 60 seconds

The live URL does not change when the file is updated.

Changing the localStorage key in the code will orphan every
artist's saved progress, so leave it alone unless the data
format changes in a way that makes old saves unreadable.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TECHNICAL NOTES

  - Built with plain HTML, CSS, and JavaScript. No frameworks,
    no build tools, no dependencies.
  - Web fonts loaded from Google Fonts (Barlow, Barlow
    Condensed, and Lora for the serif CV option).
  - User progress is saved to browser localStorage under the
    key "jerome_artist_cv_v3".
  - Section order is defined in three places that must stay in
    agreement: the nav grouping in SECTION_META, the preview in
    renderCV(), and the plain-text export in cvToPlainText().
  - Print output uses a CSS @page margin box for page numbers.
    Current browsers ignore this rule, so printed pages are
    unnumbered until that support arrives.
  - Hosted via GitHub Pages (static file hosting).
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Last updated: August 27, 2026
