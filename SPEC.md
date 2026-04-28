# Portfolio Website Specification

## Project Overview
- **Project Name**: Portfolite - Modern Portfolio Website
- **Type**: Single-page portfolio website
- **Core Functionality**: A clean, modern portfolio showcasing skills, projects, and contact information
- **Target Users**: Potential employers, clients, and collaborators

## UI/UX Specification

### Layout Structure
- **Navigation**: Fixed/sticky navbar with smooth scroll links
- **Sections**: Home, About, Projects, Services, Contact
- **Responsive Breakpoints**:
  - Mobile: < 768px
  - Tablet: 768px - 1024px
  - Desktop: > 1024px

### Visual Design

#### Color Palette
- **Background**: `#0a0a0a` (deep black)
- **Surface**: `#141414` (card backgrounds)
- **Primary Accent**: `#e8c547` (warm gold)
- **Secondary**: `#f5f5f5` (off-white text)
- **Muted**: `#6b6b6b` (secondary text)
- **Gradient**: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%)

#### Typography
- **Font Family**: 'Sora' (headings), 'DM Sans' (body)
- **Headings**: 
  - H1: 64px (desktop), 40px (mobile)
  - H2: 48px (desktop), 32px (mobile)
  - H3: 24px
- **Body**: 16px, line-height 1.7

#### Spacing System
- Section padding: 100px vertical (desktop), 60px (mobile)
- Container max-width: 1200px
- Card padding: 24px
- Gap between elements: 16px / 24px / 32px

#### Visual Effects
- Box shadows: `0 10px 40px rgba(0,0,0,0.3)`
- Border radius: 12px (cards), 8px (buttons), 50% (images)
- Backdrop blur on navbar: `blur(10px)`
- Gradient overlays on project cards

### Components

#### Navigation
- Logo on left (text-based)
- Links on right: Home, About, Projects, Services, Contact
- Mobile: hamburger menu with slide-in drawer
- Background: semi-transparent with blur

#### Hero Section
- Full viewport height (100vh)
- Animated gradient background with subtle movement
- Centered content with staggered fade-in animation
- Name in large heading
- Title/role below
- Brief tagline
- CTA buttons: "View Projects" (primary), "Contact Me" (outline)

#### About Section
- Two-column layout (image left, content right on desktop)
- Profile image with decorative border/glow
- Bio text
- Skills grid with icon badges

#### Projects Section
- 3-column grid (desktop), 2-column (tablet), 1-column (mobile)
- Project cards with:
  - Image thumbnail (16:10 aspect ratio)
  - Title
  - Short description
  - Tech stack tags
  - Links (Live demo, GitHub)
- Hover: scale up, reveal overlay with links

#### Services Section
- 3 cards in row
- Each card: Icon, title, description, list of features
- Services: Web Development, UI/UX Design, Consulting

#### Contact Section
- Two columns: Form (left), Contact info (right)
- Form fields: Name, Email, Message
- Submit button with loading state
- Success/error toast notifications

#### Footer
- Dark background
- Social icons: GitHub, LinkedIn, Twitter
- Copyright text
- Back to top button

### Animations
- Page load: Staggered fade-in from bottom
- Scroll: Sections fade in when entering viewport
- Hover: Scale, color transitions (0.3s ease)
- Navbar: Background opacity changes on scroll
- Smooth scroll behavior for anchor links

## Functionality Specification

### Core Features
1. **Smooth Scroll Navigation**: Click nav links to smooth scroll to sections
2. **Mobile Menu**: Hamburger toggle for mobile navigation
3. **Form Validation**: Validate name (min 2 chars), email (valid format), message (min 10 chars)
4. **Email Integration**: Use FormSubmit.co for form submission (no backend needed)
5. **Loading Animation**: Preloader on page load
6. **Scroll Animations**: Intersection Observer for reveal animations

### User Interactions
- Click nav link → smooth scroll to section
- Click hamburger → toggle mobile menu
- Fill form → validate → submit → show feedback
- Hover project card → reveal overlay with links
- Click social icon → open in new tab

### Form Handling
- Client-side validation before submission
- Send to FormSubmit.co API
- Show success message: "Thank you! Your message has been sent."
- Show error message on failure

## Acceptance Criteria
- [ ] Navigation is sticky and highlights active section
- [ ] All sections render correctly on mobile/tablet/desktop
- [ ] Form validates inputs and shows appropriate errors
- [ ] Form submits successfully via FormSubmit
- [ ] Smooth scroll works for all nav links
- [ ] Animations play smoothly without jank
- [ ] Images and fonts load correctly
- [ ] No console errors on page load

## File Structure
```
/mywebsite
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
│   └── (placeholder images)
└── SPEC.md
```