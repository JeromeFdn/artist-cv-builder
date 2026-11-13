ARTIST CV BUILDER
Created by Jerome Foundation
https://www.jeromefdn.org
Hosted at: https://jeromefdn.github.io/artist-cv-builder
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ABOUT THIS TOOL

The Artist CV Builder is a free, browser-based tool that helps
artists create a polished, print-ready CV. It supports a wide
range of artistic fields and multidisciplinary practices, with
sections grouped by Jerome Foundation's seven artistic fields:
dance; film; literature; music; technology centered art;
theater, performance and spoken word; and visual art. Artists
fill in only the sections that apply to their work.

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

2. Fill in the form. The CV preview updates as you type. Work
   saves automatically in the browser; the status in the top
   bar confirms it.

3. Use the section list to move between sections. It is
   grouped by Jerome Foundation's seven artistic fields, each
   with its own sections and examples, plus General and Other.
   Field groups start folded; artists open the ones they work
   in. Dance, Music, and Theater each print as a separate
   section. Artists whose saved CV predates that split see a
   "Move this entry to" menu so they can sort old entries into
   Dance or Music; nobody else sees it. A number shows how many entries are in the CV; "hidden"
   means the section has content but is switched off. Blank
   sections never print.

4. Within a section, use "+ Add another entry," the up and
   down arrows to reorder entries, or "Sort newest first."
   Education accepts optional start and end months.

5. "Arrange your CV" (pinned under the section list) sets the
   order sections print in and the typeface. A writer who has
   also made films can move Published Works above Completed
   Films there.

6. "Save as PDF or print" walks through the print settings.
   "Copy text" copies a plain-text version for pasting into an
   application form or email.

7. "Back up or reset" downloads a backup file, loads one, or
   clears the form. Loading and clearing can be undone until
   the notice is dismissed.

8. If someone closes the page with edits they have not yet
   saved to PDF, copied, or backed up, the browser asks them
   to confirm. Browsers do not let a page set the wording of
   that prompt, so the tool shows its own reminder on the page
   behind it. To limit the prompt to real save failures, set
   WARN_ON_LEAVE to 'unsaved' near the top of the script.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ACCESSIBILITY

This tool targets WCAG 2.2 AA. As of November 2026 it passes
the automated axe-core checks for that level on every screen
and dialog. Automated checks catch only part of what matters,
so a pass with a screen reader is still worth doing after any
change. What is built in:

  - Every input has a visible, associated label
  - Text contrast of at least 4.5:1; control borders and focus
    rings at least 3:1
  - Text follows the reader's browser font size and zoom
  - Below about 960px, or at high zoom, the page becomes one
    column and scrolls normally
  - Everything works from the keyboard; reordering uses
    buttons, never dragging
  - Dialogs trap focus and return it when closed
  - Adding, moving, sorting, and removing are announced to
    screen readers; the preview itself is not read out on
    every keystroke
  - The PDF is tagged with real headings (name as heading 1,
    sections as heading 2)

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
  - Web fonts loaded from Google Fonts: Figtree for the tool
    and the sans-serif CV, Lora for the serif CV. Figtree
    replaced Barlow in November 2026; it runs a little wider,
    so a CV made before then may break lines differently.
  - Section-list icons are from Lucide (lucide.dev), ISC
    License, inlined as SVG. The Dance icon is Jerome
    Foundation's own.
  - Which section groups are folded shut is remembered under a
    separate key, "jerome_artist_cv_ui", apart from the CV.
  - User progress is saved to browser localStorage under the
    key "jerome_artist_cv_v3". The November 2026 update only
    adds to that data (education months, section order). The
    first time it runs it leaves a one-time copy of the
    existing save under "jerome_artist_cv_v3_before_2026_11".
  - Field keys in FIELD_CONFIG are the saved data keys. Labels
    can change freely; renaming a key hides what artists have
    saved under it.
  - Before November 2026, dance, music, and theater shared one
    "Performances & Productions" list (key "performances").
    That key is now the Theater section, and existing entries
    stay in it and print as before until the artist moves them.
    Dance ("dance_works"), music ("music_works"), and
    technology centered art ("tech_works",
    "tech_exhibitions") are new keys.
    Saves without a section order keep the old print order.
  - Section order lives in DEFAULT_ORDER and the artist's saved
    order. ENTRY_MAP defines how each section's entries print,
    and the preview and plain-text copy both read from it.
  - Print output uses a CSS @page margin box for page numbers.
    Chrome and Edge support it; other browsers may not.
  - Hosted via GitHub Pages (static file hosting).
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Last updated: November 13, 2026
