# Mustapha Abubakar Qurami — Personal Portfolio

An 8-page personal portfolio website built for the **COEN 554 Web Programming**
examination, Question One (Department of Computer Engineering, Ahmadu Bello
University, Zaria).

## Live requirement compliance

- **No JavaScript.** No `.js` files, no inline scripts, no frameworks, no CMS.
- Built only with **HTML5, CSS3 (Flexbox, Grid, media queries), JSON, and
  JSON-LD**.
- All interactivity (mobile navigation, project category filter) is done with
  pure CSS using the checkbox/radio-button technique.

## Directory structure

```
portfolio/
├── index.html          Home
├── about.html           About Me
├── education.html       Educational Background
├── skills.html          Technical Skills
├── projects.html        Projects (CSS-only category filter)
├── hobbies.html         Hobbies & Interests
├── cv.html               Curriculum Vitae
├── contact.html          Contact Me
├── css/
│   ├── reset.css         Minimal CSS reset
│   ├── style.css         Design system: variables, typography, components
│   └── responsive.css    Breakpoint refinements + print styles
├── data/
│   └── data.json          Structured portfolio data (see below)
├── images/
│   ├── front-image.jpg    Homepage hero portrait
│   ├── about-portrait.jpg Secondary portrait (About page)
│   └── projects/          Project images
└── README.md
```

## Colour system

Built around the required combination:

```css
:root {
  --lemon-chiffon: #FEFACD;
  --ultra-violet: #5F4A8B;
}
```

All other tones (deep violet for headers/footers, pale violet tints for
chips and cards, warm neutral borders) are derived from this pair so the
whole site reads as one consistent identity.

## `data/data.json`

A single structured JSON file modelling the portfolio's content as
entities: `personal`, `education`, `certifications`, `skills`, `projects`,
`hobbies`, and `contact`. It exists as the required structured-data
architecture for the examination; because JavaScript is prohibited, the
HTML pages do not fetch it dynamically — instead its schema documents how
the site's content is organised, and its fields (id, category, status,
technology, etc.) mirror what's written directly into each page's markup.

## JSON-LD

Every page embeds a `schema.org/Person` JSON-LD block in its `<head>`,
describing Mustapha as a person with an affiliation, education history,
and areas of knowledge. This is structured metadata for search engines and
data consumers — it performs no logic and is not a substitute for the
JavaScript that is deliberately absent from this project.

## Notes on content accuracy

Per the examination's no-fabrication requirement, this site does **not**
invent a graduation date, GPA, employment history, or unconfirmed
credentials. The CCNA certification is explicitly marked "currently
pursuing," not completed. Contact details (email and phone) were supplied
by the site owner and reused from an earlier version of this portfolio.

## Viewing the site

Open `index.html` directly in any modern browser — no build step, server,
or dependency installation is required.

https://mustyabu8.github.io/my_portfolio/
