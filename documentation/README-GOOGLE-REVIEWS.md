# Add Google Reviews to Hughes Hypnotherapy Website

Objective:
Display live Google reviews on the Hughes Hypnotherapy website using Elfsight's Google Reviews widget.

Status:
Not yet implemented.

---

## Why This Approach

Benefits:

- Automatic synchronisation with Google reviews
- No backend development required
- No Google API coding required
- Compatible with static HTML websites
- Works with GitHub Pages and Cloudflare hosting
- Reviews update automatically when new reviews are received
- Can start on Elfsight's free tier

Recommended implementation:

- Create a dedicated Reviews page
- Display a small preview section on the homepage
- Link homepage visitors to the Reviews page

---

## Prerequisites

Before starting, ensure:

- Google Business Profile exists and is verified
- Google reviews are visible on the Business Profile
- Website source code is available locally

Business:

Hughes Hypnotherapy

---

## Step 1 - Create Elfsight Account

1. Visit Elfsight
2. Create a free account
3. Sign in to the dashboard

---

## Step 2 - Create Google Reviews Widget

1. Select "Google Reviews" widget
2. Search for the Hughes Hypnotherapy Google Business Profile
3. Connect the profile
4. Choose a layout

Recommended layout:

- Grid
or
- Carousel

Avoid:

- Large floating badges
- Popups

The website design is intentionally calm and professional.

---

## Step 3 - Configure Widget

Recommended settings:

Show:
- Overall rating
- Reviewer's first name
- Review text
- Star rating

Hide:
- Excessive branding
- Unnecessary profile information

Filters:

- Minimum rating: 4 stars
- Maximum rating: 5 stars

---

## Step 4 - Publish Widget

1. Click Publish
2. Copy the installation code

It will look similar to:

```html
<div class="elfsight-app-xxxxxxxx"></div>

<script srctic.elfsight.com/platform/platform.jsscript>

---

## Step 5 - Create Reviews Page

Create:

reviews.html

Add a new menu item:

Reviews

Recommended page structure:

Hero

↓

Why Reviews Matter

↓

Google Reviews Widget

↓

Book Consultation CTA

Example structure:

```html
<section class="reviews-page">

    <h1>Client Reviews</h1>

    <p>
        Read feedback from clients who have experienced
        hypnotherapy with Hughes Hypnotherapy.
    </p>

    <div class="elfsight-app-xxxxxxxx"></div>

</section>
```

---

## Step 6 - Add Widget Script

Immediately before the closing </body> tag add the script provided by Elfsight.

It will look similar to:

```html
<script src="c.elfsight.com/platform/platform.jsscript>
```

Only add this script once per page.

---

## Step 7 - Add Homepage Preview Section

Homepage objective:

Provide social proof without loading the full widget.

Suggested content:

```html
<section class="home-reviews">

    <h2>Client Reviews</h2>

    <p>
        Rated 5★ by clients across Leeds and Yorkshire.
    </p>

    reviews.html
        Read Reviews
    </a>

</section>
```

Benefits:

- Faster page load
- Fewer Elfsight widget views
- Cleaner homepage design

---

## Step 8 - Add "Leave a Review" Button

Add to footer:

```html
<a hrefREVIEW_LINK
    Leave a Google Review
</a>
```

Replace GOOGLE_REVIEW_LINK with the direct review URL from your Google Business Profile.

Recommended location:

Footer

or

Contact page

or

Reviews page

---

## Step 9 - Update Navigation

Add:

```html
<li>reviews.htmlReviews</a></li>
```

Recommended navigation:

- Home
- Services
- About
- Reviews
- Contact

---

## Step 10 - Create Reviews Call To Action

At the bottom of reviews.html:

```html
<section class="reviews-cta">

    <h2>Ready to Start Your Journey?</h2>

    <p>
        Arrange a free consultation to discuss your goals.
    </p>

    <a href="contact.html" class="ultation
    </a>

</section>
```

Purpose:

Convert visitors immediately after reading reviews.

---

## Step 11 - Mobile Testing

Test on:

- Desktop
- Tablet
- Mobile

Verify:

- Reviews display correctly
- Carousel works
- Text remains readable
- No horizontal scrolling
- Navigation functions correctly

---

## Step 12 - Performance Test

Check:

- Homepage still loads quickly
- Reviews page loads correctly
- Widget does not introduce visual layout jumps
- Images remain optimised

Tools:

- Google PageSpeed Insights
- Lighthouse

---

## Step 13 - SEO Enhancements

Add Google Business Profile URL to schema markup.

Add:

- Reviews page title
- Reviews page meta description
- Internal links to reviews page

Suggested title:

Hughes Hypnotherapy Reviews | Client Success Stories

Suggested meta description:

Read verified Google reviews from clients of Hughes Hypnotherapy and discover how hypnotherapy has helped with anxiety, confidence, smoking cessation and more.

---
