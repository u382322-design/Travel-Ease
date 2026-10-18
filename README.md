# TravelEase &mdash; Modern Travel Agency Website

A modern, responsive, and accessible travel agency website developed for a fictional travel company named **TravelEase**. This project is engineered specifically as a showcase for a professional Frontend Developer CV and portfolio.

Built strictly with **semantic HTML5**, **modern CSS3**, **Bootstrap 5**, **vanilla JavaScript (ES6+)**, and **Bootstrap Icons**. Zero heavy frontend frameworks (no React, Vue, or Angular) were utilized, highlighting deep mastery of core web fundamentals, DOM manipulation, client-side algorithms, and accessible UI engineering.

---

## 🌟 Key Highlights & Engineering Features

### 1. Visual Branding & Modern Aesthetics
- **Travel Palette:** Harmonious combination of Ocean Blue (`#0a3d62`), Teal (`#00a896`), Warm Sand (`#f4ede2`), and pure white with soft multi-layered elevation shadows.
- **Micro-Interactions & Transitions:** Card hover elevations, image zoom zooms, focus outline rings (`:focus-visible`), and smooth scrolling respecting `prefers-reduced-motion`.
- **Custom Vector Graphics:** Custom brand SVG logo (`assets/images/logo.svg`, `logo-white.svg`) and compass favicon (`assets/icons/favicon.svg`).

### 2. Comprehensive Destination Catalogue (14 Packages)
- Covers 6 continents with varied categories: **Beach & Island**, **Cultural & Heritage**, **Adventure**, **Luxury**, and **Domestic** getaways.
- Each package contains:
  - Unique alphanumeric ID
  - Destination name, Country, Region
  - Illustrative demo price and currency (e.g. `$1,850 USD`)
  - Detailed duration (days and nights)
  - Demo availability status (`Available`, `Filling Fast`, `Demo Waitlist`)
  - Curated high-resolution imagery and gallery photos
  - In-depth day-by-day itineraries
  - Included activities, inclusions, and exclusions
  - Clearly labelled illustrative demo ratings and reviews

### 3. Reactive JavaScript Modules
- **Dynamic Catalogue Filtering & Search (`js/filters.js`):**
  - Instant text search across destination name, country, region, and activity keywords.
  - Multi-category pill filters (All, Beach, Cultural, Adventure, Luxury, Domestic, International).
  - Multi-tier budget select filter (Under $1,500, $1,500-$2,500, $2,500-$3,500, $3,500+).
  - Duration filter (Short 1-4 days, Medium 5-7 days, Long 8+ days).
  - Multi-criteria sorting (Featured, Price: Low to High, Price: High to Low, Duration: Short to Long, Duration: Long to Short, Name: A-Z, Rating).
  - URL Query Parameter Synchronization (e.g. search on homepage seamlessly filters `destinations.html?q=japan&category=Cultural`).
  - Screen-reader accessible live announcement (`aria-live="polite"`) and graceful Empty State UI with "Reset Filters" action.
- **Dynamic Package Detail Renderer (`js/validation.js`):**
  - Reads `?id=[destination-id]` and renders hero gallery, key trip stats, long overview, activity chips, day-by-day timeline, and sticky booking card.
- **Robust Client-Side Validation (`js/validation.js`):**
  - **Booking Form:** Validates name, email, reasonable phone format, selectable destination, future departure date (tomorrow or later), return date strictly after departure, positive traveler count (1–10), special requests, and mandatory demo consent checkbox.
  - **Real-time Price Calculator:** Computes estimated total price on-the-fly (`unit price * travelers`).
  - **Simulated Confirmation Modal:** Displays a reference ID (e.g., `TE-DEMO-849201`), traveler breakdown, total estimate, print summary button, and clear disclaimer that no financial transaction occurred.
  - **Contact Form:** Validates name, email, subject, message length, and displays accessible confirmation.
  - **Newsletter Form:** Real-time email validation and toast notification.

### 4. SEO & Accessibility (WCAG 2.1 AA)
- Semantic landmarks (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`).
- Strict H1 &rarr; H2 &rarr; H3 heading hierarchy on all 8 pages.
- Skip to main content link for keyboard and screen reader accessibility.
- Unique page `<title>`, `<meta name="description">`, Open Graph social preview tags, and canonical tags.
- Descriptive image `alt` attributes and lazy loading (`loading="lazy"`).
- Structured Data (JSON-LD `TravelAgency`) accurately labelled for portfolio demonstration.
- `robots.txt` and `sitemap.xml` included.

---

## 📁 Project Structure

```text
TravelEase/
├── index.html                   # 13-section modern travel homepage
├── destinations.html            # Interactive catalogue with search & multi-tier filters
├── packages.html                # Curated bundles comparison & filtering
├── destination-details.html     # Dynamic day-by-day itinerary & booking sidebar
├── booking.html                 # Comprehensive booking request form with live calculator
├── about.html                   # Brand story, core values, fictional team & CV notes
├── contact.html                 # Contact form, office directory & location map
├── privacy.html                 # Ethical data policy & portfolio transparency
├── css/
│   └── style.css                # Custom CSS3 styles, variables & animations
├── js/
│   ├── destinations.js          # 14 demo packages data & query helper methods
│   ├── main.js                  # Navbar scroll, mobile nav, newsletter & toast alerts
│   ├── filters.js               # Reactive search, category, budget, duration & sort
│   └── validation.js            # Booking/contact form validation & modal confirmations
├── assets/
│   ├── icons/
│   │   └── favicon.svg          # SVG brand compass favicon
│   └── images/
│       ├── logo.svg             # Primary brand logo
│       └── logo-white.svg       # Dark-background / footer brand logo
├── robots.txt                   # Search crawler directives
├── sitemap.xml                  # XML sitemap indexing all 8 pages
└── README.md                    # Detailed documentation & portfolio guide
```

---

## 🚀 How to Run Locally

Because TravelEase is built with pure standards-compliant frontend technologies, you do not need Node.js, npm, or build tools to run it.

### Method 1: Using Python's Built-in HTTP Server (Recommended)
Open your terminal or PowerShell in the `TravelEase` directory and run:

```bash
# Python 3
python -m http.server 8000
```
Then visit [http://localhost:8000](http://localhost:8000) in your web browser.

### Method 2: Using Node.js `npx serve` or `http-server`
```bash
npx serve .
```

### Method 3: Using VS Code Live Server
1. Open the `TravelEase` folder in Visual Studio Code.
2. Right-click `index.html` and click **"Open with Live Server"**.

### Method 4: Directly in Browser
You can also double-click `index.html` to open it directly in Google Chrome, Microsoft Edge, Mozilla Firefox, or Safari.

---

## 🌐 How to Deploy for Your CV Portfolio

### Deploying to GitHub Pages (Free & Instant)
1. Initialize a git repository and commit your files:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: TravelEase modern travel agency website"
   ```
2. Create a new repository on [GitHub](https://github.com) named `travelease` or `portfolio-travelease`.
3. Push your code:
   ```bash
   git remote add origin https://github.com/<your-username>/travelease.git
   git branch -M main
   git push -u origin main
   ```
4. On GitHub, go to **Settings &rarr; Pages**.
5. Under **Branch**, select `main` and `/ (root)`, then click **Save**.
6. Your portfolio website will be live in minutes at `https://<your-username>.github.io/travelease/`!

### Deploying to Vercel or Netlify
- **Netlify:** Drag and drop the `TravelEase` folder into the Netlify dashboard for instant HTTPS deployment.
- **Vercel:** Run `npx vercel` in the project directory or import your GitHub repository.

---

## 📄 License & Attribution
- Built for professional frontend portfolio demonstration.
- Photos sourced from [Unsplash](https://unsplash.com) via royalty-free open image licenses.
- Icons by [Bootstrap Icons](https://icons.getbootstrap.com/).
