# CSS Page Architecture Guide

This document explains which sections of style.css control each page of the website.

When modifying a page, start with the page section below before digging into the full CSS.

---

# CSS Structure Overview

The stylesheet is organised into:

```text
GLOBAL
PAGE CONTAINER
HEADER
HERO
HERO TREATMENT LINKS
CALL TO ACTION
TREATMENT CARDS
ABOUT
TESTIMONIALS
CONTRAST CONTAINER
DISCLAIMER
TREATMENT HEADLINE
ACCREDITATIONS
FOOTER
CONTACT FORM
PRICES
BUTTONS
RESPONSIVE DESIGN
```

Every page reuses these building blocks.

---

# Home Page (index.html)

## Page Structure

```text
Header
Hero
Treatment Links
About
Treatment Cards
Testimonials
Disclaimer
Accreditations
CTA
Footer
```

## Relevant CSS Sections

### Header

Controls:

- Logo
- Navigation menu
- Header background image

```css
header
.header-row
.logo
nav
nav ul
nav a
```

---

### Hero

Controls:

- Main homepage heading
- Supporting text
- Hero image
- Hero panel

```css
.hero
.hero-content
.hero-image
.hero-panel
```

---

### Treatment Pills

The pill links below the hero.

```css
.treatment-links
.treatment-links li
.treatment-links a
```

Change these when:

- Adjusting pill colours
- Pill spacing
- Pill hover behaviour

---

### Treatment Cards

Controls the treatment cards lower down the page.

```css
.treatment-cards
.cards-grid
.treatment-card
.treatment-card img
```

Change these when:

- Adjusting card size
- Changing card layout
- Increasing cards per row
- Altering image size

---

### Testimonials

```css
.testimonials
.testimonial-grid
.testimonial-card
```

---

### Disclaimer

```css
.disclaimer
```

---

### Accreditations

```css
.accreditations
.logo-grid
.logo-grid img
```

If accreditation logos need resizing this is where to look.

---

### CTA

```css
.cta
```

Controls:

- Ready to Take the Next Step section
- Button positioning

---

# About Page (about.html)

## Page Structure

```text
Header
Hero
About Content
Accreditations
CTA
Footer
```

## Relevant CSS Sections

### Header

```css
header
.logo
nav
```

---

### Hero

```css
.hero
.hero-content
.hero-image
.hero-panel
```

---

### Main About Content

```css
.about
```

This section controls:

- Padding
- Background colour
- Content spacing

If the page feels cramped or too wide, this is usually the section to change.

---

### Accreditations

```css
.accreditations
.logo-grid
.logo-grid img
```

---

### CTA

```css
.cta
```

---

# Treatments Page (treatments.html)

## Page Structure

```text
Header
Treatment Cards
CTA
Footer
```

## Relevant CSS Sections

### Treatment Cards

This is the main section of the page.

```css
.treatment-cards
.cards-grid
.treatment-card
.treatment-card img
.treatment-card h3
.treatment-card p
```

---

### Number of Cards Per Row

Controlled by:

```css
.cards-grid
```

Current:

```css
grid-template-columns: repeat(4, 1fr);
```

Examples:

```css
repeat(3, 1fr)
```

3 cards per row

```css
repeat(5, 1fr)
```

5 cards per row

---

### Card Images

Controlled by:

```css
.treatment-card img
```

Example:

```css
max-width: 200px;
height: 200px;
```

---

# Individual Treatment Pages

Examples:

```text
anxiety.html
stress.html
sleep.html
habits.html
smoking.html
```

## Page Structure

```text
Header
Treatment Headline
Hero
Disclaimer
CTA
Footer
```

---

## Relevant CSS Sections

### Treatment Headline

Green banner at the top.

```css
.treatmentheadline
.treatmentheadline h2
```

---

### Hero

Main content area.

```css
.hero
.hero-content
.hero-image
.hero-panel
```

The treatment image and main treatment content are controlled here.

---

### Disclaimer

```css
.disclaimer
```

Green disclaimer section below hero.

---

### CTA

```css
.cta
```

---

# Contact Page

## Page Structure

```text
Header
Hero
Contact Form
CTA
Footer
```

## Relevant CSS Sections

### Hero

```css
.hero
.hero-content
.hero-image
.hero-panel
```

---

### Contact Form

```css
.contact-form
.contact-form input
.contact-form textarea
```

Controls:

- Form width
- Textbox styling
- Textarea styling

---

# Prices Page

## Page Structure

```text
Header
Price Cards
CTA
Footer
```

## Relevant CSS Sections

### Pricing Grid

```css
.price-grid
```

Current:

```css
repeat(5, 1fr)
```

Five price cards per row on desktop.

---

### Price Display

```css
.price
```

Controls:

- Font size
- Weight
- Alignment

---

# Changing Specific Things

## Navigation Spacing

```css
nav ul
```

Change:

```css
gap: 45px;
```

---

## Hero Layout

```css
.hero-content
```

Desktop layout:

```text
Image | Content
```

Mobile:

```text
Image
Content
```

---

## Treatment Card Layout

```css
.cards-grid
```

---

## Treatment Card Image Size

```css
.treatment-card img
```

---

## Accreditation Logo Size

```css
.logo-grid img
```

---

## Button Styling

```css
.btn
```

All buttons inherit from this one rule.

---

# Responsive Design

If something looks wrong only on tablets or phones, look at the responsive section at the bottom of the file.

```css
@media (max-width:1199px)
```

Tablet

---

```css
@media (max-width:900px)
```

Small tablet

---

```css
@media (max-width:768px)
```

Mobile

---

```css
@media (max-width:480px)
```

Small mobile

---

# Golden Rule

When changing a page:

1. Find the page structure above.
2. Identify the component being changed.
3. Go directly to that CSS section.
4. Avoid creating new classes unless absolutely necessary.

Nearly every page on the site is built from the same five components:

```text
Header
Hero
Cards
CTA
Footer
```

Most site changes can be made by modifying those existing components.