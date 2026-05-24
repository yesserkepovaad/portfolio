# PRD: History Graduate Student Portfolio Website

## Overview

A single-page personal portfolio website for a history graduate student, designed to attract employers and corporate companies by presenting academic expertise as transferable professional value.

---

## Goals

- Present the owner as a credible, hire-ready professional with a history background
- Communicate the bridge between academic skills and corporate utility
- Provide a fast, frictionless way for employers to assess fit and make contact
- Work on all devices (desktop, tablet, mobile)

---

## Target Audience

| Audience | What They Need to See |
|---|---|
| Corporate HR / Recruiters | Clear skills, clean layout, contact CTA |
| Research & Consulting firms | Publications, analytical expertise |
| Think tanks / NGOs | Academic interests, rigor, writing ability |
| University Master's program recruiters | Academic interests, writing samples, research focus, GPA/credentials |
| University PhD program recruiters | Publications, research agenda, theoretical depth, supervisor fit signals |

---

## Realization Approach

**Recommended stack:** Pure HTML5 + CSS3 + vanilla JavaScript

**Why:**
- No build toolchain or framework dependency
- Loads instantly — one `.html` file + one `.css` file
- Easy to host for free (GitHub Pages, Netlify, Vercel)
- Easy to maintain without a developer

**Alternative:** If you want a CMS or easy future editing — use Notion + Super.so, or a Hugo/Jekyll static site generator.

---

## Pages & Sections

The site is a single scrollable page with a fixed navigation bar linking to each section via anchor links.

---

### Section 1 — Greeting & Brief Introduction

**Purpose:** First impression. Establish identity and purpose within 5 seconds.

**Content:**
- Full name (large heading)
- Title: e.g. *"History Graduate Student | Researcher | Analyst"*
- 2–3 sentence personal statement positioning history skills as professional assets
- Two CTA buttons: **"View My Work"** (scrolls to Publications) and **"Contact Me"** (scrolls to Contacts)
- Optional: professional headshot photo

**Design notes:**
- Full-viewport-height hero block
- High contrast, professional color palette (navy, white, gold accent — or similar)
- Subtle animated text or fade-in on load to add polish

---

### Section 2 — Academic Interests

**Purpose:** Show depth of expertise and intellectual focus areas.

**Content:**
- Section heading: *"Academic Interests"* or *"Research Focus"*
- 3–5 areas of historical specialization (e.g. Modern European History, Colonial Studies, Digital Humanities)
- Each interest as a card or tile with:
  - Icon or small illustration
  - Title of the interest
  - 1–2 sentence description of why it matters professionally
- Dedicated subsection or highlighted badge: **Minor in Spanish & Hispanic Studies**
  - Brief note on what the minor covers (language proficiency, Latin American / Iberian history and culture, literary and cultural analysis)
  - Framed as a professional asset: cross-cultural competency, Spanish-language source access, regional expertise

**Design notes:**
- Card grid layout (3 columns on desktop, 1 on mobile)
- Minor displayed as a distinct visual element (e.g. a highlighted banner or accent card) so it stands out from the main interest cards
- Connects abstract academic work to practical relevance (e.g. "expertise in archival research → due diligence, investigative research"; "Hispanic Studies minor → ability to work with Spanish-language markets and sources")

---

### Section 3 — Skills

**Purpose:** Convince corporate employers that a historian has concrete, usable skills.

**Content:**

**Hard Skills** (technical, discipline-specific):
- Archival & primary source research
- Academic writing & long-form reporting
- Qualitative data analysis
- Literature review & synthesis
- Citation management (Zotero, EndNote)
- Foreign language proficiency (list languages + level)
- Digital humanities tools (if applicable)

**Soft Skills** (transferable):
- Critical thinking & complex problem analysis
- Attention to detail
- Written and verbal communication
- Project management (dissertation / thesis experience)
- Working with ambiguity and incomplete information
- Cross-cultural awareness

**Design notes:**
- Split into two visually distinct columns: Hard / Soft
- Use tag badges or progress-style indicators (avoid generic percentage bars)
- Each skill optionally expands or has a tooltip with a brief example

---

### Section 4 — Publications

**Purpose:** Provide concrete evidence of intellectual output and writing quality, with direct access to the full papers.

**Content:**
- Section heading: *"Selected Publications"* or *"Research Output"*
- List of 3–8 publications, each showing:
  - Title
  - Publication venue (journal name, conference, university press)
  - Year
  - One-line description of the contribution or argument
  - **"Download PDF"** button linking directly to the paper's PDF file
- Optional: tag chips per entry (e.g. `Modern History`, `Archival Research`, `Peer-reviewed`)

**PDF handling:**
- Each paper is stored as a local PDF file inside the `assets/papers/` folder (e.g. `assets/papers/paper-title-2023.pdf`)
- The download link uses the HTML `download` attribute so clicking triggers a file save rather than opening a new tab
- File naming convention: `lastname-short-title-year.pdf` (e.g. `ivanova-colonial-memory-2024.pdf`)
- No external hosting dependency — all files live in the same repository as the site

**Design notes:**
- Vertical list or card layout
- Clear visual hierarchy: title bold, venue muted, year as a badge
- Download button styled as a distinct secondary action (e.g. outlined button with a download icon)
- "Download CV" button at the bottom of this section

---

### Section 5 — Contacts

**Purpose:** Remove all friction for an interested employer to reach out.

**Content:**
- Email address (with mailto link)
- LinkedIn profile link
- ResearchGate or Academia.edu profile (optional)
- ORCID (optional, signals academic credibility)
- Short message: *"Open to research, consulting, and analytical roles. Feel free to reach out."*
- Simple contact form (Name, Email, Message) — optional but increases conversion

**Design notes:**
- Centered layout, minimal
- Social icons (not just text links)
- Footer below with copyright line

---

## Navigation

- Sticky top navigation bar with links: Introduction · Interests · Skills · Publications · Contact
- Smooth scroll behavior between sections
- Active section highlighted in the nav as the user scrolls
- Hamburger menu on mobile

---

## Non-Functional Requirements

| Requirement | Target |
|---|---|
| Page load time | < 2 seconds |
| Mobile responsiveness | Works on all screen sizes ≥ 320px |
| Accessibility | WCAG 2.1 AA (alt text, contrast ratios, keyboard nav) |
| Browser support | Chrome, Firefox, Safari, Edge (last 2 versions) |
| Hosting | Static hosting (GitHub Pages / Netlify) — free tier |
| Maintainability | All content editable in plain HTML without a developer |

---

## Design Style

**Three-word direction: Corporate · Friendly · Minimalistic**

| Principle | Implementation |
|---|---|
| Corporate | Navy primary color, structured grid layout, clean typography, no decorative clutter |
| Friendly | Warm white backgrounds, soft card shadows, rounded corners, approachable serif headings |
| Minimalistic | Generous whitespace, max-width container (900px), muted secondary text, no unnecessary elements |

**Color palette:**
- Primary: `#1B2B4B` (deep navy) — headings, nav logo, year badges
- Accent: `#2563EB` (professional blue) — links, active states, CTA buttons
- Accent light: `#EFF6FF` — tag backgrounds, hover states
- Gold: `#B7973A` / `#FEF9EC` — minor banner highlight
- Background: `#FFFFFF` / `#F9FAFB` (alternating sections)
- Text muted: `#6B7280` — secondary information

**Typography:**
- Headings: *Playfair Display* (serif — scholarly, authoritative)
- Body: *Inter* (sans-serif — clean, modern, corporate)

**Deliverable format:** Single `index.html` file with all CSS and JS embedded — no external dependencies except Google Fonts CDN. Fully responsive down to 320px screen width.

---

## Design Principles

1. **Professional over flashy** — this targets corporate employers and academic committees, not creative agencies
2. **Content-first** — skills and publications are the product; design serves them
3. **Credibility signals** — publications, institutions, language skills build trust
4. **Clear value translation** — every academic strength should have a corporate framing
5. **Single file** — all CSS and JS embedded in `index.html`; PDFs stored in `assets/papers/`

---

## Deliverables

- [ ] `index.html` — full single-page site
- [ ] `style.css` — all styles, responsive breakpoints
- [ ] `script.js` — scroll behavior, nav highlighting, optional form handling
- [ ] `assets/` — headshot photo, favicon, CV PDF
- [ ] `assets/papers/` — PDF files for each listed publication

---

## Out of Scope

- CMS or database backend
- Blog or multi-page expansion
- Payment or e-commerce
- User accounts or authentication

---

## Success Metrics

- Page renders correctly on desktop and mobile
- All 5 sections are present and populated with real content
- CV download works
- Contact method (email or form) is functional
- Page scores ≥ 90 on Google Lighthouse (Performance, Accessibility, SEO)
