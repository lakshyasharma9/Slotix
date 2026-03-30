# Design System Specification: High-Octane Kineticism

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Kineticist."** 

This is not a static interface; it is a high-performance engine captured in a digital viewport. We are moving away from the "flat web" by embracing a "Gaming + Sports" editorial aesthetic that prioritizes speed, depth, and luminosity. The system breaks the traditional grid through **intentional layering and light-emissive elements**, creating an environment that feels alive. We utilize extreme typographic contrasts—pairing massive, aggressive display faces with hyper-legible utility type—to evoke the feeling of a premium sports broadcast mixed with a futuristic gaming HUD.

---

## 2. Colors: The Luminous Spectrum
The palette is built on the high-contrast tension between absolute darkness and toxic, neon light.

### Primary & Action
*   **Primary (`#97f231`)**: Our "Neon Fuel." Use this sparingly for high-intent actions and critical status indicators.
*   **Primary Container (`#84dd15`)**: Used for button surfaces to provide a more grounded, tactile feel than the pure neon.

### Surface Hierarchy & The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Boundaries are created through tonal shifts and light.
*   **Surface (`#0e0e0e`)**: The base vacuum.
*   **Surface Container Lowest (`#000000`)**: Used for deep "wells" or background sections to create a sense of infinite depth.
*   **Surface Container High (`#1f1f1f`)**: The standard for glassmorphic card backgrounds.
*   **Surface Bright (`#2c2c2c`)**: Reserved for hover states or active "elevated" cards.

### The "Glass & Gradient" Rule
To achieve the "Premium" vibe, use **Glassmorphism** for all floating UI (Modals, Navigation Bars, Hovering Cards). 
*   **Formula:** `surface-container-high` at 60% opacity + `backdrop-blur: 20px`.
*   **Signature Texture:** Use a linear gradient on Primary CTAs transitioning from `primary` to `primary-container` at a 135-degree angle to simulate a curved, light-catching surface.

---

## 3. Typography: Editorial Dominance
We use a dual-font strategy to balance aggressive branding with functional clarity.

*   **Display & Headline (Space Grotesk):** This is our "Branding" voice. Use `display-lg` (3.5rem) and `headline-lg` (2rem) for hero sections and sports stats. The wide aperture of Space Grotesk feels high-tech and engineered.
*   **Body & Label (Inter):** Our "Utility" voice. Inter provides the Swiss-style legibility required for dense gaming data and betting odds. Use `body-md` (0.875rem) for most secondary information.
*   **Hierarchy Note:** Use `on-surface-variant` (`#ababab`) for secondary body text to ensure the white `on-surface` text remains the focal point.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden. We use **Luminous Elevation.**

*   **The Layering Principle:** Stack `surface-container-low` components on a `surface` background. If an element needs to "pop," use a background color shift rather than an outline.
*   **Ambient Glows:** Instead of black shadows, use "Neon Underglows" for primary elements. A shadow with a 20px blur using `primary` at 15% opacity creates an emissive effect, making the button look like it’s powered by light.
*   **The "Ghost Border" Fallback:** If a container requires a border for accessibility, use `outline-variant` (`#484848`) at **15% opacity**. It should be felt, not seen.
*   **Corner Radii:** Apply `xl` (1.5rem / 24px) for main containers and `md` (0.75rem / 12px) for inner nested elements to create a sophisticated, concentric nesting look.

---

## 5. Components: The Kinetic HUD

### Buttons
*   **Primary:** High-saturation `primary` background. Sharp 135° gradient. No border. Text is `on-primary` (Deep Dark Green).
*   **Secondary (Glass):** `surface-container-high` at 40% opacity with a `backdrop-blur`. This is the "Sports HUD" look.
*   **Tertiary:** Pure text using `primary` color, strictly for low-priority navigation.

### Cards & Data Lists
*   **The Divider Ban:** Never use lines to separate list items. Use a `2.5` (0.625rem) vertical gap and a slight `surface-container-low` background on alternating items or on-hover.
*   **Nesting:** A `surface-container-highest` card should only sit on a `surface-container-low` background. This creates a logical physical stack.

### Input Fields
*   **Base State:** `surface-container-low` background with a `sm` (4px) bottom-accent bar in `outline-variant`.
*   **Focus State:** The bottom-accent bar expands to 2px thickness and transforms into `primary` neon, accompanied by a subtle `primary` outer glow.

### Signature Component: The "Live-Glow" Chip
*   Used for "Live" sports or active games. A `surface-container-highest` pill with a pulsing 4px `primary` dot. This utilizes the system’s "fast" vibe.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme whitespace (Scale `12` to `20`) between major editorial sections to let the "Pure Black" background feel premium.
*   **Do** overlap elements. Having a high-res athlete image or game asset break the container of a card adds to the "Editorial" feel.
*   **Do** use `primary` neon sparingly. If everything glows, nothing is important.

### Don't:
*   **Don't** use pure grey `#808080`. Always use the tokens (like `on-secondary-container`) to ensure the greys feel "warm" or "cool" in line with the brand.
*   **Don't** use 100% opaque borders. They flatten the design and destroy the "High-Tech" glassmorphic illusion.
*   **Don't** use standard "Drop Shadows." Only use tinted, high-blur ambient glows or tonal shifts.