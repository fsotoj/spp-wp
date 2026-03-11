# Subnational Politics Project (SPP) - Hero Layer

This repository contains the front-end "Hero Layer" and landing page for the **Subnational Politics Project (SPP)**. The SPP provides systematic, transparent, and publicly accessible data on subnational political institutions and electoral outcomes across Latin American countries.

This specific codebase acts as a lightweight, interactive landing page (built with HTML, CSS, and Vanilla JavaScript) that seamlessly integrates and wraps the core analytical tool: a **Shiny R Dashboard**.

## Features

- **Interactive Hero Section:** A sleek, animated landing page that introduces the project and its goals.
- **Shiny Dashboard Integration:** Embeds the main SPP Shiny dashboard (hosted on Hugging Face) via an `iframe`, creating a unified user experience. Cross-origin communication (`postMessage`) is used to handle transitions and events between the hero layer and the Shiny app.
- **About & Documentation Flow:** Includes built-in layers detailing the project's background, the team behind the SPP, database structures, and citation references.
- **Analytics Integration:** Configured to receive Google Analytics events directly from the embedded Shiny dashboard, enabling unified tracking across the front-end and the R backend.

## Architecture

- `index.html`: The main entry point. It contains the DOM structure for the Hero layer, the About layer, and the `iframe` that loads the Shiny application.
- **Styling:** Custom Vanilla CSS for animations, responsive design, layered visibility toggling (e.g., bringing up the dashboard or the About section), and typography.
- **Interactivity:** Vanilla JavaScript manages DOM manipulation, scroll events, map animations, and the `postMessage` event listeners.

## The SPP Databases

The project compiles multiple databases with a country–state–year structure:
- **SED:** Subnational Executive Database
- **SEED:** Subnational Executive Elections Database
- **SLED:** Subnational Legislative Elections Database
- **SDI:** Subnational Democracy Indices
- **CFTDFLD:** Capital Federal & Tierra del Fuego Legislatures Database
- **NED:** National Executive Database

Data can be explored via the dashboard or downloaded directly from the [Harvard Dataverse](https://dataverse.harvard.edu/dataverse/spp).

## Team

- **Agustina Giraudy** (American University / Tecnológico de Monterrey) - Principal Investigator
- **Francisco Urdinez** (Universidad Católica de Chile) - Collaborator
- **Guadalupe González** (University of Maryland, College Park) - Collaborator
- **Felipe Soto Jorquera** (Hertie School, Berlin) - Collaborator
- **Sergio Huertas Hernández** (Universidad Católica de Chile) - Research Assistant

## Usage

Since this is a static HTML/JS/CSS project, you can simply open `index.html` in any modern web browser or serve it using a basic local web server:

```bash
# Example using Python 3
python -m http.server 8000
```

Then navigate to `http://localhost:8000` to view the hero layer and access the dashboard.
