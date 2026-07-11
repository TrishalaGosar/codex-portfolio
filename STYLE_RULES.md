# Portfolio Style Rules

Use these rules across all portfolio pages unless a page is intentionally treated as a sub-brand or experiment.

## Core Spacing Scale

- `4px`: hairline adjustments only
- `8px`: pill gap, icon gap, micro spacing
- `12px`: inline action gap
- `16px`: card internal rhythm, mobile inset
- `20px`: default side gutter on desktop pages
- `24px`: card padding start point
- `32px`: major block spacing inside hero and sections
- `56px`: hero bottom spacing
- `76px`: default top and bottom section spacing

## Page Container

- `.wrap`: `width: min(1160px, calc(100% - 40px))`
- Mobile `.wrap`: `width: min(100% - 28px, 1160px)`
- Use the same container width on all primary portfolio and case-study pages.

## Navbar

- Navbar min height: `80px`
- Navbar gap between brand and links: `20px` to `24px`
- Navbar background should be translucent, light, and blurred.
- Navbar border should be a single low-contrast bottom border only.
- Nav link padding: `10px 10px`
- Nav link font size: `0.94rem`
- Nav link weight: `540` to `580`
- Brand weight: `680` to `700`

## Hero

- Hero top padding: `68px` to `78px`
- Hero bottom padding: `54px` to `56px`
- Hero grid gap: `28px` to `72px` responsive
- Eyebrow margin bottom: `14px` to `16px`
- CTA row top margin: `28px` to `32px`

## Buttons

- Minimum height: `46px`
- Horizontal padding: `18px` to `20px`
- Use one radius system only per page family:
  - default portfolio system: `8px`
  - branded enterprise variant: `999px`
- Button font weight: `600` to `640`
- Keep primary and secondary button heights identical.
- Do not mix square, rounded-pill, and sharp button treatments on the same page.

## Cards And Panels

- Standard card padding: `22px` to `24px`
- Standard radius:
  - default portfolio system: `8px`
  - premium/branded variant: `18px` to `24px`
- Keep one radius family per page.
- Grid gaps between cards: `14px` to `16px`

## Sections

- Default section spacing: `76px 0`
- Mobile section spacing: `58px 0`
- Section heading bottom spacing before content: `30px`
- If section dividers are used, apply them consistently across all major sections on that page.

## Pills / Tags

- Padding: `6px 9px` or `7px 11px`
- Gap between pills: `8px`
- Add `6px` bottom margin below the pill row when a footer link follows.
- Pill treatment should support the page palette, not introduce new colors.

## Typography

- Body/UI font: `Inter`
- Display/section headline font: `Georgia` for current system
- Avoid introducing extra display fonts unless a page is intentionally experimental.
- Keep nav, pills, buttons, and metadata visually quieter than headings.

## Color Governance

- Core base: `ink`, `muted`, `paper`, `surface`, `line`
- Core brand accents: `sage`, `terra`, `gold`, `sky`
- Atmosphere colors like `aqua` and `orchid` should stay mostly in gradients and hover surfaces.
- Do not introduce a separate SaaS-style palette on one page unless that page is intentionally isolated from the portfolio brand.

## Propagation Priority

Apply consistency in this order:

1. `index.html`
2. `CX+.html`
3. `art-galore.html`
4. `ai-assistant-for-education.html`
5. `games/index.html`

Treat these as optional outliers unless you want full unification:

- `experiment/index.html`
- `tv-competitor-analysis.html`
- `test.html`

## Responsive Rule: Mandatory For All Pages

Every current and future page must be responsive by default.

### Required Breakpoints

- Desktop base: `> 920px`
- Tablet and small laptop: `<= 920px`
- Mobile: `<= 620px`

Add these breakpoints to every page unless a page has a very specific reason to use additional ones.

### Layout Rules

- Never rely on fixed page widths for primary content.
- Use `width: min(..., calc(100% - ...))` containers instead of hard pixel page shells.
- Multi-column layouts must collapse to `1fr` on tablet or mobile.
- Hero sections must stack on smaller screens.
- Side minimaps, floating chrome, and decorative side elements must hide or reposition on mobile.
- Horizontal scroll should only exist for intentional components like project rails, never for the page itself.

### Spacing Rules

- Desktop page gutter: `40px` total subtraction pattern
- Mobile page gutter: `28px` total subtraction pattern
- Desktop section spacing: `76px 0`
- Mobile section spacing: `58px 0`
- Reduce hero height from full-screen compositions to content-height layouts on smaller screens.

### Typography Rules

- Headline sizes must use `clamp(...)`, not fixed pixel sizes.
- Body copy must remain readable on mobile without zooming.
- Avoid `white-space: nowrap` on major headings unless there is a safe mobile override.
- Long labels and metadata rows must be allowed to wrap.

### Component Rules

- Navigation must switch to wrapped or stacked layout on mobile.
- Buttons in action rows must wrap cleanly.
- Cards in grids must collapse to one column on mobile.
- Images, iframes, and videos must use fluid width and bounded aspect ratios.
- Embedded content must not overflow its parent card.

### Media Rules

- Images: `width: 100%`, `height: auto`
- Videos/iframes: use aspect-ratio containers or explicit mobile height rules
- Large illustrations must scale down before causing horizontal overflow

### QA Rule

Before any page is considered complete, check:

- no horizontal overflow at mobile width
- readable heading hierarchy on phone screens
- CTA buttons wrap without collision
- nav remains usable on small screens
- embedded media remains visible and contained
- section spacing still feels intentional after stacking

### Future Page Rule

Any new HTML page added to this portfolio must include:

- the standard `.wrap` responsive container
- the standard tablet and mobile media queries
- stacked mobile behavior for hero, sections, grids, and navigation
- fluid media sizing for images and embeds
