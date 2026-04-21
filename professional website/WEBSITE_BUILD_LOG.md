# WEBSITE BUILD LOG
**Site:** Yassine Hariri — Personal Career Website  
**Build Date:** 2026-04-20  
**Builder:** Claude (Cowork Mode)  
**Target:** GitHub Pages — pure HTML/CSS/JS, no build step

---

## Files Created

| File | Description |
|------|-------------|
| `index.html` | Full single-page career site — all sections |
| `MEMORY.md` | Project memory / session state |
| `WEBSITE_BUILD_LOG.md` | This file |

---

## Source of Content

> ⚠️ `Profile.pdf` was **not found** in the workspace or uploads directory at build time.
> All content was sourced from the user's session profile context (user_preferences).
> **Action required:** Share Profile.pdf and re-run content population for Experience, Publications, and Talks.

| Section | Content Source | Completeness |
|---------|---------------|--------------|
| Hero | Session profile context | ✅ Complete (pending URLs) |
| About | Session profile context | ✅ Complete |
| Expertise | Session profile context | ✅ Complete — all 8 domains |
| Experience | Session profile context | ⚠️ Current role only — past roles need Profile.pdf |
| Projects | Session profile context | ✅ 4 projects extracted |
| Publications | Session profile context (domain names only) | ❌ Needs Profile.pdf |
| Talks | Session profile context | ⚠️ 1 series — full list needs Profile.pdf |
| Contact | Email from session context | ⚠️ Pending: LinkedIn URL, GitHub, YouTube URL |

---

## Sections Built

### 1. Hero
- Full-viewport dark hero with animated dot-grid background
- Gold accent glow (radial gradient, top-right)
- Circuit board SVG art (custom-drawn, gold on dark)
- Staggered entrance animations (CSS keyframes, 7 elements)
- Name, role, org, tagline, 3 CTA buttons
- 4 stat counters: 17+ years, PhD, 5 editions, 3 languages
- Scroll indicator with animated drop line

### 2. About
- 2-column grid: bio text + portrait placeholder
- 3-paragraph bio extracted from profile context
- Pill tags: degree, institution, location, languages, domains
- Portrait box with `YH` monogram (placeholder for photo)
- `<!-- TODO: add photo -->` comment included

### 3. Expertise
- 8 domain cards in auto-fill CSS grid
- Left-border accent reveal on hover (transform: scaleY)
- Lift + shadow on hover
- Skill chips per domain (monospace, subtle)
- Domains: ASIC, FPGA/SoC, Edge AI, Embedded, IoT, SDR, Research, Leadership

### 4. Experience
- Vertical timeline with connecting line
- Gold dot markers
- Current role fully populated (5 bullet points)
- HTML comment template included for adding past roles

### 5. Projects
- 4-card grid with gold bottom-border reveal on hover
- Cards: FABrIC Program, Edge AI Surveillance, Accelerating AI Workshop, YouTube Channel
- Tech tags per card
- Lift + deep shadow on hover
- HTML comment for adding more projects

### 6. Publications
- Numbered list structure (pub-item, pub-n, pub-title, pub-meta)
- Placeholder entry with known research domains listed
- PhD institution noted (ÉTS)
- HTML comment with full entry format template

### 7. Talks & Workshops
- Card grid
- Accelerating AI series (2020–2025) fully entered
- HTML comment template for adding more talks

### 8. Contact
- 2-column: contact links + mailto form
- Links: email, LinkedIn (placeholder URL), GitHub (TODO), YouTube (TODO)
- Form: name, subject, message → `mailto:` action
- Subtle gold top-border line separator

### Navigation
- Fixed, transparent → frosted dark on scroll (backdrop-filter: blur)
- Scroll-based active link highlight (IntersectionObserver)
- Mobile hamburger menu with CSS animation

### Footer
- Minimal: copyright + back-to-top

---

## Design System

| Token | Value |
|-------|-------|
| `--bg` | `#0D0D0D` |
| `--bg-2` | `#111111` |
| `--bg-3` | `#161616` |
| `--accent` | `#FFB800` (Gold) |
| `--text` | `#EFEFEF` |
| `--text-2` | `#9A9A9A` |
| `--font-h` | Syne (Google Fonts) |
| `--font-m` | Space Mono (Google Fonts) |
| `--font-b` | Inter (Google Fonts) |

**Animations:**
- Page load: `up-in` keyframe — staggered 7 elements
- Scroll reveal: `IntersectionObserver` + `.rv` / `.on` class toggle, sibling stagger capped at 400ms
- Hover: `translateY(-5px)` + border-color transition on cards
- Nav: smooth opacity + backdrop-filter transition
- Scroll cue: `scroll-line` keyframe loop

---

## TODOs — Content Gaps (requires Profile.pdf or user input)

- [ ] **Experience**: Add all past roles (dates, org, achievements)
- [ ] **Publications**: Populate full list from PDF
- [ ] **Talks**: Add all conference appearances and keynotes
- [ ] **LinkedIn URL**: Confirm correct handle
- [ ] **GitHub URL**: Add username and link
- [ ] **YouTube URL**: Add channel link (href in 2 places: hero CTA + contact)
- [ ] **Photo**: Save as `images/yassine.jpg` — swap `portrait-monogram` div (comment in HTML)
- [ ] **CV PDF**: Save as `cv/yassine-hariri-cv.pdf` — update hero `[Download CV]` button href
- [ ] **PhD thesis title + year**: Add to publications section
- [ ] **Experience start year**: Add to current role timeline date

---

## GitHub Pages Compatibility

- No server-side code
- No build step required
- All fonts loaded from Google Fonts CDN
- All JS is vanilla (no dependencies)
- Pure `mailto:` form (no backend)
- Push-ready: `git add . && git commit -m "Rebuild career site" && git push`

---

## File Size (approx)
- `index.html`: ~700 lines, ~38KB unminified
- Loads: Google Fonts (3 families) + no other external dependencies
