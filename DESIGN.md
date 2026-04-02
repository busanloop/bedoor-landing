# Design System Strategy: The Global Gateway

## 1. Overview & Creative North Star
The design system for this professional MICE and incubation firm is built upon a Creative North Star called **"The Digital Curator."** 

MICE (Meetings, Incentives, Conferences, Exhibitions) and startup incubation require a delicate balance: the authoritative "trust" of public sector partnerships and the high-energy "innovation" of the startup world. We move beyond a standard corporate template by using an editorial, high-end approach. This design system favors large-scale typography, intentional white space (asymmetry), and overlapping photographic elements that bleed across sections, suggesting a firm that "connects the dots" on a global scale.

The visual language transitions from the rigid "B" and "D" geometric shapes of the logo into a fluid, layered interface that feels architectural and premium.

## 2. Colors: Tonal Architecture
We utilize a sophisticated palette where the deep navy provides the anchor of authority, and the vibrant secondary tones inject modern energy.

### Core Token Usage
- **Primary (`#002046`)**: Used for high-level branding, heavy headlines, and primary navigation anchors.
- **Secondary (`#00677d`)**: Our "Innovation teal." Reserved for interactive elements, progress indicators, and startup-focused callouts.
- **Surface & Background (`#f4fafe`)**: A cool-tinted white that prevents the "stark" look of pure `#FFFFFF`, providing a softer, more professional canvas.

### The "No-Line" Rule
To maintain a high-end editorial feel, **1px solid borders are strictly prohibited** for defining sections. Instead, boundaries must be created through:
- **Tonal Shifts**: Use `surface-container-low` sections placed against a `surface` background.
- **Strategic Padding**: Utilize the Spacing Scale (specifically `16` to `24`) to create breathing room that naturally separates content blocks.

### Surface Hierarchy & Nesting
Think of the UI as layers of physical material. 
1. **Base Layer**: `surface` (`#f4fafe`)
2. **Structural Sections**: `surface-container-low`
3. **Interactive Cards**: `surface-container-lowest` (pure `#ffffff`) to create a subtle "lift."
4. **Active Overlays**: Glassmorphism using `surface_variant` with a 60% opacity and a `backdrop-filter: blur(12px)`.

### Signature Textures
Main CTAs should not be flat. Use a subtle linear gradient (45-degree angle) from `primary` to `primary_container` to give buttons a "weighted" feel that mimics premium leather or high-quality matte print.

## 3. Typography: Editorial Authority
The system pairs **Manrope** for high-impact displays with **Inter** for functional reading.

*   **Display & Headlines (Manrope)**: These are your "Statement" pieces. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create an authoritative, global presence. The geometric nature of Manrope mirrors the circular forms in the BEDOOR logo.
*   **Titles & Body (Inter)**: Inter provides the "Trust" factor. Its high x-height ensures readability for complex MICE schedules or incubation reports.
*   **The Hierarchy Goal**: Large, bold headlines should be paired with significantly smaller, light-gray (`on_surface_variant`) body text to create a high-contrast, premium "editorial" layout reminiscent of a luxury business magazine.

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are often messy. This system uses **Tonal Layering** to convey hierarchy.

*   **The Layering Principle**: Instead of a shadow, place a `surface-container-lowest` card inside a `surface-container` area. This "paper-on-paper" look is more modern and cleaner.
*   **Ambient Shadows**: For floating elements (like a navigation bar or a mobile FAB), use an extra-diffused shadow: `box-shadow: 0 12px 40px rgba(0, 32, 70, 0.06);`. Note the shadow color is a tint of our `primary` navy, not black.
*   **The "Ghost Border" Fallback**: If a border is required for a form field or a button, use `outline_variant` at **20% opacity**. It should be felt, not seen.
*   **Glassmorphism**: Use semi-transparent layers for navigation menus to allow hero images to bleed through, maintaining the "Global" feel.

## 5. Components

### Buttons: The "Interaction Anchor"
- **Primary**: Solid `primary` background, white text. Corners at `md` (0.375rem). On hover, transition to the `secondary` teal to signal innovation.
- **Tertiary**: No background or border. Text only in `primary` with a 2px underline in `secondary` that expands on hover.

### Structured Portfolio Cards
- **Construction**: No borders. Use `surface-container-lowest` as the background.
- **Imagery**: Use a 16:9 aspect ratio for hero images with a slight `xl` (0.75rem) corner radius.
- **Separation**: Never use divider lines. Use `spacing-6` (1.5rem) between the header and the body text.

### High-Quality Icons
- Use 2px stroke-weight icons (e.g., Lucide or Phosphor). 
- Icons should always be housed in a `secondary_container` circular background to tie back into the circular "D" of the logo.

### Input Fields
- Background: `surface_container_highest` at 50% opacity.
- Border: "Ghost Border" only on focus.
- Typography: Label must be `label-md` in `on_surface_variant`.

## 6. Do's and Don'ts

### Do
- **Do** use asymmetrical layouts where text sits on one side of a 12-column grid and an image overlaps the gutter.
- **Do** use the `secondary` teal sparingly—it is a highlighter, not a background color.
- **Do** embrace verticality. Let the user scroll through generous sections of information.

### Don't
- **Don't** use 100% black text. Use `on_surface` (`#161d1f`) to keep the interface feeling premium.
- **Don't** use sharp 90-degree corners. Stick to the `md` and `lg` roundedness scale to keep the brand "innovative and approachable."
- **Don't** use standard "drop shadows." If it looks like a default Photoshop shadow, it’s too heavy.
- **Don't** use divider lines between list items. Use the `surface-container` shifts.