# PROJECT_VIAGRAPH

## Project Purpose

**ViaGraph** is a web-based transportation guide designed to assist **MSU-IIT students**, **non-local commuters**, and **first-time visitors** in navigating jeepney and minibus routes within **Iligan City**.
The project aims to simplify route selection by visually displaying real transportation paths on an interactive map, while also providing fare-related information based on passenger type (regular, student, senior, or PWD).

By combining map visualization and structured route data, ViaGraph helps users understand **where to go**, **how to get there**, and **what to expect when commuting**, addressing common challenges faced by non-locals in urban public transportation.

---

## Technologies Used

* **HTML5** – Structure and content of the web pages
* **CSS3** – Layout, styling, and responsive design
* **JavaScript** – Core logic, routing behavior, and user interaction
* **Leaflet.js** – Interactive map rendering and visualization
* **GeoJSON** – Storage and representation of actual jeepney and minibus routes

---

## Proponents

**Project Leader:**

* *Jevelou Suba-an*

**Members:**

* *Dominique Anne Cominguez*
* *Charmaine Hazel L. Romero*

---

## System Overview

ViaGraph follows a **modular, data-driven architecture**, where each component has a specific responsibility. This design ensures maintainability, scalability, and ease of future enhancement.

The system consists of:

* A user-facing web interface
* JavaScript logic for routing and interaction
* Predefined transportation route data
* A map visualization layer

---

## System Block Diagram

```
[ User ]
   |
   v
[ Web Interface (HTML / CSS) ]
   |
   v
[ JavaScript Logic ]
   |
   v
[ Route Data (GeoJSON) ]
   |
   v
[ Leaflet.js Map Visualization ]
```

**Block Diagram Explanation:**

* The **user** interacts with the system through a web browser.
* The **web interface** collects user inputs such as origin, destination, and passenger type.
* **JavaScript logic** processes the inputs and determines the appropriate route.
* **GeoJSON route data** provides real-world jeepney and minibus paths.
* **Leaflet.js** renders the computed route on an interactive map.

---

## Website Flow

### 1. Index / Sign-In Page (`index.html`)

**Purpose:**

* Serve as the entry point of the ViaGraph website
* Allow users to sign in or proceed to the main dashboard

**Key Features:**

* ViaGraph branding and introductory layout
* Email and password input fields
* Sign-in button redirecting to `home.html`
* Optional Google sign-in button (UI-ready)
* Responsive design for desktop use

---

### 2. Main Dashboard (`home.html`)

The main dashboard is the **core interface** of ViaGraph and is divided into three major sections.

---

### A. About Iligan City

**Purpose:**

* Provide geographic and contextual background
* Help non-locals familiarize themselves with the city

**Content Includes:**

* Popular landmarks and tourist destinations
* Key areas and locations within Iligan City
* Brief descriptions for geographic orientation

---

### B. About ViaGraph

**Purpose:**

* Present the system’s value proposition

**Highlights:**

* Visualized jeepney and minibus routes
* Student-friendly fare awareness
* Route clarity and transfer identification
* Designed specifically for MSU-IIT students and non-locals

---

### C. Route Finder (Core Feature)

**User Inputs:**

* Origin point
* Destination point
* Passenger type:

  * Regular
  * Student
  * Senior
  * PWD

**System Output:**

* Displays the optimal transportation route
* Renders the route visually on the map
* Shows detailed commuting information

**Route Information Panel Displays:**

* Transportation type (Jeepney or Minibus)
* Route stops (if applicable)
* Transfer points (if any)
* Fare breakdown by passenger type
* Route notes (Direct / With transfer)
* Estimated total fare

---

## Map Logic (`map.js`)

The `map.js` file manages all **map-related functionality**.

**Responsibilities:**

* Initialize the Leaflet map
* Set the default map view to Iligan City
* Load base layers (standard and satellite views)
* Populate origin and destination dropdowns
* Handle user selections
* Render selected routes on the map

**Key Concept:**
`map.js` controls **how routes are displayed**, not **what routes exist**.

---

## Route Data (`routes.js` / `routes.json`)

This component stores all **actual jeepney and minibus routes** used by the system.

**Contents Include:**

* GeoJSON `FeatureCollection` objects
* `LineString` geometries
* GPS coordinate sequences representing real routes

**Example Routes:**

* Tambo Terminal routes
* Dalipuga routes
* Pala-o routes
* Ubaldo routes
* Santiago and San Miguel routes
* Minibus routes

---

## Target Users

* MSU-IIT students
* Non-local commuters
* New residents and tourists
* Daily jeepney and minibus passengers

---

## Future Enhancements

* Automated fare computation
* Route recommendations based on user history
* User accounts and personalization
* Real-time traffic and route updates

---
