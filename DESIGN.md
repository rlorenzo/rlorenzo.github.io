---
name: Rex Lorenzo Index
description: Root hub page for rlorenzo.github.io; shares the portfolio's design system so the two surfaces read as one identity.
colors:
  brand: "oklch(53% 0.14 50)"
  brand-deep: "oklch(38% 0.11 50)"
  brand-soft: "oklch(96% 0.025 60)"
  paper: "oklch(98% 0.008 60)"
  paper-soft: "oklch(95% 0.014 60)"
  rule: "oklch(88% 0.012 60)"
  ink: "oklch(22% 0.012 50)"
  ink-soft: "oklch(46% 0.012 50)"
  brand-dark: "oklch(75% 0.13 55)"
  brand-deep-dark: "oklch(85% 0.10 55)"
  brand-soft-dark: "oklch(28% 0.045 50)"
  paper-dark: "oklch(18% 0.008 50)"
  paper-soft-dark: "oklch(22% 0.011 50)"
  rule-dark: "oklch(30% 0.013 50)"
  ink-dark: "oklch(95% 0.008 50)"
  ink-soft-dark: "oklch(72% 0.012 50)"
typography:
  body:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontWeight: 400
    lineHeight: 1.5
  display:
    fontFamily: "Bricolage Grotesque, system-ui, sans-serif"
    fontWeight: 600
    lineHeight: 1.0
rounded:
  control: "4px"
  card: "0.5rem"
spacing:
  transitionFast: "0.15s"
  transitionNormal: "0.3s"
  transitionSlow: "0.5s"
  ease: "cubic-bezier(0.22, 1, 0.36, 1)"
---

<!-- markdownlint-disable-next-line MD025 -->
# Design System: Rex Lorenzo Index

> **This page shares the portfolio's design system.** The canonical source is
> `rlorenzo.github.io/portfolio`'s own DESIGN.md. This file records how that system
> is applied to the single self-contained `index.html` at the site root. When the
> portfolio's tokens change, update them here too so the two surfaces stay in sync.

## 1. Overview

**Creative North Star: "The Practitioner's Portfolio," front door edition.**

The root index is a hub that routes to Rex's projects and games and serves as the
content-rich page submitted to Google AdSense. It inherits the portfolio's voice:
the design is the work sample, typography breathes, motion earns its frame budget,
copy is one confident first-person voice. The only divergence is tone: this surface
is allowed to be a little more playful, because it points at games and experiments
rather than a resume.

**Key characteristics:**

- Brand register. The page IS the product.
- Single self-contained HTML file with inline critical CSS. No build step; right
  for a tiny static root page on GitHub Pages (deployed with `path: .`).
- Light theme default; dark theme opt-in via a persisted toggle, with FOUC prevention.
- Flat. Hairline `--rule` borders and `--paper-soft` fills separate surfaces; no
  decorative shadows, no grain, no glow.
- Type-led, editorial. Projects are a list, not a card grid.
- Motion respects `prefers-reduced-motion`.
- WCAG 2.1 AA floor in both themes.

## 2. Colors

Identical to the portfolio: one warm-amber brand hue plus warm-tinted neutrals, in
`oklch`. Light and dark share the hue; only lightness shifts. No second accent hue;
emphasis comes from weight, scale, and rule lines.

- **Brand** `oklch(53% 0.14 50)` (light) / `oklch(75% 0.13 55)` (dark): links on
  hover, the role line, the project arrow, chapter mark, focus ring.
- **Paper / Paper Soft / Rule:** page background, sunken sections, hairlines.
- **Ink / Ink Soft:** body text and headings / secondary text.

**The Single-Hue Rule** and **The Tint-Over-Color Rule** carry over from the
portfolio. One brand color per screen; reach for `--brand-soft`/`--paper-soft`
before a second hue.

## 3. Typography

**Bricolage Grotesque** (variable, 400 to 700), `system-ui, sans-serif` fallback.
One family carries everything; weight and size do the hierarchy. Headings set
`font-variation-settings: 'opsz' <size>, 'wdth' 100` to match the portfolio's
optical sizing, with tight negative tracking on display sizes.

- **Display** (600, fluid clamp, line-height ~1.0): hero name.
- **Headline** (600, clamp ~2.25–3.25rem): section heading ("Projects").
- **Title** (600, ~1.4–1.9rem): project name.
- **Body / Lede** (400, line-height 1.5–1.6): paragraph and lede copy.
- **Label** (600, 0.75rem, uppercase, tracked): chapter mark numeral.

Carried-over copy rules: **One Voice**, **No-Repeat** (no section intro restates its
heading), **No-Em-Dash**.

## 4. Elevation

Flat-first, same as the portfolio. Hairline `--rule` + `--paper-soft` fills + white
space before any shadow. The fixed header gains a `--rule` bottom border only after
the page scrolls past a threshold.

## 5. Components

- **Header:** fixed top, `--paper` background, transparent bottom border that becomes
  `--rule` once scrolled; wordmark fades in on scroll; theme toggle; skip link.
- **Hero:** type-led, asymmetric, staggered entrance. Name + role line + lede + a
  utility row of profile links (GitHub, LinkedIn) using inline SVG icons.
- **Projects:** editorial list (`projects__row--featured` two-column grid on desktop:
  title/tech left, description right), hairline dividers, title link with a
  hover-revealed arrow, tech as `·`-separated text. No cards, no chips, no glow.
- **Chapter mark:** small uppercase tracked numeral with a trailing brand rule,
  punctuating the Projects section. Used once, deliberately, not as per-section grammar.
- **Footer:** editorial colophon. Hairline rule, wordmark + copyright, profile links,
  a typeface/stack credit line.

## 6. Do's and Don'ts

### Do

- **Do** keep tokens in lockstep with the portfolio's DESIGN.md.
- **Do** keep the palette to one brand hue plus warm neutrals.
- **Do** respect `prefers-reduced-motion` on every animation.
- **Do** keep a visible focus ring on every interactive element.
- **Do** keep copy in the no-em-dash, one-voice style.

### Don't

- **Don't** reintroduce the grain overlay, hover glow gradients, oversized serif
  numerals, or card grid from the previous version.
- **Don't** add a second brand hue, a second typeface, or gradient text.
- **Don't** add an eyebrow kicker above every section; the chapter mark is used once.
- **Don't** let the page read as a thin AdSense doorway: each project carries a real,
  specific description.
