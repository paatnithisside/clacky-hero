# Clacky hero and design system

A new hero section for [clacky.app](https://clacky.app/) and the design system behind it, built as plain HTML, CSS and a little JS. No framework, no build step, no UI library.

- **Live hero:** https://clacky-hero.vercel.app/
- **Live design system:** https://clacky-hero.vercel.app/designsystem

## What is in here

| Path | What it is |
|---|---|
| `index.html` | The hero section, one self-contained file. |
| `designsystem/index.html` | The design system page: colour, type, space and shape, elevation, motion, the dotted desk, and every component at full viewport with its tokens. |
| `docs/clacky landing page copy and visual design brief.md` | The copy and visual brief: palette, art direction, motion rules, copy for every section. |
| `docs/Clacky-landing-page-conversion-audit.pdf` | The conversion audit of the current landing page: what to fix and why. |

## Start here (for an AI agent)

1. Read `docs/Clacky-landing-page-conversion-audit.pdf`, then `docs/clacky landing page copy and visual design brief.md`.
2. Open `designsystem/index.html`. Its `:root` block holds the tokens; each section lists the tokens and values one component uses.
3. Read `index.html` as the reference for how the components combine into a page.
4. Build the next section of the page from the same tokens and components. Do not invent a new palette or add a UI component library.

A prompt to begin with:

> Read `README.md`, the two files in `docs/`, and `designsystem/index.html`. Redesign the next section of the Clacky landing page (the one after the hero) using only the tokens and components in the design system. Follow the brief's copy, keep the headline and body sizes from the system, and show me the result as a single HTML file.

## Rules the system follows

- Every accent has one job: sky is selection and the playhead, sage is success, peach is a highlight, lilac is the cursor ripple.
- The dotted desk is the background of the whole page.
- Headline and body text never shrink to make room; the layout changes instead.
- Motion is one short procedure that ends on its final frame. `prefers-reduced-motion` shows the finished state.
- Product windows (Studio, Analytics, Task completed) are HTML mocks. Analytics is labelled "Sample data". Replace them with real captures when available.

## Things to know

- The design system page carries its own copy of the component CSS from `index.html`. If you change a token or component in one, change it in the other.
- Inter loads from Google Fonts. The Clacky mark is inlined from clacky.app's favicon; the name and mark belong to Clacky.
- Pricing, trial terms and macOS version wording change often. Check them against the live product before using them.
