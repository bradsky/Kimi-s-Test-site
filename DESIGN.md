# Design System Strategy: The Curated Ritual

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Curated Ritual."** We are not building a generic e-commerce platform; we are designing a digital gallery that honors the precision and clarity of the coffee-making process. 

To achieve a "High-End Editorial" feel, we move away from standard boxed layouts. We embrace **Asymmetric Zen**—a layout philosophy where intentional whitespace acts as a structural element, and high-quality photography is treated as fine art rather than a mere asset. By utilizing overlapping elements (e.g., a display headline slightly breaking the bounds of a product image) and extreme typographic contrast, we create an experience that feels human, intentional, and premium.

---

## 2. Colors: Tonal Depth vs. Structural Lines
Our palette is rooted in the iconic "Blue Bottle Blue," but its application must be surgical. We use color to define space, never lines.

*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Boundaries must be defined through background shifts. For example, a transition from `surface` (#f9f9f9) to `surface-container-low` (#f3f3f4) provides a sophisticated, soft-touch separation that feels integrated rather than partitioned.
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers.
    *   **Base Layer:** `surface` (#f9f9f9).
    *   **Interactive/Elevated Layer:** Use `surface-container-lowest` (#ffffff) for cards to create a subtle "lift."
    *   **Feature Layer:** Use `surface-container-highest` (#e2e2e2) for utility sidebars or secondary content areas.
*   **The "Glass & Gradient" Rule:** To avoid a flat, "out-of-the-box" look, floating elements (like a navigation bar or a sticky "Add to Cart" mobile bar) should use `surface_container_lowest` at 80% opacity with a `20px` backdrop-blur. 
*   **Signature Textures:** For primary CTAs, use a subtle linear gradient from `primary` (#006688) to `primary_container` (#00a9e0). This adds a "jewel-like" depth that a flat hex code cannot achieve.

---

## 3. Typography: The Editorial Voice
We use **Manrope** across all scales to maintain a clean, sans-serif modernism. The hierarchy is designed for "Scan-and-Savor" reading.

*   **Display & Headline:** Use `display-lg` (3.5rem) and `headline-lg` (2rem) to create emotional impact. These should be paired with generous tracking (letter-spacing: -0.02em) to feel tighter and more premium.
*   **Body & Labels:** `body-md` (0.875rem) is our workhorse. Use `label-md` (0.75rem) in all caps with increased tracking (+0.05em) for category headers or technical coffee specs (e.g., "ORIGIN: ETHIOPIA") to mimic high-end print magazines.
*   **The High-Contrast Gap:** Avoid using too many font sizes on one screen. Pair a `display-md` headline directly with `body-md` text. The large "jump" in scale creates a sophisticated, minimalist aesthetic.

---

## 4. Elevation & Depth: Tonal Layering
Depth in this design system is felt, not seen. We reject heavy drop shadows in favor of **Ambient Light.**

*   **The Layering Principle:** Instead of shadows, stack tiers. A `surface-container-lowest` card placed on a `surface-container-low` background creates a natural, soft-edge definition.
*   **Ambient Shadows:** When an element must float (e.g., a modal), use a highly diffused shadow: `box-shadow: 0 20px 40px rgba(26, 28, 28, 0.06)`. Note the color: we use a tint of `on-surface` (#1a1c1c), never pure black, to keep the shadow "organic."
*   **The "Ghost Border" Fallback:** If accessibility requires a border (e.g., in high-contrast modes), use `outline-variant` (#bdc8d0) at 15% opacity. It should be barely perceptible.
*   **Glassmorphism:** Use backdrop blurs to allow the high-quality coffee photography to "bleed" through the UI, softening the edges of the digital experience and making the interface feel like a lens.

---

## 5. Components: Precision & Purpose
Components are the "tools" of the ritual. They should feel tactile and refined.

*   **Buttons:**
    *   **Primary:** Gradient from `primary` to `primary_container`. `DEFAULT` (0.25rem) roundedness. No border.
    *   **Secondary:** `surface-container-highest` background with `on-surface` text. 
    *   **Tertiary:** Text-only using `primary` color, with a 2px underline that appears only on hover.
*   **Input Fields:** Avoid the "box" look. Use a `surface-container-low` background with a bottom-only stroke of `outline-variant` (20% opacity). On focus, transition the stroke to `primary`.
*   **Cards & Lists:** **Strictly no divider lines.** Separate items using the Spacing Scale `8` (2.75rem) or `10` (3.5rem). Use "The Hero Plinth" layout: an image that takes up 60% of the card width, with text overlapping the image slightly to break the grid.
*   **Chips:** Use `secondary_fixed` (#e2e2e2) for inactive states and `primary_fixed` (#c2e8ff) for active states. Keep them small (`label-sm`) and Pill-shaped (`full` roundedness).

---

## 6. Do's and Don'ts

### Do:
*   **Embrace the Asymmetry:** Place a product image off-center and counter-balance it with a `display-sm` headline on the opposite side.
*   **Use White Space as a Feature:** If a section feels "empty," leave it. White space in this system represents the premium nature of the brand.
*   **Prioritize Photography:** Every screen should be anchored by a high-resolution image. Use the `surface_dim` color as a placeholder to maintain the tonal mood while images load.

### Don't:
*   **Don't Use Pure Black:** Always use `on_surface` (#1a1c1c) for text to maintain a soft, ink-on-paper feel.
*   **Don't Use Default Shadows:** Avoid the "floating box" look of 2010-era Material Design.
*   **Don't Over-Corner:** While we have an `xl` roundedness scale, use it sparingly. The `DEFAULT` (0.25rem) is our signature—it provides a sharp, professional architectural feel without being "bubbly."
*   **Don't Use Icons in Isolation:** Icons should always be accompanied by a `label-sm` or be extremely intuitive (e.g., Search, Cart). We prefer text-based navigation for an editorial look.