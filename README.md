# Real Estate Project Presentation Platform (Reusable Base Plate)

An enterprise-grade, high-aesthetic web application and presentation system for real-estate developer launches, client visits, showroom TV displays, and investor presentations.

Built strictly according to the PRD as a **reusable base plate** where project data, imagery, building specifications, roadmap, and contact details are completely decoupled from UI components.

---

## Key Features

1. **Reusable Base Plate Architecture**:
   - Single configuration file (`src/config/project.config.ts`) driving all numbers, copy, imagery, and contact info.
   - Clean asset directory structure in `public/assets/`.
2. **Hero Presentation**:
   - Cinematic full-screen architectural render with status badges, project identity, and primary CTAs.
3. **Project Overview & Metrics**:
   - 6 vital statistics cards (Acreage, Towers, Units, Amenities, Timeline, RERA Approval).
4. **Architectural Vision & Pillars**:
   - Editorial storytelling with architect quotes and 4 core lifestyle pillars (Biophilic Design, Smart Living, Clubhouse, Zero Carbon).
5. **Current Construction Transparency**:
   - Live progress bars for each tower and infrastructure item.
   - Drone aerial inspection gallery with date and altitude stamps.
6. **Current vs Future Visualization**:
   - Interactive Before/After comparison slider (drag to compare active civil work with the finished photorealistic 3D render).
7. **Building & Tower Showcase**:
   - Tabbed tower selector (The Solaria, The Celestia, The Pinnacle, Solarium Pavilion).
   - Floor plans with interactive modal lightbox and CAD layout request.
   - Engineering specs (ceiling height, marble, acoustic glazing, HVAC).
8. **Interactive Master Plan Viewer**:
   - Deep zoom (+ / -), reset, and pan canvas with fullscreen mode.
   - Clickable interactive hotspot pins with detail drawers and zone enquiries.
9. **Phased Development Roadmap**:
   - Chronological milestones (2026 ground work through 2030 handover) with civil deliverable checklists.
10. **The Finished Sanctuary (Expected Outcome)**:
    - Architectural showcase of completed amenities: Cantilevered Olympic Lap Pool, Biophilic Sky Gardens, Triple-Height Lobbies, and Night Illumination.
11. **Strategic Location & Connectivity**:
    - Interactive Leaflet map with CartoDB Dark Matter architectural styling (no API keys required).
    - Category filtering: Transport, Business, Schools, Hospitals, Shopping, Highways.
    - Travel time & distance matrix cards (Airport, Metro, Tech Park, IB Schools).
12. **Curated Architectural Gallery**:
    - Filterable by categories (All, Architecture, Interiors, Amenities, Construction, Master Plan).
    - Fullscreen lightbox with zoom, captions, and keyboard arrows (`Left`/`Right`/`Esc`).
13. **VIP Site Visit Booking System**:
    - Booking modal with time slot picker, guest count, and complimentary chauffeur airport pickup request.
    - Festive confetti celebration on confirmation.
14. **WhatsApp Lead Conversion System**:
    - Floating desktop button + bottom mobile conversion bar.
    - Contextual pre-filled WhatsApp enquiry generators (General, Site Visit, Building Pricing, Master Plan, Driving Directions).
15. **Dedicated Boardroom Presentation Mode**:
    - 10-slide fullscreen presentation designed for iPad, sales laptops, and showroom TVs.
    - Minimalist presentation chrome with keyboard navigation (`ArrowRight`, `ArrowLeft`, `Space`, `Esc`) and slide-overview drawer.

---

## Tech Stack

- **Framework**: React 19 + TypeScript + Vite
- **Styling**: Tailwind CSS v4 + Bespoke Luxury Architectural Design System (Obsidian, Slate, Champagne Gold, Glassmorphism)
- **Icons**: Lucide React
- **Maps**: Leaflet + CartoDB Dark Matter
- **Celebration / Interactions**: Canvas Confetti

---

## Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build production bundle
npm run build

# Preview production build locally
npm run preview
```

See [HOW_TO_CUSTOMIZE.md](./HOW_TO_CUSTOMIZE.md) for instructions on adapting this website for any real-estate development.
