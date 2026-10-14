# kiki — Graphic Designer portfolio

Static site. No build step: extract the folder and open `index.html`, or deploy the complete folder to your host.

## Current home page

- Game Boy hero with a generated pixel-art idea meadow and a crisp pixel dissolve into the normal page background; EN/RU language switch.
- Animated poster workspace with a demonstration conversation.
- Telegram and mail banners.
- GitHub and Community banners with translucent glass backing in the style of the folder pockets.
- Five folder chapters: about, works, services, process, contact.
- Pixel-art footer with cursor-following tilt, image parallax and light.

The site uses the original light background through the very bottom. Theme switching, the Toolkit button/modal and the software folder have been removed.

## Files

- `index.html`: home page.
- `section.html?s=about|works|services|process|contact`: chapter pages.
- `js/data/translations.js`: EN/RU UI copy.
- `js/data/sections.js`: folder definitions and chapter content.
- `css/components/community-glass.css`: glass backing for GitHub/Community.
- `css/components/design-studio.css`, `js/site/design-studio.js`: animated design demo.
- `css/components/portfolio-footer.css`, `js/site/portfolio-footer.js`: footer and cursor motion.
- `assets/images/footer-pixel-art.webp`: generated footer artwork.

Mouse/pen motion responds to real pointer events and works with a mouse on touch-capable computers. Touch gestures are not hijacked. Reduced-motion preferences are respected. PNG previews are static; test movement in the actual HTML page.

## Pixel hero wallpaper

`assets/images/hero-meadow-transition.webp` contains the idea-meadow artwork and its square-pixel transparent bottom edge in ONE image. No separate mask image is needed. `css/components/hero-pixel.css?v=2` positions the background at the bottom so cover-cropping cannot remove the transition. The unchanged `--site-bg` shows through the transparent pixels.

The standalone “From your idea to a design that’s ready to go” banner is removed. The original poster/chat banner and the How I work folder are kept.

When deploying, upload the complete updated folder, including the new artwork and stylesheet; replacing the background image alone will not apply the CSS change.

## Conversation banner — direct conversation revision

The banner is about contact, questions, clarification and feedback, not personal ideas, methods or a portfolio showcase. The existing three-scene geometry and motion are retained; the tree now reads Question / Answer / Summary. The header, description and tabs align left with the main portfolio introduction. The preview remains centered. The outer background inherits --site-bg.

The plus controls use a geometric CSS cross, centered horizontally and vertically without relying on font baseline. Tree icons and connectors stay on the aligned grid. The footer CTA, Pause/Resume control and disclaimer remain removed. RU/EN copy and reduced-motion support are retained. All dialogue is sample copy, not a live-chat backend. Deploy the whole folder; no build step.

## Word-search banner and intro typography

The main intro headline now matches the “Let’s talk / На связи” font family, size, weight, tracking and line height; emphasized words use the same face rather than a different treatment.

A new format word-search is the final section immediately before the footer, after the folder chapters. It supports RU/EN with nine format words and locally hosted Departure Mono (OFL license included). Three groups of words cycle every 4420ms; pixel-stepped outlines draw in 1020ms with staggered 520ms letter emphasis. Motion pauses offscreen and in hidden tabs and is static for reduced-motion users. The decorative grid has an accessible text alternative.

New files: `css/components/intro-type.css`, `css/components/word-formats.css`, `js/site/word-formats.js`, `assets/fonts/departure-mono.woff2` and its license. Deploy the complete folder.

## Automatic conversation and raised mini-cards

The contact showcase now runs a complete visible cycle: three dialogues (request and reply typed in sequence), five moving topic cards, and a six-stage animated conversation tree with automatically updated side-panel details. Hovering no longer stops it. Keyboard focus and manual controls keep reading stable; offscreen/hidden-tab motion stops and reduced-motion preferences are respected.

Four raised navigation tiles are placed between the folders and the word-search banner: Work, Services, About kiki, Contact. Each links to the corresponding existing chapter. Mouse/pen movement produces restrained 3D tilt, a cursor-positioned light spot, and a slightly cursor-following action label. Touch has a static visible label; reduced-motion disables tracking. No external brands, testimonials or invented customer counts are used.

New files: `css/components/mini-cards.css`, `js/site/mini-cards.js`. Updated conversation assets use `?v=6` to avoid old cached versions. Deploy the complete folder.

## Recessed magnetic mini-cards (v7)

The four tiles are now visually inset with inner shadows, not lifted by external shadows or 3D tilt. The action badge follows the cursor using a damped spring: up to about 40–50px horizontally and 15–30px vertically, constrained to stay inside the tile and below its label. It smoothly recenters when the pointer leaves. Keyboard focus and touch use a stable centered action; reduced-motion disables tracking. Icons are personalized vector marks, not copied partner logos.

## Magnetic mini-cards (v8)
Desktop labels and icons stay centered on hover. The action follows the cursor below the label and may extend up to 28px below the tile. Extended hover area prevents flicker; caption spacing reserves room. Mobile retains fixed, always-visible actions inside cards.

## Free vertical magnetic action (v9)
Desktop action follows the pointer across the entire tile, including the top edge. Brand stays fixed. Mobile retains its stable layout.
