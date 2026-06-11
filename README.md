# Pressure Playground 🍅⚡

An interactive, browser-only educational site that teaches **Pressure = Force ÷ Area** to school students (Class 9–11). No server, no build step — just open the HTML files in any modern browser.

---

## Pages

| Page | File | Description |
|------|------|-------------|
| 🍅 **Play** | `index.html` | Interactive game: choose a knife, hold PRESS, watch a tomato get sliced — or squished. Demonstrates P = F/A live. |
| 📖 **Learn** | `learn.html` | Full learning module: 6 sections, 7 animated/interactive diagrams, 3 real-world story cards, 6 solved examples, and a 7-question quiz. |

---

## Project Structure

```
/
├── index.html          ← Game page (original; nav bar added)
├── learn.html          ← Learn module
├── css/
│   └── learn.css       ← All styles for learn.html (uses same design tokens as game)
├── js/
│   └── learn.js        ← All interactivity: animations, quiz, TOC scroll-spy
└── README.md
```

---

## Learn Module — What's Inside

### Section 1 · Introduction to Pressure
- Definition, P = F/A formula
- **Interactive area toggle** — same block, small vs large area; pressure arrows + heatmap update live
- Relatable pressure comparison cards (grain of salt → deep ocean)
- Pressure vs Force vs Stress comparison table
- **Flip cards** (tap to reveal) — 4 common misconceptions debunked

### Section 2 · Types of Pressure
- **Tabbed panel** covering Atmospheric, Gauge, Absolute, Hydrostatic, Vapor pressure
- **Altitude animation** — balloon rises, pressure reading drops in real time
- **Hydrostatic tank** — depth slider moves a diver; wall arrows grow with depth; live P = ρgh readout

### Section 3 · Key Laws & Principles
Each law has a smooth SVG animation with a Replay button:
- **Pascal's Law** — small piston pressed → car lifts on large piston
- **Archimedes' Principle** — object lowered into water; water level rises; buoyant force arrow appears; float/sink toggle
- **Bernoulli's Principle** — coloured particles flow through narrow pipe; speed up; labels show high/low pressure zones
- **Boyle's Law** — slider compresses gas in a cylinder; pressure doubles as volume halves; dots redistribute

### Section 4 · Real-World Applications (3 detailed stories)
1. 🚗 **Hydraulic Brakes** — step-by-step Pascal's Law story with master/slave cylinder diagram
2. 🫀 **Blood Pressure** — systolic/diastolic explained simply with an animated gauge
3. 🌦️ **Weather Barometer** — Torricelli's mercury tube, high/low pressure, weather prediction

### Section 5 · Solved Examples
6 expandable worked problems (Easy → Moderate → Hard):
- P = F/A (find pressure and force)
- P = ρgh (hydrostatic depth)
- Boyle's Law (volume halved → pressure doubled)
- Real-world comparison (high heels vs sneakers)
- Dam base pressure (P = ρgh at 30 m)

Each card: question visible → click **Show Solution** → Given / Formula / Substitution / Answer

### Section 6 · Quiz
- 7 questions (6 MCQ + 1 easy numerical)
- One question at a time, progress bar, score tracker
- 💡 Hint button per question
- Instant feedback with explanation after every answer
- Results screen with encouraging message; confetti on 6/7 or 7/7 ✨

---

## How to Open Locally

1. Download or clone this folder.
2. Open `index.html` **or** `learn.html` in any modern browser (Chrome, Firefox, Safari, Edge).
3. No internet required after the first load (Google Fonts are the only external resource).

```bash
# Or serve with Python for the cleanest experience:
python -m http.server 8000
# then visit http://localhost:8000
```

---

## Design System

The Learn module uses the exact same tokens as the game:

| Token | Value | Used for |
|-------|-------|----------|
| `--cream` | `#FFF6E9` | Page background |
| `--tomato` | `#FF5A4E` | Active nav, badges, accents |
| `--leaf` | `#58B368` | Correct answers, buoyancy |
| `--pressure` | `#A04EF6` | Pressure formula, TOC active |
| `--force` | `#FF9F2E` | Force arrows, moderate badges |
| `--area` | `#3E8BFA` | Area, water, Bernoulli pipe |
| Fonts | Fredoka (headings) + Nunito (body) | Google Fonts |

---

## Accessibility & Compatibility

- Semantic HTML (`<nav>`, `<main>`, `<section>`, `aria-label`, `role`)
- Keyboard operable: flip cards (Enter/Space), tabs, quiz options
- `prefers-reduced-motion` respected — all animations and transitions disabled
- Responsive down to **360 px** wide; sidebar TOC collapses on mobile
- No frameworks, no build step, no Node.js — pure HTML + CSS + vanilla JS
