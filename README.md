# Freetown Student Housing

> Safe, verified, affordable student rooms near campus in Freetown, Sierra Leone.

Freetown Student Housing is a responsive, multi-page website that helps students find verified accommodation close to their campus, and helps landlords reach genuine student tenants. It was built for **DCOMP204 – Web Design 1 (Assignment 2: HTML, CSS & Responsive Website)** at Limkokwing University of Creative Technology, Sierra Leone Campus, and is the coded version of the Assignment 1 design (project proposal, user research, information architecture, wireframes and Figma prototype).

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Screenshots](#screenshots)
3. [Problem Statement and Goals](#problem-statement-and-goals)
4. [Features](#features)
5. [Pages in Detail](#pages-in-detail)
6. [Site Map and User Flow](#site-map-and-user-flow)
7. [Project Structure](#project-structure)
8. [Tech Stack](#tech-stack)
9. [Design System](#design-system)
10. [Responsive Design](#responsive-design)
11. [Accessibility and Semantics](#accessibility-and-semantics)
12. [Getting Started](#getting-started)
13. [Deployment](#deployment)
14. [Testing Checklist](#testing-checklist)
15. [Known Issues and Roadmap](#known-issues-and-roadmap)
16. [Assignment Deliverables](#assignment-deliverables)
17. [Contact](#contact)
18. [Credits](#credits)

---

## Project Overview

| | |
|---|---|
| **Project name** | Freetown Student Housing |
| **Type** | Static, multi-page website (HTML + CSS) |
| **Audience** | Students looking for rooms; landlords listing rooms |
| **Primary campus** | Limkokwing University, Freetown |
| **Location** | Freetown, Sierra Leone |
| **Currency** | Leones (Le) |

## Screenshots

### Home
![Home page: hero, search form, featured accommodations](screenshots/home.png)

### About
![About page: mission, stats, how it works and team](screenshots/about.png)

### Browse Listings
![Listings page: filter sidebar, result cards and pagination](screenshots/listings.png)

### Listing Detail and Booking Request
![Listing detail page: gallery, amenities, booking buttons and rating breakdown](screenshots/listing-detail.png)

### Contact
![Contact page: enquiry form, campus details and FAQ](screenshots/contact.png)

## Problem Statement and Goals

Finding safe, affordable housing near campus is difficult for first-year and returning students. Listings are scattered, hard to verify, and often far from campus. This site aims to:

- Make it easy to **search and filter** rooms by price, distance and amenities
- Build **trust** through verified landlords and a visible rating breakdown
- Show **proximity to campus** (for example, "8 min walk to Limkokwing") on every listing
- Give students a simple path from **search, to contact, to move in**
- Give landlords a way to reach genuine student tenants

## Features

### For students
- **Browse listings** with a result count, sort control and pagination
- **Filter sidebar**: price range, distance to campus, room type, bedrooms, amenities, move-in date and a "Verified only" toggle
- **Listing detail view**: image gallery with thumbnails, monthly price, walking distance, amenities list and map preview
- **Rating breakdown**: percentage bars from 5 stars down to 1 star
- **Booking actions**: *Request to Book / Contact Landlord* and *Save to Favourites*
- **Similar listings** to keep students exploring

### Site-wide
- Consistent header navigation with an active-page highlight
- Breadcrumb navigation on every inner page
- Four-column footer: brand blurb, quick links, support links, contact details
- Dark theme with gold accent colour, controlled through CSS custom properties

### Trust and support content
- "How it works" in three steps (Search, Contact, Move in)
- Key stats: 120+ listings, 5 campuses covered, 40+ landlords
- FAQ covering landlord verification, booking fees and reporting fake listings
- Contact form and campus contact details

## Pages in Detail

### Home (`index.html`)
Landing page and entry point for all navigation links.

### About (`pages/about.html`)
- Hero section with image, mission statement and a "Read our story" button
- Stats grid (listings, campuses, landlords)
- "How it works" cards
- Team section with three member cards (name and role placeholders to be completed)
- Founding-team testimonial banner

### Listings (`pages/listings.html`)
- Two-column layout: a 280px filter sidebar and a results column
- Heading shows the result count, for example "24 results near Limkokwing University"
- Horizontal listing cards with image, title, price, distance, **Save** and **View Details**
- Pagination controls (previous, 1, 2, 3, next)
- A "Map View" link for a future map mode

### Listing Detail (`pages/details.html`)
- Main column: large gallery image, four thumbnails, rating breakdown
- Sidebar: title, price (Le 750 / month), walking distance, amenities, map placeholder, booking buttons
- Similar listings grid

### Listing Detail and Booking Request (`pages/listing_detail___booking_request.html`)
An alternative, semantic version of the detail page using `main`, `section`, `aside` and `article`. It includes the gallery, an info card with the booking box, a map preview image, the rating breakdown and a similar-listings grid.

### Contact (`pages/contact.html`)
- Contact form: full name, phone number, email address, subject and message
- Campus details panel with map placeholder, phone, email, opening hours (Mon to Fri, 9am to 5pm) and social icons
- FAQ section

## Site Map and User Flow

```
Home
├── About
├── Listings
│   └── Listing Detail
│       └── Booking Request / Contact Landlord
└── Contact (FAQ, enquiry form)
```

**Main student journey:** Home, then Listings (apply filters), then Listing Detail (check amenities, rating and distance), then Request to Book / Contact Landlord.

## Project Structure

```
freetown-student-housing/
├── index.html
├── CSS/
│   └── main.css
├── pages/
│   ├── about.html
│   ├── listings.html
│   ├── details.html
│   ├── listing_detail___booking_request.html
│   └── contact.html
├── screenshots/
│   ├── home.png
│   ├── about.png
│   ├── listings.png
│   ├── listing-detail.png
│   └── contact.png
└── README.md
```

All inner pages load the shared stylesheet with `../CSS/main.css`, so `CSS/` and `pages/` must stay as siblings.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 with semantic elements (`header`, `nav`, `main`, `section`, `aside`, `article`, `footer`) |
| Styling | CSS3: custom properties, Flexbox, CSS Grid |
| Images | Unsplash (placeholder photography) |
| Design | Figma (Assignment 1 prototype) |
| Version control | Git and GitHub |

No frameworks, build tools or package managers are required.

## Design System

The visual style is a dark UI with a gold accent, defined once in `CSS/main.css` and reused through CSS custom properties.

### Design tokens used in the pages

| Token | Used for |
|-------|----------|
| `--bg-card` | Card and panel backgrounds |
| `--bg-input` | Form fields and small circular icons |
| `--border-color` | Card, input and divider borders |
| `--text-main` | Primary text |
| `--text-muted` | Secondary text, captions, descriptions |
| `--accent-gold` | Prices, links and highlights |
| `--radius-sm` | Small corners (inputs, thumbnails) |
| `--radius-md` | Larger corners (cards, images) |

### Reusable components

| Component | Class names |
|-----------|-------------|
| Header and navigation | `.site-header`, `.nav-container`, `.nav-links`, `.brand-logo`, `.auth-link` |
| Breadcrumbs | `.breadcrumbs` |
| Buttons | `.btn`, `.btn-primary`, `.btn-secondary`, `.btn-outline`, `.btn-block` |
| Cards | `.listing-card`, `.stat-card`, `.faq-item` |
| Layout grids | `.cards-grid`, `.stats-grid`, `.detail-layout`, `.detail-grid`, `.contact-grid`, `.footer-grid` |
| Detail page | `.gallery-main`, `.gallery-thumbs`, `.detail-sidebar`, `.info-card`, `.amenities-list`, `.map-placeholder` |
| Ratings | `.rating-bar-container`, `.rating-bar`, `.rating-fill`, `.rating-row`, `.rating-bar-bg`, `.rating-bar-fill` |
| Forms | `.filter-group`, `.contact-form` |
| Footer | `.site-footer`, `.footer-col`, `.footer-bottom` |

## Responsive Design

- Every page declares `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Page layouts are built on CSS Grid and Flexbox so content can reflow between desktop, tablet and mobile
- Images use `object-fit: cover` to keep consistent proportions
- Target devices for Assignment 2: **mobile, tablet and desktop**

When you finalise the stylesheet, document your breakpoints here, for example:

| Device | Width | Layout notes |
|--------|-------|--------------|
| Mobile | up to 600px | _fill in_ |
| Tablet | 601px to 1024px | _fill in_ |
| Desktop | 1025px and above | _fill in_ |

## Accessibility and Semantics

- Language set with `<html lang="en">`
- Descriptive `alt` text on images (for example "Self Contained Room Main View")
- Landmark elements used for navigation, main content and footer
- Form fields have visible labels
- Suggested improvements: associate every `<label>` with its input using `for`/`id`, add `aria-current="page"` to the active nav link, and check colour contrast of muted text on the dark background

## Getting Started

### Prerequisites
- A modern browser (Chrome, Edge, Firefox or Safari)
- An internet connection (Unsplash images load from the web)
- Optional: VS Code with the Live Server extension

### Run locally

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd freetown-student-housing

# 2. Open the site
# Option A: open index.html directly in your browser
# Option B: serve it locally
python -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

### GitHub Pages
1. Push the project to a GitHub repository
2. Go to **Settings, then Pages**
3. Under **Source**, choose the `main` branch and the `/ (root)` folder
4. Save, and your site will be live at `https://<username>.github.io/<repo-name>/`

Use consistent lowercase file names with no spaces. GitHub Pages is case-sensitive, so `CSS/main.css` must match exactly.

## Testing Checklist

- [ ] All five pages open without errors
- [ ] Every navigation link and footer link goes to the right page
- [ ] The stylesheet loads on every page
- [ ] Images load and keep their proportions
- [ ] Layouts checked at mobile, tablet and desktop widths
- [ ] Forms display correctly and fields are usable on touch screens
- [ ] HTML validated with the [W3C Markup Validator](https://validator.w3.org/)
- [ ] CSS validated with the [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)
- [ ] Tested in at least two browsers

## Known Issues and Roadmap

### Known issues to fix
- `listings.html` links its first card to `../pages/listing detail & booking request.html` (spaces and ampersand); it should point to `listing_detail___booking_request.html`
- The other listing cards link to `detail.html`, but the file is named `details.html`
- Footer links in the inner pages use `index.html`, which resolves to `pages/index.html`; they should be `../index.html`
- The two detail pages use different class names and structure; consolidate into one
- Header markup differs between pages (`ul.nav-links` versus `nav.main-nav`)
- Team section on the About page still has placeholder names and roles
- Listing cards repeat the same title ("Listings 2: self-contained room, Congo Cross")
- "Login / Register" links to the contact page or `#`

### Planned improvements
- Working filters and sorting with JavaScript
- Real map integration for listings and campus
- Login and registration for students and landlords
- Working contact form and booking request submission
- Favourites saved per user
- Landlord dashboard for adding and managing listings
- Reporting button for suspicious listings
- Support for the other four campuses

## Assignment Deliverables

| Deliverable | Status |
|-------------|--------|
| Source code (minimum 5 pages) | Included in this repository |
| Responsive website (mobile, tablet, desktop) | Included |
| GitHub repository | This repository |
| Screenshots | Included in `screenshots/` and shown above |
| A3 design board | Submitted separately |

| | |
|---|---|
| **Course** | DCOMP204 – Web Design 1 |
| **Assignment** | Assignment 2 – HTML, CSS & Responsive Website |
| **Institution** | Limkokwing University of Creative Technology, Sierra Leone Campus |
| **Faculty** | Faculty of ICT |

## Contact

- Email: support@fsh.sl
- Phone: +232 88 176 514
- Address: Limkokwing University, Freetown Campus, Freetown, Sierra Leone
- Hours: Monday to Friday, 9am to 5pm

## Credits

- **Author:** JNO
- **Photography:** [Unsplash](https://unsplash.com)
- **Prototype:** Figma (Assignment 1)

> This project was created for academic purposes. Listings, prices, statistics, names and contact details are sample content.
