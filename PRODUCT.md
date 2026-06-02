# Product

## Register

brand

## Users

Two audiences land here. First, Google AdSense reviewers evaluating whether the
site hosts meaningful, original content before approving ads on the free games.
Second, visitors who arrive from one of the projects (e.g. the 2048 solver) or
from a search and want to see what else Rex builds. Both scan quickly: the
reviewer is checking for substance and polish, the visitor is deciding whether
to click into a project.

Their job-to-be-done: in a few seconds, understand that this is a real person's
real body of work, and find the project worth opening next.

## Product Purpose

This is the root index page for `rlorenzo.github.io`: a hub that points to Rex's
projects, games, and experiments. It exists to (1) present a credible, content-rich
front door for Google AdSense approval so ads can run on the free games, and
(2) route visitors into the individual projects.

The design is the product. It must read as the work of someone who ships quality
software, and it must stay visually consistent with the main portfolio at
`rlorenzo.github.io/portfolio` so the two surfaces feel like one identity.

Success looks like:

- A reviewer or visitor immediately reads the page as intentional and real, not a
  thin placeholder or a template.
- Every project on the page is one click away, with enough description to convey
  what it is and why it's worth opening.
- The page is visually indistinguishable in voice and craft from the portfolio:
  same palette, same type, same editorial restraint.

## Brand Personality

Inherited from the portfolio so the two surfaces read as one person: **seasoned,
pragmatic, approachable.** For this hub specifically, add **curious** — Rex builds
to find out what's possible with AI tools and agents, so the copy is warmer and more
exploratory than the resume voice. Do NOT frame him as a "game maker": games are one
output of that exploration, not his identity.

- Voice: first-person, direct, plainspoken. Confidence without bravado.
- Tone: warm, builder-to-builder. "Here's what I've been exploring," not marketing.
- Emotional goal: this is someone curious who makes things worth your click.

## Anti-references

This page should explicitly NOT look like:

- **Generic dev-portfolio templates.** Identical icon-heading-text card grids,
  decorative glow gradients on hover, oversized serif numerals as ornament,
  grain-overlay-for-texture. The previous version of this page leaned on several
  of these; they are what to design away from.
- **A different brand from the portfolio.** Drifting palette, a second typeface,
  or a different elevation language would make the two surfaces look like two
  unrelated sites. Identity consistency with `/portfolio` wins.
- **A thin AdSense doorway page.** A hero plus two bare links reads as a
  placeholder to a reviewer. The content must demonstrate real substance.
- **AI-generated portfolio look.** Blue-to-purple gradients, glassmorphism, eyebrow
  kickers above every section, FontAwesome icons inline with headings.

## Design Principles

1. **One identity across both surfaces.** This hub and the `/portfolio` site share
   palette, typography, elevation, and motion. A visitor moving between them should
   never feel a seam. The portfolio's DESIGN.md is the source of truth.
2. **Earn every flourish.** No glow, grain, or decorative numeral survives unless it
   does real work. Hairlines, tints, and whitespace before shadows; weight and scale
   before extra color.
3. **Show the work, route to it.** The projects are the point. Push real, specific
   descriptions of each project above any performative chrome, and make the path into
   each one obvious.
4. **One confident voice.** Copy is the same person as the portfolio: first-person,
   plainspoken, no marketing verbs, no em dashes.
5. **Credible on both ends.** Reviewers open it on desktop; players arrive on phones.
   It has to feel intentional at every width, in both light and dark themes.

## Accessibility & Inclusion

- WCAG 2.1 AA as the floor. Color contrast holds in both light and dark themes.
- Respect `prefers-reduced-motion`: every animation has a reduced-motion alternative.
- All interactive elements are keyboard-reachable with a visible focus state. Inline
  SVG icons that are the sole content of a control carry an accessible name.
- Theme toggle persists across visits and prevents a flash of the wrong theme (FOUC).
