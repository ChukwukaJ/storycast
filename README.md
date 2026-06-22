# StoryCast — Accessible Media Microsite

A 3-page accessible microsite showcasing audio and video storytelling from African creatives and the diaspora. Built with semantic HTML5, Sass, CSS Grid, Flexbox, and container queries. No frameworks.

## Pages

- `index.html` — Home page with featured story and story grid
- `story/episode-one.html` — Story detail page with audio, video, transcript, and sidebar
- `about.html` — Mission, accessibility features, and how to engage

## Project Structure

    storycast/
    ├── index.html
    ├── about.html
    ├── story/
    │   └── episode-one.html
    ├── sass/
    │   ├── tokens/
    │   ├── components/
    │   ├── layout/
    │   └── main.scss
    ├── css/
    │   └── main.css
    ├── assets/
    │   └── transcripts/
    │       └── ep1-captions.vtt
    └── README.md

## Running Locally

1. Install Sass: `npm install -g sass`
2. Compile: `sass sass/main.scss css/main.css --watch`
3. Open `index.html` in your browser or use Live Server in VS Code

## Accessibility Checklist

| Requirement | How it's met |
|---|---|
| Semantic HTML5 | nav, main, article, section, aside, figure, figcaption, header, footer used throughout |
| Heading hierarchy | h1 once per page, followed by h2 and h3 in logical order |
| Audio accessibility | Native audio controls with figcaption and full inline transcript |
| Video captions | track kind="captions" with .vtt file, set as default |
| Skip link | "Skip to main content" visible on keyboard focus on every page |
| ARIA labels | aria-label on navs, aria-labelledby on all sections, aria-current="page" on active nav link |
| Transcript region | role="region", aria-label, tabindex="0" for keyboard scroll |
| Colour contrast | Gold #E8C547 on near-black #0D0D0D = 10.6:1 ratio (exceeds AA 4.5:1) |
| Focus states | focus-visible outline on all interactive elements globally |
| Reduced motion | prefers-reduced-motion disables all transitions and scroll behavior |
| Keyboard navigation | All links and media controls reachable via Tab key |
| Container query | media-card--featured switches to horizontal grid via @container at 500px |
| Responsive grid | story-grid collapses 3-col to 2-col to 1-col via media queries |

## Design Decisions

- Dark theme — reduces eye strain for long listening sessions
- Playfair Display for editorial warmth, Inter for UI clarity, JetBrains Mono for transcripts
- Gold accent #E8C547 — warmth of candlelight and voice, specific to the platform identity
- Container queries on the featured card respond to component size, not just viewport