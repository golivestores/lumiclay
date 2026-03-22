```markdown
# Design System: Tactile Serenity

## 1. Overview & Creative North Star
**Creative North Star: "The Curated Atelier"**

This design system rejects the frantic, crowded nature of traditional e-commerce. Instead, it mirrors the experience of a high-end pottery gallery—quiet, intentional, and deeply tactile. We move beyond the "template" look by utilizing **Asymmetric Breathing Room**. 

Rather than centering every element, we use the spacing scale to create "pockets of silence" that allow the organic shapes of the pottery to speak. The interface should feel like a series of physical layers—hand-pressed paper, raw clay, and smooth glaze—stacked with deliberate care.

---

## 2. Colors: The Earth & The Kiln
The palette is rooted in the natural world, moving from the scorched earth of `charcoal` to the soft, light-reflective quality of `sand`.

### Surface Hierarchy & Nesting
To achieve a premium look, we never use lines to separate content. We use **Tonal Nesting**.
- **Base Layer:** `surface` (`#fafaf5`) – The "gallery wall."
- **Content Blocks:** `surface-container-low` (`#f3f4ee`) – A subtle shift to define a region.
- **Floating Details:** `surface-container-lowest` (`#ffffff`) – Used for cards or overlays to create a "bleached" highlight effect.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. A change in background color from `surface` to `surface-container-high` (`#e5eae0`) is the only permitted method for sectioning. This ensures the layout feels "poured" rather than "constructed."

### Signature Textures
Apply a subtle linear gradient to hero backgrounds or large CTAs: 
- From `secondary_container` (`#f4e0be`) to `secondary_fixed_dim` (`#e6d2b0`). This mimics the variegated texture of natural clay.

---

## 3. Typography: Editorial Sophistication
We pair a high-contrast serif with a functional, modern sans-serif to bridge the gap between ancient craft and digital precision.

*   **Display & Headlines:** `notoSerif`. Use `display-lg` (3.5rem) for hero moments. The elegant serifs reflect the "rim" of a vessel.
*   **Body & Utility:** `manrope`. A clean, open sans-serif that ensures readability against textured backgrounds.
*   **The Intentional Scale:** Always use a "Leap" in scale. Pair a `headline-lg` with `body-sm` metadata to create an editorial, magazine-like hierarchy. Avoid using mid-range sizes (like `title-md`) in the same view as headlines to prevent visual "mud."

---

## 4. Elevation & Depth
In this system, depth is a suggestion of light, not a physical drop shadow.

*   **The Layering Principle:** Stacking `surface-container-highest` on top of `surface-dim` creates a natural sense of weight.
*   **Ambient Shadows:** For floating elements (like a "Cart" drawer), use an ultra-diffused shadow: `blur: 40px`, `opacity: 6%`, using the `on_surface` (`#2e342d`) color. It should look like a soft shadow cast on a studio floor.
*   **Glassmorphism:** Use `surface_bright` at 80% opacity with a `20px backdrop-blur` for navigation bars. This allows the pottery colors to bleed through as the user scrolls, maintaining a sense of continuity.
*   **The "Ghost Border" Fallback:** If a container must be defined on a similar background, use `outline_variant` at **15% opacity**. It should be barely felt, not seen.

---

## 5. Components

### Buttons: The "Glaze" Interaction
*   **Primary:** Background: `secondary` (`#6c5d42`); Text: `on_secondary`. Shape: `xl` (1.5rem) for a softened, pebble-like feel.
*   **Secondary:** Background: `transparent`; Border: `Ghost Border` (outline-variant @ 20%).
*   **Tertiary:** Text: `primary`. No container. Underline only on hover using a 1px `primary_container` stroke.

### Input Fields: The "Hand-Pressed" Look
*   **Style:** No background. Only a bottom border using `outline_variant`. 
*   **Focus State:** The bottom border transitions to `secondary`. Labels (`label-md`) float above in `on_surface_variant`.

### Cards & Lists: Organic Grouping
*   **Forbid Dividers:** Never use `<hr>` tags.
*   **The Gap Rule:** Use `spacing-12` (4rem) to separate list items. Use background shifts (`surface-container-low`) for hover states rather than boxes.
*   **Image Treatment:** Pottery images should use the `lg` (1rem) corner radius to mimic the roundness of the wheel.

### Additional Signature Component: The "Process Chip"
*   **Usage:** Used to denote "Hand-thrown," "Pit-fired," or "Local Clay."
*   **Style:** Small, pill-shaped (`full` roundedness) using `tertiary_container` with `on_tertiary_container` text. These should look like small maker's marks.

---

## 6. Do’s and Don'ts

### Do:
*   **Embrace Asymmetry:** Place a product image at 60% width and the description at 30% width with a large gap between them.
*   **Use Generous Leading:** Set line-height for `body-lg` to 1.6 to ensure the text feels "airy."
*   **Tone-on-Tone:** Use `surface_container_high` text on `surface_dim` backgrounds for low-priority captions.

### Don’t:
*   **No Pure Black:** Never use `#000000`. Use `on_background` (`#2e342d`) for all text to keep the "Zen" warmth.
*   **No Sharp Corners:** Avoid the `none` or `sm` roundedness tokens. Pottery is rarely perfectly sharp; the UI shouldn't be either.
*   **No Crowding:** If you feel the need to add a border to "fix" a layout, it means you haven't used enough white space. Double the `spacing` token instead.