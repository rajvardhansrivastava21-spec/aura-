# How to Customize This Real Estate Base Plate

This website is engineered as a **reusable real-estate presentation engine**. You can deploy it for any new residential tower, luxury villa enclave, commercial park, or mixed-use master development **without rewriting any code or redesigning components**.

All customizations are separated into two simple areas:
1. **Project Data & Copy**: Handled in a single file: `src/config/project.config.ts`
2. **Media & Imagery**: Handled in the `/public/assets/` directory (or external CDN / S3 URLs)

---

## 1. Quick Start: Rebranding for a New Project

Open `src/config/project.config.ts`:

### A. Update Project Identity & Hero
```typescript
projectIdentity: {
  name: "YOUR PROJECT NAME",
  tagline: "Your Project Subtitle / Property Type",
  shortLocation: "Sector, City",
  fullLocation: "Complete Address with Pincode",
  heroSubtitle: "A 2-sentence captivating description of your vision...",
  statusBadge: "Phase 1 Under Construction",
  launchBadge: "RERA APPROVED • PRE-LAUNCH PRIVILEGE",
  heroBackgroundRender: "/assets/hero/main-render.jpg", // or any high-res image URL
}
```

### B. Update Vital Statistics
Change the overview cards (e.g. Acreage, Number of Towers, Units, Amenities, Completion Target, RERA):
```typescript
overviewStats: [
  { label: "Master Land Parcel", value: "85", unit: "Acres", subtext: "60% Greenery", iconName: "Trees" },
  { label: "Towers", value: "6", unit: "Towers", subtext: "G+32 Floors", iconName: "Building2" },
  // ...
]
```

### C. Update Buildings & Floor Plans
In `buildings`:
- Add or remove towers (`Tower A`, `Tower B`, `Clubhouse`, `Villas`)
- Set construction progress (`progressPercentage: 75`)
- Add unit configurations (e.g. 2 BHK, 3 BHK, 4 BHK, Penthouses) with carpet area and floor plan image links
- Customize specifications (Ceiling height, Flooring marble, Acoustic glazing, HVAC, Home automation)

### D. Update Master Plan
In `masterPlan`:
- Place your master layout blueprint in `/public/assets/master-plan/master-layout.jpg`
- Add clickable hotspot pins with percentage coordinates `(x: 35, y: 45)` corresponding to your master plan image
- Add zone descriptions, specifications, and amenity tags

### E. Update Construction Transparency & Live Progress
In `currentDevelopment`:
- Set current percentages for each structure or civil engineering milestone
- Add date-stamped drone photos and site camera logs

### F. Update Before / After Transformation Slider
In `beforeAfter`:
- Set `currentImage` (actual raw site photo)
- Set `futureImage` (photorealistic 3D architectural render)

### G. Update Location, Map & Distances
In `location`:
- Set coordinates `{ lat: XX.XXXX, lng: YY.YYYY }`
- Add nearby landmarks (Airport, Railway/Metro, Top Schools, Hospitals, Tech Parks, Shopping Malls) with distance and drive times
- Leaflet map will automatically render dark architectural map tiles with glowing markers!

### H. Update WhatsApp & Contact Channels
In `contact`:
```typescript
contact: {
  whatsappNumber: "15550192834", // International format digits only (no '+', dashes, or spaces)
  whatsappDisplay: "+1 (555) 019-2834",
  phone: "+18002872872",
  phoneDisplay: "+1 (800) AURA-LIVING",
  email: "sales@yourproject.com",
  salesOfficeAddress: "Project Experience Centre, Gate 1...",
  reraNumber: "PRM/KA/RERA/...",
}
```

---

## 2. Media Asset Directory Structure

Place all new media assets inside `public/assets/`:
```text
public/assets/
├── logo/               -> Vector SVG or PNG logos
├── hero/               -> Main hero renders or video loops
├── buildings/          -> High-resolution building renders & photos
├── current-development/-> Periodic drone photos and site logs
├── future-renders/     -> Photorealistic 3D outcome renders
├── master-plan/        -> High-res master zoning blueprints
├── floor-plans/        -> CAD / 3D unit floor plan drawings
├── amenities/          -> Clubhouse, lap pool, and sports arena photos
└── gallery/            -> High-res architectural photo archive
```

---

## 3. Running & Deploying

- **Local Preview**: `npm run dev` (Runs locally on `http://localhost:5173`)
- **Showroom Pitch / Offline Meetings**: Run `npm run preview` or open in full-screen on any laptop or showroom TV
- **Production Build**: `npm run build` generates a standalone static bundle in `/dist` that can be deployed to Vercel, Netlify, Cloudflare Pages, AWS S3, or any web server.
