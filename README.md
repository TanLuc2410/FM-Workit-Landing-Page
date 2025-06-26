# Frontend Mentor - Workit landing page challenge

This project is a challenge from Frontend Mentor where I re-create the static web page based on the figma file.
The challenge is here: [Workit Landing Page](https://www.frontendmentor.io/challenges/workit-landing-page-2fYnyle5lu)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Header](#1-the-header-section)
  - [Main](#2-the-main-section)
  - [Footer](#3-the-footer-section)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

This is a responsive landing page solution for the Workit Landing Page challenge on Frontend Mentor. Built with HTML and CSS, the project focuses on clean layout structure, visual hierarchy, and responsive design. It showcases a promotional page for a fictional startup, highlighting strong call-to-actions and bold typography. This project was created to strengthen my skills in semantic HTML and mobile-first CSS styling.

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![](./images/Workit%20README.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## 🛠️ My Process

I approached this project with the intention to finish each section separately, working from top to bottom. I started by writing the HTML for the section I wanted to work on first, then used CSS to create custom properties, utility classes, and styles.

### 1. The `<header>` Section

This was the part where I struggled the most. There were **two major problems** in this section:

- **The "curved" bottom border**
- **The background patterns**

#### Curved Border

I initially tried solving this by setting `border-radius` on the bottom corners and using negative margins to stretch out the background. However, this caused the background to overflow. Even after setting `body { overflow-x: hidden; }`, the issue persisted. I only found the solution after browsing other people's ideas — by using the `clip-path` property, I was finally able to create the curved background without any overflow issues.

#### Background Patterns

This second problem frustrated me quite a bit. While the pattern on the left was normal and easy to position, the second pattern on the right kept overflowing along the x-axis. I had **absolutely no idea why** it happened. I tried many approaches but nothing seemed to work.

Eventually, I decided to position it **inside the viewport width** (`vw`). Although it doesn’t look exactly precise compared to the original design, at least it doesn’t cause overflow. Now that I think about it — _what if I used the pseudo-element `::after` and set its `background-image` to be the pattern?_ Would it turn out differently? I intend to try out that option in another project.

### 2. The `<main>` Section

My `<main>` section consists of two parts: **Call-to-action** and **Founder Image**.

#### Call-to-action

This part is relatively easy. I did come across some issues, but nothing major. The thing I learned from this interaction is that using default block elements' behavior with margin for spacing is sometimes better than using CSS Grid or Flexbox. With the mobile-first approach, I think this solution is more optimal.

#### Founder Image

This is where it gets a bit tricky. The problem was positioning the founder's message section relative to the founder's image. While it is quite simple to do it on mobile, when it comes to tablet and desktop mode, I had to change the message section `<width>` **based on the viewport width (`vw`)**.  
The solution I came up with was abstracting the message wrapper `<width>`, and it worked fantastically.

### 3. The `<footer>` Section

This section is the simplest part. I used CSS Grid to center the logo and social icons — and it's done.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- `clip-path` css property

### Continued development

I believe I still need more experience with positioning backgrond image and making background shapes. Addtionally, I need to use abstraction more in my css code to feel comfortable with it.

### Useful resources

- [clip-path MDN docs](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path)
- [Youtube: clip-path tutorial](https://www.youtube.com/watch?v=oWXm5n-Zi38)

## Author

- Website - [Khuu Tan Luc](https://lucfrontenddev.framer.website/)
- Frontend Mentor - [@TanLuc2410](https://www.frontendmentor.io/profile/TanLuc2410)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

The clip-path solution was inspried by [Frontend Mentor: Onias da Rocha Filho](https://www.frontendmentor.io/solutions/react-with-typescript-and-css3-fully-responsive-b1e38TJe1r)
