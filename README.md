# April's Game Parlor

A small, hand-made parlor of browser games. This is **Project 1** of the
CS5610 Web Development course at Northeastern University: a static,
multi-page site built with **HTML and CSS only** (no JavaScript, no CSS
frameworks). It opens with a playable, CSS-only mini crossword; the other
three games join in later projects.

**Live site:** https://aprilyanggarwood.github.io/game-parlor/

**Author:** April Yang

## Pages

- **Home** (`index.html`) — landing page introducing the parlor and its
  four game "cabinets."
- **Crossword** (`crossword.html`) — a 6x6 Seattle-themed mini crossword you
  fill in from the keyboard. Reveal a hint for any single word, or show the
  whole solution, all with pure CSS.
- **About** (`about.html`) — a short bio and a few personal photos.
- **Contact** (`contact.html`) — direct links (email, phone, GitHub,
  LinkedIn) plus a message form whose button opens the visitor's own mail app.

## How the crossword works (no JavaScript)

Each white square is a single-character `<input>`; black squares are plain
`<div>`s. Every answer sits in a hidden overlay on its cell. Revealing is
done entirely in CSS with the `:has()` selector and checkboxes: a global
"Reveal all answers" toggle, plus one "hint" toggle per clue that shows only
that word. Because pure CSS can't compare a typed letter to the solution,
the puzzle offers reveals rather than answer-checking (validation arrives in
Project 2 with Svelte).

## Built with

- Semantic HTML5
- CSS3: custom properties, Flexbox, CSS Grid, media queries, transitions and
  transforms, `:focus-visible`, `:has()`
- [Font Awesome 6](https://fontawesome.com/) icon files (used only on the
  Contact page)
- Google Fonts: Libre Baskerville and Edu SA Beginner

No JavaScript and no CSS framework are used.

## Accessibility and standards

- All four pages pass the W3C HTML validator with no errors.
- Lighthouse Accessibility: 100 on every page.
- Text meets a 4.5:1 contrast minimum; interactive targets are at least
  44x44px; navigation is keyboard-operable with a visible focus ring and a
  current-page indicator.
- Respects `prefers-reduced-motion`.

## Running locally

No build step. Clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/aprilyanggarwood/game-parlor.git
cd game-parlor
# then open index.html (double-click, or use a simple static server)
```

The photos on the About page load from the `images/` folder, so keep that
folder alongside the HTML files.

## Project structure

```
game-parlor/
├── index.html
├── crossword.html
├── about.html
├── contact.html
├── style.css          # one shared stylesheet for all pages
├── images/            # About-page photos
│   ├── april-portrait.jpg
│   ├── purple-flowers.jpg
│   ├── yellow-tulips.jpg
│   └── mountains-from-plane.jpg
└── README.md
```

## Roadmap

This site grows across the course. Planned additions: **2048** (Svelte),
**Battleship** (Express + MongoDB), and **Liar's Dice** (real-time
WebSockets).

## Credits

Fonts by Google Fonts. Icons by Font Awesome. All photographs and site
content by April Yang.
