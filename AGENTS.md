# AGENTS.md - Wedding Invitation Website

## Project Overview
Static wedding invitation website for Leonardo & Jessica with personalized greetings, countdown timer, photo gallery, and message system.

## Build/Development Commands
- **Live Server**: Use any static file server (e.g., `python -m http.server 8000` or `npx live-server`)
- **No build process required** - Pure HTML/CSS/JS static site
- **Cache busting**: Add `?v=TIMESTAMP` to CSS/JS URLs when updating

## Code Style Guidelines

### HTML Structure
- Semantic section-based layout (section-0 through section-10)
- Mobile-first responsive design with max-width 1080px
- Chinese language support (`lang="zh-CN"`)

### CSS Conventions  
- BEM-inspired naming: `.section-N`, `.section-N-content`, `.section-N-background`
- Animation classes: `.animate-on-scroll`, `.delay-1` through `.delay-5`
- iOS-specific fixes using `@supports (-webkit-touch-callout: none)`
- Font families: "Times New Roman" (body), "Monsieur La Doulaise" (headings)

### JavaScript Patterns
- Vanilla JS only - no frameworks
- API endpoints: `https://dashboard.sayjesstoleo.site/api/`
- Intersection Observer for scroll animations
- Media preloading for performance
- Error handling for autoplay restrictions

### Asset Management
- Images hosted on: `https://titu.b-cdn.net/`
- Cache busting with version query parameters
- Preload critical assets (images, videos, audio)

### Key Features Implementation
- **Personalized Greeting**: URL param `?name=NAME` (removed API validation)
- **Countdown Timer**: Target date `2025-11-22T18:00:00`
- **Message System**: POST to `/api/comments`, GET from `/api/comments`
- **Music Toggle**: Background audio with user interaction requirement
- **Invitation Validation**: Simple name parameter check (no API call)
- **Couple Info**: Boby Chandra & Stefany Dwi Christiani
- **Wedding Events**: Pemberkatan Nikah (10:00 WIB) & Resepsi (18:00 WIB) on 22/11/25
- **Bank Accounts**: BCA accounts for digital gifts
- **Landscape Photos**: 7 landscape photos in "Our Moments" section (bobby20-26_land)

### Performance Considerations
- Image preloading in DOMContentLoaded
- Video autoplay with fallback handling
- Mobile-optimized background attachments
- Scroll performance with Intersection Observer