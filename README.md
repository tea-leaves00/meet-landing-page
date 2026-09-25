# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

<!-- TODO: add a screenshot of the finished page and update this path -->
![](./screenshot.jpg)

### Links

- [Solution URL](https://github.com/tea-leaves00/meet-landing-page)
- [Live Site](https://tea-leaves00.github.io/meet-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- [BEM](https://getbem.com/) class naming
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Responsive images with `<picture>`

### What I learned

- **Semantic HTML:** using `<header>`, `<main>`, `<section>` and `<footer>` instead of generic `<div>`s, keeping heading levels in order, and using `alt=""` for decorative images so screen readers skip them.
- **Responsive images:** the `<picture>` element lets the browser pick a different image file per screen size, which suits the hero and footer images.

```html
<picture class="footer__picture">
  <source media="(min-width: 1024px)" srcset="./assets/desktop/image-footer.jpg">
  <source media="(min-width: 768px)" srcset="./assets/tablet/image-footer.jpg">
  <img class="footer__image" src="./assets/mobile/image-footer.jpg" alt="">
</picture>
```

- **BEM naming:** `block__element--modifier` (for example `button--primary`) keeps class names predictable and avoids relying on nested selectors.
- **Centering an image wider than the screen:** an image that is shrunk by `max-width: 100%` looks centered on small screens, but once the screen is wider than the image it sits on the left. `display: block` on its `<picture>` plus `margin: 0 auto` on the image fixes it.
- **Overlapping elements:** the "02" circle straddles the top of the footer using `position: absolute` with `transform: translate(-50%, -50%)`, and a `::after` pseudo-element puts a teal tint over the footer photo.

### Continued development

- Matching a design's exact fonts and colours from the design file instead of estimating them.
- Testing the layout at in-between screen widths, not just at the mobile, tablet and desktop sizes in the mockups.
- Making the desktop footer and hero image positioning more precise.

### Useful resources

- [MDN: The Picture element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) - explained how `<source>` and `media` work together for responsive images.
- [Get BEM](https://getbem.com/introduction/) - the official introduction to the BEM naming convention.
- [CSS-Tricks: A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) - a visual reference for the gallery and footer layouts.

### AI Collaboration

I used Claude Code for this project:

- To review my HTML mockup, convert the image tags to `<picture>` elements, and add BEM class names.
- To write a first pass of the CSS, which I then tested in the browser at different screen sizes.
- To fix layout problems by comparing my page against the design screenshots, such as the hero images not centering between breakpoints and the gallery grid on mobile.

What worked well was giving it clear reference screenshots for each screen size. The first preview image didn't show the full design, so the first attempt got some details wrong until I supplied better ones. Its colours and fonts were also estimates that needed checking against the design file.

## Author

- Frontend Mentor - [@tea-leaves00](https://www.frontendmentor.io/profile/tea-leaves00)
