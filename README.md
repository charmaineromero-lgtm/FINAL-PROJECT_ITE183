# FINAL-PROJECT_ITE183

# ViaGraph

**ViaGraph** is a web-based transport guide designed to help commuters—especially **MSU-IIT students** and **non-locals**—navigate **Iligan City** using jeepney and minibus routes. The platform visualizes real commuting paths, simplifies route selection, and lays the foundation for fare computation and user-based personalization.

---

## Project Overview

ViaGraph follows a **modular, data-driven architecture**:

- **HTML / CSS** – User interface and layout  
- **JavaScript** – Map logic and routing behavior  
- **GeoJSON** – Accurate route and path visualization  
- **Leaflet.js** – Interactive mapping library  

Each component has a clear responsibility, making the system **easy to maintain, extend, and scale**.

---

## Website Flow

### 1. Index / Sign-In Page (`index.html`)

**Entry point of the ViaGraph website**

#### Purpose
- Introduce ViaGraph
- Allow users to sign in or proceed to registration

#### Key Features
- Clean, centered layout with ViaGraph branding
- Email and password input fields
- Sign-in button that redirects to `home.html`
- Optional Google sign-in button (UI-ready)
- Responsive and desktop-friendly design

---

### 2. Main Dashboard (`home.html`)

The **core interface** where users interact with ViaGraph.  
The dashboard is divided into **three main sections**, guiding users from context to route planning.

---

### A. About Iligan City

#### Purpose
- Provide contextual and geographic information
- Help non-locals and students become familiar with the city

#### Displayed Content
- Popular tourist spots and landmarks
- Key areas and destinations
- Brief descriptions for cultural and geographic context

This section helps users understand **where they are navigating**, not just **how to commute**.

---

### B. About ViaGraph (Value Proposition)

#### Purpose
- Explain what ViaGraph is and what it offers

#### Highlights
- Optimized jeepney and minibus routing
- Student-friendly fare awareness
- Accurate, map-based visualization of real routes
- Designed specifically for **MSU-IIT students and non-locals**

---

### C. Route Finder (Core Feature)

The **main functionality** of ViaGraph.

#### User Actions
- Select an **origin point**
- Select a **destination point**
- Choose **passenger type**:
  - Regular
  - Student
  - Senior
  - PWD
- Click **Search / Find Route**

#### System Output
- Computes the optimal route using available jeepney and minibus paths
- Visually draws the route on the map
- Displays detailed route information in a side panel

#### Route Information Panel
- **Transportation Type**: Jeepney / Minibus  
- **Stops**: Specific stops (if applicable)  
- **Transfer Points**: If transfers are required  
- **Fare Breakdown**:
  - Jeepney fare (Regular vs Student/Senior/PWD)
  - Minibus fare (Regular vs Student/Senior/PWD)
- **Route Notes**: (e.g., Direct route, With transfer)
- **Estimated Total Fare**

---

## Map Logic (`map.js`)

Handles all **map-related behavior**.

### Responsibilities
- Initialize the Leaflet map
- Set the default view to **Iligan City**
- Load map layers (Standard & Satellite views)
- Populate origin and destination dropdowns
- Manage user selections (origin, destination, passenger type)
- Render selected routes on the map

> **Key Concept:**  
> `map.js` controls **how routes are displayed**, not **what the routes are**.

---

## Route Data (`routes.js` / `routes.json`)

Stores all **actual jeepney and minibus routes**.

### Contents
- GeoJSON `FeatureCollection` objects
- `LineString` geometries
- Detailed GPS coordinate sequences

### Example Routes
- Tambo Terminal routes
- Dalipuga routes
- Pala-o routes
- Ubaldo routes
- Santiago & San Miguel routes
- Minibus routes

---

## Target Users

- **MSU-IIT students**
- **Newcomers and tourists**
- **Non-local commuters**
- **Daily jeepney and minibus riders**

---

## Future Enhancements
- Fare computation automation
- Route recommendations based on user history
- User profiles and personalization
- Real-time traffic and route updates

---

> ViaGraph aims to make commuting in Iligan City **clear, visual, and student-friendly**.
