# AGENTS.md - Wedding Invitation Website

## Build/Development Commands
- **Live Server**: `python -m http.server 8000` or `npx live-server`
- **No build/lint/test** - Pure static HTML/CSS/JS site
- **Cache busting**: Add `?v=TIMESTAMP` to CSS/JS URLs

## Code Style Guidelines

### HTML
- Semantic sections: `section-0` through `section-10`
- Mobile-first, max-width 1080px, lang="zh-CN"
- Inline JavaScript only, no external JS files

### CSS  
- BEM naming: `.section-N`, `.section-N-content`, `.section-N-background`
- Animation classes: `.animate-on-scroll`, `.delay-1` to `.delay-5`
- iOS fixes: `@supports (-webkit-touch-callout: none)`
- Fonts: "Times New Roman" (body), "Monsieur La Doulaise" (headings)

### JavaScript
- Vanilla JS only, embedded in HTML
- APIs: `https://nikayu-bobbystefany-qroiau-84bf02-160-187-210-229.traefik.me/api/` (attendee validation & comments)
- Intersection Observer for animations
- Media preloading, autoplay error handling

### Assets
- Images: `https://titu.b-cdn.net/`
- Couple: Boby Chandra & Stefany Dwi Christiani
- Wedding: 22/11/25, 10:00 WIB (ceremony), 18:00 WIB (reception)
- Features: Countdown to 2025-11-22T18:00:00, message system, music toggle
- Attendee validation: URL param `?id=ATTENDEE_ID` with API validation