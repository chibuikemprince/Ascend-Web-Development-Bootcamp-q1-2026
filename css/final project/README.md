# CSS Track — Final Project (Step-by-step)

This document explains the structure and styling of the final project in `css/final project`.


## Live class recording

## Live class recording
[Watch the live class](https://youtube.com/live/yk9OcLblX3g)

```
https://youtube.com/live/yk9OcLblX3g
```

[![Live class recording](https://img.youtube.com/vi/yk9OcLblX3g/hqdefault.jpg)](https://youtube.com/live/yk9OcLblX3g)



## Folder contents
- `index.html`: Page structure (header, hero, features, gallery, footer)
- `styles.css`: Layout, typography, responsiveness, and animations
- `car-video.mp4`: Class demo asset

## HTML walkthrough (`index.html`)
1. **Head**: Sets charset, viewport, title, and links `styles.css`.
2. **Header**: Brand on the left, nav links in the middle, and a menu button for mobile.
3. **Hero section**: Two-column layout on large screens (text + “What you'll master” card).
4. **Features section**: Title and a grid of feature cards.
5. **Gallery section**: Responsive grid with six tiles.
6. **Footer**: Simple copyright line.
7. **Script**: Toggles the `open` class on `.nav` when the menu button is clicked.

## CSS walkthrough (`styles.css`)
1. **Reset + base**
   - Universal `box-sizing: border-box` for predictable sizing.
   - Body sets margin, font, background, text color, and line-height.
   - Links inherit color and remove underline.

2. **Layout utilities**
   - `.container` constrains width and centers content.
   - `.header` uses `position: sticky` to stay visible and `flex` for alignment.

3. **Navigation**
   - `.nav` is hidden by default on small screens and appears as a dropdown.
   - `.nav.open` shows the menu when toggled by JS.
   - `.menu-btn` is styled like a pill button.

4. **Hero**
   - `.hero` is a card with border, radius, and vertical layout on mobile.
   - `.actions` wraps CTA buttons; `.btn` adds hover lift + shadow.
   - `.hero-card` highlights the list with a tinted background and `fadeUp` animation.

5. **Features + gallery**
   - `.features-grid` and `.gallery-grid` use auto-fit grids to adapt to screen size.
   - `.feature` and `.tile` share card-like styling.

6. **Animations**
   - `@keyframes fadeUp` animates opacity and vertical position.

7. **Responsive breakpoints**
   - `@media (min-width: 768px)`: Switches nav to horizontal, hides the menu button, and places hero content side by side.
   - `@media (min-width: 1024px)`: Larger hero title and taller gallery tiles.

8. **Accessibility**
   - `prefers-reduced-motion` disables animations and transitions for users who prefer less motion.

## Known issues to review
These are small typos that affect behavior and can be fixed later:
- `.features-grid` in CSS doesn’t match `.feature-grid` in HTML.
- `feature:hover` is missing the dot prefix (`.feature:hover`).
- `@keyframes fadeUp` has `frmom` instead of `from`.
- `menu-btn` in the tablet breakpoint is missing the dot prefix (`.menu-btn`).

