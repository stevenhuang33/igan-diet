# IgA Nephropathy Stage 3 CKD Dietary Plan - Specification

## Project Overview
- **Project Name**: IgA Nephropathy Stage 3 CKD Dietary Plan
- **Type**: Single-page educational web application
- **Core Functionality**: Comprehensive dietary guide for patients with Stage 3 IgA Nephropathy/CKD
- **Target Users**: Patients with IgAN Stage 3, caregivers, healthcare educators

---

## UI/UX Specification

### Layout Structure

**Header**
- Fixed navigation bar with logo/title
- Sticky on scroll
- Mobile: Hamburger menu

**Hero Section**
- Full-width banner with kidney health illustration
- Main title with subtitle
- Quick stats cards (daily targets)

**Main Content Sections**
1. Foods to Eat (Good)
2. Foods to Limit/Avoid (Bad)
3. Daily Nutritional Targets
4. Sample Meal Plan
5. Portion Size Guide
6. Tips for Eating Out
7. Kidney-Friendly Recipes

**Footer**
- Medical disclaimer
- Quick links
- Copyright

### Responsive Breakpoints
- Mobile: < 768px (single column)
- Tablet: 768px - 1024px (two columns)
- Desktop: > 1024px (full layout)

### Visual Design

**Color Palette**
- Primary: `#1a5f4a` (Deep kidney green)
- Primary Light: `#2d8a6e` (Sage green)
- Secondary: `#f8f5f0` (Warm off-white)
- Accent Gold: `#c9a227` (Warm gold)
- Good/Green: `#22c55e` (Eat)
- Moderate/Yellow: `#f59e0b` (Limit)
- Avoid/Red: `#ef4444` (Avoid)
- Text Dark: `#1f2937`
- Text Light: `#6b7280`
- Background: `#fafaf9`
- Card Background: `#ffffff`

**Typography**
- Headings: "Playfair Display", serif (elegant, trustworthy)
- Body: "Source Sans 3", sans-serif (clean, readable)
- Font Sizes:
  - H1: 3rem (mobile: 2rem)
  - H2: 2rem (mobile: 1.5rem)
  - H3: 1.5rem (mobile: 1.25rem)
  - Body: 1rem
  - Small: 0.875rem

**Spacing System**
- Section padding: 80px vertical (mobile: 48px)
- Card padding: 24px
- Element gap: 16px
- Border radius: 12px (cards), 8px (buttons)

**Visual Effects**
- Card shadows: `0 4px 20px rgba(0,0,0,0.08)`
- Hover lift: translateY(-4px)
- Smooth transitions: 0.3s ease
- Gradient accents on headers
- Subtle background patterns

### Components

**Category Accordion**
- Expand/collapse with smooth animation
- Icon rotation on expand
- Color-coded left border

**Food Cards**
- Color badge (green/yellow/red)
- Food name and portion
- Nutritional info mini-table
- Hover state with shadow

**Search Bar**
- Floating search with icon
- Real-time filtering
- Clear button
- "No results" state

**Nutrient Badges**
- Small pill-shaped badges
- Color-coded by nutrient type
- Tooltip for details

**Meal Plan Cards**
- Time of day indicator
- Meal name
- Food items list
- Nutritional summary

**Print Button**
- Fixed position
- Print-specific styles

**Mobile Navigation**
- Slide-in menu
- Smooth animation
- Close on outside click

---

## Functionality Specification

### Core Features

1. **Search & Filter**
   - Search by food name
   - Filter by category (Good/Limit/Avoid)
   - Filter by nutrient (low-potassium, low-phosphorus, etc.)
   - Real-time results

2. **Category Expand/Collapse**
   - All categories expandable
   - Smooth accordion animation
   - "Expand All" / "Collapse All" buttons
   - Remember state in session

3. **Print Functionality**
   - Print-friendly CSS
   - Hide interactive elements
   - Optimized layout for A4
   - Include disclaimer

4. **Mobile Responsiveness**
   - Touch-friendly interactions
   - Swipe to close menus
   - Optimized tap targets (min 44px)

5. **Nutritional Information Display**
   - Per-serving values
   - Traffic light coding
   - Serving size conversions

### Data Structure

**Foods Database**
```
{
  name: string,
  category: "good" | "moderate" | "avoid",
  type: "protein" | "fruit" | "vegetable" | "grain" | "fat" | "fluid",
  portion: string,
  nutrition: {
    protein: string,
    potassium: string,
    phosphorus: string,
    sodium: string
  },
  notes: string,
  recipe?: string
}
```

### User Interactions
- Click to expand categories
- Type to search foods
- Click badges to filter
- Hover for additional info
- Click print button for printable view
- Mobile: tap to expand, swipe menu

### Edge Cases
- Empty search results: Show helpful message
- Print mode: Hide interactive elements
- Slow connection: Graceful loading states
- Small screens: Stack all content vertically

---

## Acceptance Criteria

### Visual Checkpoints
- [ ] Hero section displays with gradient overlay
- [ ] All color coding matches spec (green/yellow/red)
- [ ] Typography hierarchy is clear
- [ ] Cards have proper shadows and hover states
- [ ] Mobile menu works smoothly
- [ ] Print preview shows clean layout

### Functional Checkpoints
- [ ] Search filters foods in real-time
- [ ] Categories expand/collapse with animation
- [ ] Filter badges work correctly
- [ ] Print button triggers print dialog
- [ ] All external links work
- [ ] Mobile responsive at all breakpoints

### Content Checkpoints
- [ ] All 5 main sections present
- [ ] Foods categorized correctly
- [ ] Nutritional targets listed
- [ ] Meal plan has 4+ meals
- [ ] Portion guide with visual refs
- [ ] Disclaimer visible in footer
