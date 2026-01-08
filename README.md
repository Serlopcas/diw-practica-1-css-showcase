# Freky’s Winter Hut — CSS Modern Showcase

A one-page “portfolio-grade” landing page for **Freky’s Winter Hut**, a fictional dog-sled touring company based in **Alta, Norway**.  
The project is built as a **CSS modern showcase**, focusing on interaction states, animations, advanced image effects, typography, and responsive layout.

This repository was created for **DIW (Diseño de Interfaces Web)** as a CSS-focused front-end project and follows the assignment requirements: pseudoclasses, CSS animations,
advanced image styling, Font Awesome icons, external typography, and responsive design.


## Live / Demo

- **Live site:** https://serlopcas.github.io/diw-practica-1-css-showcase/
- **Repository:** https://github.com/Serlopcas/diw-practica-1-css-showcase


## Project Goals

- Build a **clean, presentable** showcase project suitable for a personal portfolio.
- Demonstrate modern CSS techniques in a realistic UI (not a “random effects” demo).
- Keep the project simple: **HTML + CSS only**, no frameworks.


## Tech Stack

- **HTML5**
- **CSS3 (modern features)**
- **Google Fonts** (Inter + Space Grotesk)
- **Font Awesome** (icons)


## Project Structure

The project follows this structure.

```
/showcase-css
├── index.html
├── /css
│   └── style.css
├── /img
│   ├── Logo.png
│   ├── Malamute01.png ... Malamute06.png
│   └── Gallery01.png ... Gallery03.png
└── /assets
    └── favicon/favicon.ico
```


## Page Sections

All content is organized as a single-page website with internal navigation:

- **Header / Navigation** (sticky, icon-first nav with label reveal)
- **Hero** (background image, aurora animation + brand watermark)
- **Routes** (cards: distance, time, difficulty)
- **Pack** (dog cards with photo styling + tilt effect)
- **Gallery** (image tiles with caption overlay)
- **Contact** (styled form with visible validation states)
- **Footer** (social links)


## Key UI Details

- Sticky header with an icon-first navigation that reveals labels on hover/focus.
- Hero section with layered aurora lighting using `mix-blend-mode` for natural blending.
- Subtle 3D tilt micro-interaction enabled only on elements with the `.tilt` class.
- Contact form with visible validation states (`:valid` / `:invalid`) and consistent focus styling.


## CSS Showcase: What’s Implemented and Where

### 1) Pseudoclasses
- `:hover` → nav items, buttons, cards, gallery tiles.
- `:focus-visible` → global focus ring + unified ring on nav/CTA/footer pills.
- `:active` → buttons/nav interactions.
- `:nth-child()` → routes highlight pattern and alternating dog image clip-path patterns.
- `:valid` / `:invalid` → email field styling in the contact form.

### 2) Animations + transitions
- `@keyframes` + `animation`:
  - Hero aurora “comet” background animation.
  - Hero scroll hint dot.
- `transition`:
  - UI hover effects (buttons/nav/gallery/cards).
  - Image filter transitions.

### 3) Images + advanced visual effects
- Uses images as **backgrounds and content** (hero background, dogs, gallery).
- `mix-blend-mode` applied to blend aurora layers with the hero background.
- `background-image`, `background-size`, `background-position` used across hero/gallery.
- `filter`, `opacity`, `clip-path` used in dog photos and hero/overlays.

### 4) External typography
- Google Fonts:
  - **Space Grotesk** (headings / UI emphasis)
  - **Inter** (body / readable text)

### 5) Font Awesome icons (exclusive icon source)
- Icons integrated into:
  - Navigation items
  - Buttons (CTA)
  - Metadata labels (routes)
  - Hero badges

### 6) Responsive design
- Multiple breakpoints for header/nav behavior and layout.
- Uses relative units (%, vw, rem) and responsive typography (`clamp()` for titles).
- Mobile UX: navigation labels are always visible where hover is not available.

### 7) CSS organization (maintainability)
- Token-based design via `:root` variables (colors, spacing, fonts).
- Clear sectioning and documentation comments.
- Opt-in interaction behavior with `.tilt` class.


## Accessibility Notes

- Strong global `:focus-visible` ring for keyboard users.
- `prefers-reduced-motion: reduce` disables 3D/animated transforms where possible.
- Decorative imagery uses `aria-hidden="true"` when it does not convey content.


## How to Run Locally

No build step required.

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   ```
2. Open `index.html` directly in your browser, **or** use a local server:
   ```bash
   # VS Code Live Server, or:
   python -m http.server 5500
   ```
3. Visit:
   ```
   http://localhost:5500
   ```


## Deployment (GitHub Pages)

1. Push to GitHub.
2. Go to **Settings → Pages**.
3. Deploy from **branch**: `main` and folder `/ (root)`.
4. Your site will be available at your GitHub Pages URL.


## Credits

- Fonts: Google Fonts (Inter, Space Grotesk)
- Icons: Font Awesome
- Images: Project assets placed in `/img` (hero, dogs, gallery)


## License

MIT License — see the `LICENSE` file for details.
