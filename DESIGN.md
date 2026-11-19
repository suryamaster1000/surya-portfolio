# Design System: Surya Neerukonda Portfolio

## 1. Visual Theme & Atmosphere
A dark, engineering-forward personal portfolio that feels like a live creative coding console. Dense but legible, with a wide asymmetrical hero, hairline grid lines, tiny uppercase metadata, and vivid mint signals against deep forest-black surfaces. Density 7/10, variance 6/10, motion 4/10. Motion should clarify interaction and lend the orbital graphic life without distracting from the work.

## 2. Color Palette & Roles
- **Night Canvas** (#07100E) — Primary page background.
- **Forest Panel** (#0C1713) — Hero art and elevated work surfaces.
- **Console Surface** (#101A17) — Metric tiles and interactive panels.
- **Mint Signal** (#55E6B3) — Single accent for active links, fine rules, and primary actions.
- **Paper Ink** (#E8F1ED) — Main headings and body copy.
- **Quiet Label** (#84948D) — Secondary text, labels, and timestamps.
- **Grid Trace** (#1C2B25) — Fine structural borders and orbital lines.

## 3. Typography Rules
- **Display:** DM Sans, bold, tightly tracked, responsive via `clamp()`.
- **Body:** DM Sans, relaxed leading, limited to roughly 65 characters per line.
- **Mono:** DM Mono for navigation labels, section indices, metadata, and stats.
- Use uppercase mono labels sparingly; preserve readability at mobile sizes.

## 4. Component Stylings
- **Buttons:** Mint rectangular primary action with crisp edges, clear hover shift, and tactile active press. Secondary action is quiet text with a thin rule.
- **Panels:** Dark surfaces with thin green-grey borders and slight radius. Reserve filled panels for the hero visualization and metric hierarchy.
- **Navigation:** Compact horizontal mono links, active/hover color in mint; collapses to wrapped links on narrow screens.
- **Orbital graphic:** SVG rings, nodes, and labelled destinations; all labels remain separate and readable. Subtle rotation only on ring strokes.
- **Focus:** Visible mint outline with sufficient offset. Minimum 44px interactive targets on touch layouts.

## 5. Layout Principles
- Wide contained canvas (max 1440px), 12-column desktop rhythm, split hero with copy on left and orbital visualization on right.
- The hero is followed by a four-part stat strip, then work, skills, journey, and contact sections.
- Use fine separators and intentional negative space; cards are compact because the reference is console-dense.
- Collapse all multi-column layouts to one column below 760px. Prevent horizontal overflow.

## 6. Motion & Interaction
- Use short opacity and transform transitions for hover, reveal, and menu states.
- The orbital SVG may rotate slowly; pause decorative movement when `prefers-reduced-motion: reduce` is set.
- Keep all animation compositor-friendly and avoid layout-affecting motion.

## 7. Anti-Patterns (Banned)
- No purple or neon glow effects, no gradients as decoration, no pure-black canvas.
- No generic three-column feature-card row, emojis, custom cursor, or oversized centered hero.
- No overlapping text and graphics, fake metrics, filler scroll prompts, or placeholder project names.
- Keep personal facts and project links grounded in the existing portfolio content.
