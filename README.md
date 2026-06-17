# Student Portfolio Website

A multi-page personal portfolio website built as part of a college internship project.
The focus is on writing correct semantic HTML5, following web accessibility standards
(WCAG 2.1), and achieving high Lighthouse Accessibility and SEO scores — using only
HTML and CSS, with no frameworks or JavaScript.

---

## Pages

| File | Page |
|---|---|
| `index.html` | Home — introduction and site overview |
| `about.html` | About — background, skills, education |
| `projects.html` | Projects — three sample projects |
| `contact.html` | Contact — accessible contact form |
| `style.css` | Shared stylesheet for all pages |

---

## Features

- Four-page portfolio with consistent header, navigation, and footer
- Hero section on home page with introduction and call-to-action buttons
- Skills, education, and personal details on the About page
- Three project cards with technology tags and status indicators
- Accessible contact form with name, email, subject, and message fields
- Responsive layout that works on mobile, tablet, and desktop
- Single external CSS file — no inline styles, no frameworks

---

## Accessibility Features (WCAG 2.1)

- **Skip-to-content link**: Hidden link at the top of every page that appears on keyboard focus, letting keyboard users jump past navigation directly to the main content
- **Semantic HTML**: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` used throughout instead of generic `<div>` containers
- **Heading hierarchy**: One `<h1>` per page; `<h2>` for sections; `<h3>` for sub-items — consistent across all pages
- **ARIA labels**: `aria-label` on navigation (`<nav aria-label="Main navigation">`), buttons with shared text (`aria-label="View source code for ... on GitHub"`), and lists
- **ARIA current page**: `aria-current="page"` on the active navigation link so screen readers announce which page is active
- **ARIA required**: `aria-required="true"` on all required form inputs, alongside the HTML `required` attribute
- **ARIA describedby**: Form inputs linked to helper text and the required-fields note using `aria-describedby`
- **Visible focus indicator**: A 3px golden outline (`#f0a500`) appears on all interactive elements when focused via keyboard — overrides browser defaults which are sometimes invisible
- **Label/input association**: Every form input has a `<label>` with a matching `for`/`id` pair
- **Decorative elements hidden**: The avatar circle uses `aria-hidden="true"` so screen readers skip it
- **`aria-hidden` on decorative asterisks**: The `*` used to mark required fields is hidden from screen readers; the word "asterisk" is provided in visually-hidden text instead
- **`.visually-hidden` utility class**: Hides elements visually while keeping them in the accessibility tree
- **`lang="en"` on `<html>`**: Tells screen readers which language to use for pronunciation
- **`prefers-reduced-motion` media query**: Disables transitions and smooth scrolling for users who have enabled the reduced motion setting in their OS
- **Sufficient colour contrast**: All text/background colour pairs were checked to meet WCAG AA (4.5:1 for normal text, 3:1 for large text)
- **Keyboard-friendly navigation**: All interactive elements are focusable and operable using keyboard alone
- **`tel:` and `mailto:` links**: Phone and email details are real links that activate the relevant app on mobile and desktop
- **Descriptive link text**: Avoids "click here" — every link describes its destination or action

---

## SEO Features

- Unique `<title>` tag on every page
- Unique `<meta name="description">` on every page
- `<meta name="keywords">` on every page
- `<meta name="author">` on every page
- `<meta name="viewport">` for responsive display
- Meaningful heading structure for search engine crawlers
- Semantic HTML elements help search engines understand content roles
- `aria-current="page"` helps reinforce page structure signals

---

## Technologies Used

- HTML5
- CSS3 (custom properties, Flexbox, Grid, media queries)
- No JavaScript
- No CSS frameworks (no Bootstrap, no Tailwind)
- No external fonts (system font stack used)

---

## Folder Structure

```
portfolio/
├── index.html       ← Home page
├── about.html       ← About Me page
├── projects.html    ← Projects page
├── contact.html     ← Contact page
├── style.css        ← Shared stylesheet
└── README.md        ← This file
```

---

## How to Run Locally

No build tools or server are required. This is a static site — just open the HTML files directly in a browser.

**Option 1 — Open directly:**
1. Download or clone this repository
2. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari)

**Option 2 — VS Code Live Server (recommended for development):**
1. Install [Visual Studio Code](https://code.visualstudio.com/)
2. Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
3. Right-click `index.html` → "Open with Live Server"
4. The site opens at `http://127.0.0.1:5500`

---

## Lighthouse Scores (Target)

| Category | Target |
|---|---|
| Accessibility | ≥ 95 |
| SEO | ≥ 95 |
| Best Practices | ≥ 90 |

To run a Lighthouse audit: open Chrome → DevTools → Lighthouse tab → Generate report.

---

## Author

**Student**  
Web Development Student  
Tamil Nadu, India  
student123@example.com
