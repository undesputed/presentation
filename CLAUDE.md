# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a standalone HTML5 slide presentation about an AI-powered Project Management tool. The entire project is a single file: `presentation.html` (with `logo.png` for the cover slide).

## Running the Presentation

Open `presentation.html` directly in any modern web browser — no build step, no dependencies, no install required.

## Architecture

**Single-file structure**: All HTML, CSS, and JavaScript are embedded in `presentation.html`. There are no external JS libraries (vanilla JS only). External resources are limited to Google Fonts and Simple Icons CDN (with emoji fallbacks).

**16 slides** organized into sections: Problem → Solution → Mission & Vision → Demo. Section boundaries use full-screen "section break" slides.

**Navigation system** (`goTo`, `next`, `prev`, `jumpSection`, `updateUI`):
- Keyboard: arrow keys, spacebar
- Touch: swipe left/right (50px threshold)
- Bottom dots: jump to section starts
- Slide 15 (Live Workflow) has special logic — `→` reveals the 5 workflow steps one at a time before advancing; `resetWorkflow()` resets on re-entry

**CSS design tokens** (defined as `--` variables at `:root`):
- Primary dark: `#0F172A`, accent blue: `#1D4ED8`
- Fonts: Syne (headers, 800w), Epilogue (body), Noto Sans JP (Japanese text)
- Fluid typography via `clamp()`

**Slide entry animation**: 550ms cubic-bezier transition on `.slide.active`; child elements use staggered `animation-delay` (0.1s–0.5s) via `.fade-up` class.
