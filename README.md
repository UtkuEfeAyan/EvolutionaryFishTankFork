# Evolutionary Fish Tank

An interactive, browser-based fish tank simulation where fish evolve over time through natural selection, predation, and genetic inheritance — built with [p5.js](https://p5js.org/).

🔗 **[Live Demo on GitHub Pages](https://UtkuEfeAyan.github.io/Evolutionary-Fish-Tank/)**

---

## Overview

Fish live in a shared tank, eat plankton or each other, breed with compatible partners, and pass on their traits to offspring — with small random mutations each generation. Over time, the population naturally adapts to the conditions you set.

## Features

- **Evolutionary genetics** — offspring inherit blended traits (speed, size, fin size, color, aggression, lifespan, salinity preference) with random mutations
- **Two diets** — herbivores eat plankton; carnivores hunt herbivores
- **State machine AI** — fish wander, hunt prey, or flee predators based on a cone-shaped field of vision
- **Salinity system** — each fish has a preferred salinity level and a tolerance range; fish outside their tolerance gradually lose health
- **Interactive side panel** — click any fish to inspect its live stats (name, energy, health, age, speed, aggression, diet, salinity preference, and more)
- **Fish Almanac** — browse the history of fish that have lived in the tank
- **Custom fish creator** — design and spawn your own fish with hand-picked traits
- **Clone fish** — clone a selected fish directly into the tank
- **Real-time controls**:
  - **Tick speed** slider — fast-forward or slow down simulation time
  - **Plankton rate** slider — control how quickly new plankton spawns
  - **Salinity** slider — adjust the tank's salt level and watch fish adapt (or die)

## Controls

| Action | How |
|---|---|
| Inspect a fish | Click on any fish |
| Dismiss side panel | Click elsewhere in the tank |
| Adjust tick speed | Use the **Tick Speed** slider |
| Adjust plankton spawn rate | Use the **Plankton Rate** slider |
| Adjust salinity | Use the **Salinity** slider |
| Clone selected fish | Click **Clone Fish** (visible when a fish is selected) |
| Create a custom fish | Use the **Custom Fish** panel |

## Tech Stack

- **[p5.js](https://p5js.org/) v1.9.0** — rendering and animation
- Vanilla HTML / CSS / JavaScript — no build step required

## Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/UtkuEfeAyan/Evolutionary-Fish-Tank.git
   ```
2. Open `index.html` in your browser (a local server is recommended to avoid CORS issues with asset loading, e.g. `npx serve .` or the VS Code Live Server extension).

## Project Structure

```
Evolutionary-Fish-Tank/
├── index.html
├── css/
│   └── style.css
├── js/
│   ├── sketch.js               # Main p5.js setup/draw loop and global state
│   └── components/
│       ├── fishclass.js        # Fish class (traits, AI, breeding, display)
│       ├── updatefish.js       # Fish update logic
│       ├── planktonclass.js    # Plankton class
│       ├── updateplankton.js   # Plankton update logic
│       ├── tankbackground.js   # Tank background rendering
│       ├── sidepanel.js        # Selected-fish stats panel
│       ├── almanac.js          # Fish history almanac
│       └── feeder.js           # Draggable food-dispenser widget that drops plankton into the tank
└── assets/
    ├── fish.json               # Starting fish data
    ├── fishnames.json          # Random fish name pool
    └── *.png                   # Images used in the UI
```
