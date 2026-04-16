# AI Assistant PM Tool — Slide Deck

A standalone HTML5 slide presentation for an AI-powered project management tool. Everything runs in the browser with no build step or package install.

## Quick start

1. Open `presentation.html` in a modern desktop or mobile browser (double-click the file, or use **File → Open**).

That’s it — no server required for local viewing.

## What’s in the repo

| File | Purpose |
|------|---------|
| `presentation.html` | Full deck: HTML structure, embedded CSS, and vanilla JavaScript |
| `logo.png` | Cover slide asset |
| `CLAUDE.md` | Notes for AI-assisted editing (architecture and conventions) |

## Navigation

- **Keyboard:** Arrow keys or Space to move between slides  
- **Touch:** Swipe left/right (about 50px)  
- **Bottom dots:** Jump to the start of each major section  

**Live Workflow slide:** On that slide, the right arrow reveals workflow steps one at a time before moving to the next slide. Re-entering the slide resets the sequence.

## Structure

The deck has **16 slides** in four parts: **Problem → Solution → Mission & Vision → Demo**, with full-screen section breaks between themes.

Styling uses CSS custom properties on `:root` (e.g. dark `#0F172A`, accent `#1D4ED8`). Typography: **Syne** (headings), **Epilogue** (body), **Noto Sans JP** (Japanese text), loaded from Google Fonts. Icons may use the Simple Icons CDN with emoji fallbacks.

## Editing

All markup and behavior live in `presentation.html`. There are no external JavaScript libraries — only vanilla JS. For deeper detail (slide count, navigation helpers, animations), see `CLAUDE.md`.

## Requirements

- A current browser (Chrome, Firefox, Safari, Edge, etc.)  
- Network optional after first load if fonts/icons are cached; for fully offline use, you’d need to self-host fonts or accept fallbacks  

---

*Title in the deck: Carrie Yu — AI Assistant PM Tool*
