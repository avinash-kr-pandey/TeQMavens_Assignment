# NextCar — Interactive Automotive Experience

A responsive, animation-focused automotive interface built from the provided
design reference as a frontend development assignment. The project recreates
the supplied UI in Next.js with reusable components, responsive layouts,
light/dark themes, and polished motion.

## Submission

- **Repository:** https://github.com/avinash-kr-pandey/TeQMavens_Assignment
- **Live demo:** https://te-q-mavens-assignment-advx.vercel.app/
- **Figma/design source:** Add provided Figma URL
- **Demo video/screenshots:** Add video or screenshot URL

> Replace the placeholders above before submitting the assignment.

## Assignment Coverage

- Next.js and React implementation
- TypeScript throughout the application
- Tailwind CSS configuration with reusable theme tokens
- Custom responsive CSS for the cinematic layouts and visual effects
- Desktop, tablet, portrait-phone, and landscape-phone support
- Functional light and dark theme toggle
- Reusable, independently maintained UI components
- Smooth page, timeline, carousel, vehicle, and reveal animations
- Accessible buttons, labels, and reduced-motion support

## Features

- Interactive vehicle customization dashboard
- Circular vehicle presentation with performance statistics
- Responsive left and right navigation controls
- Animated pricing cards and a mobile horizontal pricing carousel
- Functional booking modal
- Animated customer-support reveal
- Multi-stage vehicle delivery timeline
- Delivery-van loading and return sequence
- Animated certification presentation
- Persistent layered automotive background
- Lap-style progress footer with responsive wave points
- Theme persistence using `next-themes`

## Tech Stack

| Technology | Usage |
| --- | --- |
| Next.js 15 | Application framework and App Router |
| React 19 | Component-based UI |
| TypeScript | Type-safe development |
| Tailwind CSS 3 | Utility framework, design tokens, and theme configuration |
| Custom CSS | Complex responsive composition, gradients, masks, and effects |
| Framer Motion | Page transitions, spring animations, and sequences |
| next-themes | Light/dark theme management |
| Lucide React | Accessible interface icons |
| clsx | Conditional class names |
| tailwind-merge | Safe utility-class composition |

## Getting Started

### Prerequisites

- Node.js 20 or later
- npm 10 or later

### Installation

```bash
git clone <repository-url>
cd teq-mavens
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Production build

```bash
npm run build
npm start
```

## Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Starts the Turbopack development server |
| `npm run build` | Creates an optimized production build |
| `npm start` | Runs the production server |
| `npm run lint` | Runs the configured Next.js lint command |

## Project Structure

```text
app/
├── globals.css             # Theme tokens, responsive rules, and visual effects
├── layout.tsx              # Root layout and theme provider
└── page.tsx                # Application entry point

components/
├── BookingModal.tsx        # Pricing enquiry/booking interaction
├── CertificateStage.tsx    # Certification reveal sequence
├── Experience.tsx          # Main view controller and shared interface
├── Heading.tsx             # Primary page heading
├── HomeStage.tsx           # Vehicle performance presentation
├── LapTrack.tsx            # Responsive progress-wave footer
├── Logo.tsx                # Brand mark
├── Pricing.tsx             # Desktop pricing grid and mobile carousel
├── SideNav.tsx             # Primary navigation
├── ThemeProvider.tsx       # next-themes configuration
├── ThemeToggle.tsx         # Light/dark controls
├── TimelineStage.tsx       # Delivery timeline and van animation
└── VehicleStage.tsx        # Vehicle customization dashboard

lib/
└── utils.ts                # Shared class-name utility

public/
└── *.png                   # Vehicle and interface image assets
```

## Architecture and Code Decisions

### Component structure

Large interface areas are separated into focused components. `Experience`
controls the active view, while each screen owns its content and animation
sequence. This keeps the code easier to extend without coupling individual
features.

### Responsive implementation

The desktop interface preserves the wide cinematic composition from the design.
Smaller breakpoints adjust image sizes, navigation placement, typography,
pricing behavior, and footer geometry. Pricing uses a horizontal touch-enabled
carousel on phones instead of stacking oversized cards.

### Theme handling

Theme state is managed with `next-themes` using class-based dark mode. Shared CSS
variables control the foreground, background, panels, borders, rings, and
lighting in both themes.

### Animation

Framer Motion is used for coordinated view transitions and interactive
sequences. CSS handles stable atmospheric effects and responsive layout. This
separation avoids unnecessary re-renders for static visual layers.

## Assumptions

- The supplied design is treated as the source of truth for layout, color,
  hierarchy, and visual direction.
- Vehicle and illustration assets are supplied raster images and are displayed
  without modifying their source artwork.
- Pricing and vehicle information are demonstration data.
- Booking currently uses a client-side interaction because no backend API was
  included in the assignment.
- Navigation is implemented as a single interactive experience rather than
  separate URL routes to preserve the designed transitions.
- Production API credentials and private environment variables are not required.

## Accessibility

- Semantic buttons and navigation elements
- Descriptive `aria-label` attributes on icon-only controls
- Alternative text for meaningful images
- Keyboard-accessible interactions
- Reduced-motion handling through `prefers-reduced-motion`
- Theme controls with visible active states

## Browser Support

The interface targets the latest stable versions of:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

## Known Limitations

- Booking submissions are not sent to a backend.
- Pricing and vehicle data are currently stored in the frontend.
- Raster assets can be migrated to the Next.js Image component or an image CDN
  for additional production optimization.
- Automated visual-regression and end-to-end tests are not included yet.

## Potential Improvements

- Connect the booking flow to a REST or GraphQL API
- Add authentication and saved vehicle configurations
- Move content and pricing into a CMS or database
- Add unit, integration, and visual-regression tests
- Optimize all raster assets through an image pipeline
- Add analytics and error monitoring

## Evaluation Notes

The implementation focuses on the assignment’s primary evaluation areas:

1. Fidelity to the supplied design
2. Responsive behavior across screen sizes
3. Functional light and dark themes
4. Reusable component structure
5. Clean TypeScript code
6. Smooth, purposeful animation

---

Built as a React/Next.js frontend assignment.
