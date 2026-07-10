# Design System Document

## 1. Overview & Creative North Star: "The Digital Embassy"
This design system moves away from the "bureaucratic form" and toward the "Digital Embassy"—an experience that is authoritative yet welcoming, sophisticated yet accessible. By combining the heritage of the Turkish Republic's visual identity with high-end editorial layouts, we create a sense of "Institutional Fluidity."

The Creative North Star is **Trust through Transparency.** We achieve this not with heavy borders or rigid grids, but through layered depth, intentional white space, and a "Glass & Light" philosophy. The interface should feel like a premium physical document—tactile, clean, and impossible to misinterpret.

---

## 2. Color Theory & Surface Architecture
We move beyond flat backgrounds. This system utilizes a "Tonal Atmosphere" where colors are not just fills, but indicators of depth and importance.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. Use `surface-container-low` for large content areas sitting on a `surface` background. This creates a soft, modern distinction that feels "grown" rather than "drawn."

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked premium materials:
- **Base Layer:** `surface` (#f6fafd) – The foundation.
- **Section Layer:** `surface-container-low` (#f0f4f7) – Used for grouping related content blocks.
- **Action Layer:** `surface-container-lowest` (#ffffff) – Reserved for interactive cards or primary input fields to make them "pop" against the background.

### The "Glass & Gradient" Signature
To provide visual "soul," use subtle linear gradients for primary CTAs and Hero sections:
- **Hero Backgrounds:** A soft transition from `primary` (#00214a) to `primary-container` (#1c3761).
- **Glassmorphism:** For floating navigation bars or modal headers, use `surface` at 80% opacity with a `20px` backdrop-blur. This ensures the brand colors "bleed through," keeping the user grounded in the interface.

---

## 3. Typography: The Editorial Authority
The typography scales are designed to balance the modernity of Public Sans with a structural, clear hierarchy.

- **Display & Headlines (`headline-lg` to `display-lg`):** These are your "Statement" tiers. Use them with tight letter-spacing (-0.02em) to create a bold, authoritative editorial feel. This is the "voice" of the state—clear and undeniable.
- **Title Tiers (`title-lg` to `title-sm`):** These act as the navigational anchors. They should always use the `on-surface` color to ensure maximum readability.
- **Body & Labels:** Use `body-md` as the standard for all functional information. To emphasize secondary information without adding "noise," drop the color to `on-surface-variant` rather than reducing font size.

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are often "dirty." We use **Ambient Depth** to guide the eye.

- **The Layering Principle:** Instead of a shadow, place a `surface-container-lowest` (#ffffff) card on a `surface-container` (#eaeef1) background. The 2-step color shift provides enough contrast for the eye to perceive a physical lift.
- **Ambient Shadows:** When a floating element (like a FAB or a Bottom Sheet) is required, use:
  - **Color:** `primary` at 6% opacity.
  - **Blur:** 24px to 32px.
  - **Spread:** -4px.
  - *Result:* A soft, blue-tinted glow that feels integrated into the brand's palette.
- **The "Ghost Border" Fallback:** If a border is required for high-accessibility contexts, use `outline-variant` at 15% opacity. Never use 100% opaque lines.

---

## 5. Components

### Buttons
- **Primary:** Rounded `xl` (1.5rem). Gradient fill from `primary` to `primary-container`. Typography: `title-sm` in `on-primary`.
- **Secondary:** Surface-only. No border. Fill with `secondary-fixed-dim`. This creates a "soft-touch" button feel.
- **Tertiary:** Text-only in `primary` color. Reserved for "Cancel" or "Learn More."

### Input Fields
- **Styling:** Forgo the traditional "box." Use a `surface-container-highest` background with a `bottom-stroke` only when focused. 
- **Corners:** `md` (0.75rem) on top corners to maintain a "document" feel.
- **States:** Errors must use `error` (#ba1a1a) text with a `error-container` (#ffdad6) subtle background glow.

### Cards & Lists
- **The "No-Divider" Rule:** Forbid 1px dividers between list items. Use `spacing-4` (1rem) of vertical white space or alternating subtle shifts between `surface-container-low` and `surface-container-lowest`.
- **Visual Grouping:** Use a `xl` (1.5rem) corner radius for cards to give them a friendly, modern tech-app appeal.

### Specialized Component: The "Status Ledger"
Specifically for e-Devlet contexts (tracking applications/documents):
- A vertical stack using "Tonal Steps." Each status item sits on a slightly different shade of the background, creating a natural flow of time and progress without a single line being drawn.

---

## 6. Do's and Don'ts

### Do:
- **DO** use asymmetry in headers. Align the logo left and a "Profile/Search" glass-circle right to break the "template" feel.
- **DO** use `secondary` (#13658b) for informational icons and `tertiary` (#4d0004) only for critical alerts.
- **DO** leverage the `xl` roundedness for all main containers to communicate safety and modern accessibility.

### Don't:
- **DON'T** use pure black (#000000) for text. Always use `on-surface` (#171c1f) to maintain the premium, soft-ink look.
- **DON'T** use "Drop Shadows" on cards. Use background color nesting first.
- **DON'T** crowd the interface. If a screen feels full, increase the spacing scale by one increment (e.g., move from `spacing-4` to `spacing-5`). Trust is built through breathing room.