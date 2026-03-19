# Design System Strategy: Industrial Precision & The Engineering of Clarity

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Blueprint"**

In the industrial world of plastic manufacturing, precision is the ultimate form of trust. This design system moves away from the "generic corporate factory" aesthetic and toward a high-end, editorial experience that mirrors the technical accuracy of 山宏塑膠有限公司. 

The "Architectural Blueprint" approach treats the digital interface like a technical drawing: organized, spacious, and authoritative. We break the "template" look by utilizing **intentional asymmetry**—offsetting headings to one side of the grid—and using **layered depth** to suggest the physical stacking of materials like PE and BOPP. This is not just a website; it is a digital manifestation of manufacturing excellence.

---

## 2. Colors: Tonal Architecture
The palette is rooted in a deep, reliable `primary` (#003466) to anchor the brand, supported by a sophisticated range of `surface` and `secondary` tones that create professional polish.

*   **The "No-Line" Rule:** To achieve a premium feel, 1px solid borders for sectioning are strictly prohibited. Section boundaries must be defined solely by background shifts. For example, a `surface-container-low` (#f2f4f6) section should sit directly against a `surface` (#f8f9fb) background.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers. Use the `surface-container` tiers to create "nested" importance. 
    *   *Example:* Place a `surface-container-lowest` (pure white #ffffff) card on top of a `surface-container-high` (#e6e8ea) section to create a soft, natural lift.
*   **The Glass & Gradient Rule:** For floating navigation or product overlays, use **Glassmorphism**. Apply `surface-container-low` at 80% opacity with a `backdrop-filter: blur(20px)`. 
*   **Signature Textures:** Use subtle linear gradients for CTAs, transitioning from `primary` (#003466) to `primary_container` (#1a4b84) at a 135-degree angle. This adds "visual soul" and mimics the sheen of high-quality plastic materials.

---

## 3. Typography: Authority Through Scale
We use a high-contrast typographic scale to differentiate between "Technical Data" and "Brand Vision."

*   **Display & Headlines (Public Sans):** This typeface provides an industrial, geometric foundation. Use `display-lg` (3.5rem) for hero statements, ensuring tight letter-spacing (-0.02em) to maintain an authoritative, dense look.
*   **Titles & Body (Inter):** Inter provides neutral, high-legibility clarity for technical specifications of materials like PP and BOPP. 
*   **The Hierarchy Strategy:** Lead with an asymmetrical `headline-lg` (2rem) in `on_surface`, then follow with `body-lg` (1rem) in `on_surface_variant` (#424750) to create a clear visual path that doesn't overwhelm the reader.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "software-generic." We use **Ambient Depth** to convey the manufacturing context.

*   **The Layering Principle:** Depth is achieved by "stacking." A product card should not use a shadow to stand out; it should use a `surface-container-lowest` color against a `surface-dim` (#d8dadc) background.
*   **Ambient Shadows:** If a "floating" effect is required (e.g., a mobile dropdown menu), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(0, 52, 102, 0.06)`. Note the use of a blue-tinted shadow to match the `on_primary_fixed_variant` rather than a dead grey.
*   **The "Ghost Border" Fallback:** For input fields where definition is mandatory, use a "Ghost Border": the `outline_variant` (#c3c6d1) at 20% opacity. 

---

## 5. Components: Industrial Primitives

### Responsive Navigation Bar
*   **Desktop:** Asymmetrical layout. Logo pinned left, navigation links centered, and a high-contrast CTA (`primary`) pinned right. Use `surface_container_lowest` with a subtle `surface_tint` bottom-edge glow (2px).
*   **Mobile Dropdown:** Full-screen `surface_container_highest` (#e0e3e5) overlay with a 10% `backdrop-blur`. Links should use `headline-sm` for high-impact touch targets.

### High-Quality Product Cards (PE, PP, BOPP)
*   **Structure:** No dividers. Use `spacing-6` (1.5rem) of padding.
*   **Visual:** The top half contains a high-resolution product image. The bottom half sits on a `surface-container-low` background. 
*   **Content:** Material name in `title-lg`, technical specs in `label-md` using `on_surface_variant`. 
*   **Interaction:** On hover, the card should shift color from `surface-container-low` to `primary_container`, and text should transition to `on_primary_container`.

### Input Fields & Contact Sections
*   **Fields:** Background-filled using `surface_container_high`. No bottom line. Label sits in `label-sm` above the field in `outline`.
*   **Contact Section:** Use a two-column asymmetrical grid. Column 1 (40% width) contains the `headline-md` and "Trust Badges." Column 2 (60% width) contains the contact form on a `surface-container-lowest` "sheet."

---

## 6. Do's and Don'ts

### Do:
*   **Do** use `spacing-12` and `spacing-16` for vertical section breathing room. Industrial design needs space to feel "clean."
*   **Do** use `rounded-md` (0.375rem) for most components to balance "industrial" (sharp) with "modern" (accessible).
*   **Do** use `tertiary` (#522900) and its containers for "Industrial Alerts" or "New Material" badges to provide a sophisticated warm contrast to the blues.

### Don't:
*   **Don't** use 100% black text. Always use `on_surface` (#191c1e) for better optical comfort.
*   **Don't** use dividers or lines to separate list items. Use a slight background shift (alternate between `surface` and `surface_container_low`).
*   **Don't** use standard "Blue" icons. Use `on_secondary_container` (#4e6874) to keep icons professional and integrated.