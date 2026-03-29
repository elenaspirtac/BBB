# BBB Presentation — Session Journal
## AEC Hackathon Copenhagen 2026 — 29 March 2026

---

## PROJECT OVERVIEW
We built a retro 8-bit Minecraft-themed pitch presentation for the AEC Hackathon Copenhagen 2026. The presentation is for **Team BBB** (6 members) pitching an open-source, AI-enabled, community-driven BIM platform.

## REPOS
- **Presentation (standalone):** https://github.com/elenaspirtac/BBB
- **Live link:** https://elenaspirtac.github.io/BBB/
- **Main project repo:** https://github.com/elenaspirtac/vibe-code-features
- **Main project local:** C:\Users\KE919\Downloads\authoring-main\authoring-main

## TEAM BBB — 6 Members
1. Ivan (🕵️) — top-left
2. Dima (🧙‍♂️) — top-right
3. Elena (🧝‍♀️) — mid-left
4. Marius (🐉) — mid-right
5. Kim (🦊) — bottom-right
6. Christian (🛡️) — center-left

Members float with bobbing animations on the cover slide.

---

## PRESENTATION STRUCTURE (6 slides)

### Slide 1 — COVER
- Team BBB in big pink text
- Date: 29 March 2026 — Copenhagen
- "> What if we could reinvent BIM?"
- 🏗️🤖⚡ icons
- Chat terminal (SESSION START / Loading BIM world / AI Tool Generator: ONLINE)
- 6 floating team members scattered around edges
- 5 vendor icons at bottom (Revit, Tekla, Solibri, ArchiCAD, Bentley) with laser targeting/shooting animation
- Content pushed to lower portion with `justify-content:flex-end;padding-bottom:18vh`

### Slide 2 — THE DREAM (1975)
- ★ THE DREAM — 1975 ★ badge in yellow
- Charles Eastman quote: "What if a building was a database before it was a building?"
- 4 blocks (same style as slide 3): One Model, Smart Objects, Changes Propagate, Model Lives Forever
- Patrick MacLeamy quote (CEO HOK Architects): "BIM is not about technology. It's about integrating knowledge..."
- XP bar: "The Dream — 100% complete... on paper"

### Slide 3 — 50 YEARS LATER (What Failed)
- "50 YEARS LATER." in big red text
- "Where it failed" heading
- Causal chain with red arrows: 💰 The "I" Died → 🔒 Vendors Fragmented the Model → ⚰️ Model Dies at Handover
- ⬇ arrow to consequences: 📉 Standing still + 🧠 Too complex BIM Tools
- Stats: $177B lost/year (McKinsey 2017), 20% of tool features used, 50 years same problems (Eastman 1975 → Today)
- DHH quote removed from this slide

### Slide 4 — THE INDUSTRY'S BETS
- 3 blocks: ISO 19650 (right principle, wrong tools), OpenBIM/IFC (right destination, still a file format), Digital Twins (right vision, wrong foundation)
- DHH vendor lock-in quote REMOVED

### Slide 5 — THE SOLUTION (Demo intro)
- Matrix rain background (green falling code with Japanese + BIM characters)
- THE SOLUTION 🛠️ in gold
- "An open source, AI-enabled, community-driven BIM platform."
- 4 blocks: Open Source, AI-Enabled, Community Driven, Vibe-Coded
- DEMO 🚀 in big green text
- **KNOWN ISSUE:** Text visibility over matrix rain — tried many approaches (text-shadow, dark panels, z-index). Current approach uses `-webkit-text-stroke` and z-index:20. May need further work.

### Slide 6 — YOUR TURN (Close)
- YOUR BIM. YOUR RULES. YOUR TOOLS. in gold
- Antonio (That Open Company) quote: "They told me I couldn't build what the billion-dollar companies had. I did it anyway. Free and open source."
- "Now it's your turn."
- "The tool nobody built? Build it this weekend."
- 🧑🏻‍💻🤘🏻

---

## TWO CHARACTER AVATARS

### DHH — David Heinemeier Hansson (~85% of quotes)
- Style: Orange border (#ff8800), dark background (#1a0800)
- CSS class: `.dhh`
- Role: The philosopher. Anti-monopoly, pro-ownership, anti-SaaS
- Full name shown as footnote on slide 2: "DHH — David Heinemeier Hansson, CTO 37signals, creator of Ruby on Rails"

### Antonio — That Open Company (~15% of quotes)
- Style: Teal border (#00c896), dark background (#001a10)
- CSS class: `.ant`
- Role: The proof. "I built it. Free and open source."
- Only appears on slide 6 (close)
- Voice based on his real LinkedIn posts (see antonios_posts.txt)

---

## DESIGN SYSTEM

### Theme
- Retro 8-bit / Minecraft aesthetic
- Font: Press Start 2P (Google Fonts)
- Background: #0d1117
- Green grass bar at top
- Hotbar navigation at bottom (like Minecraft)

### Key CSS Classes
- `.slide` — flex column, centered, full viewport
- `.dhh` — orange quote block
- `.ant` — teal quote block
- `.block` — dark info card with emoji icon + yellow title
- `.blocks` — flex row of blocks
- `.wiki` — Wikipedia-style info box (cream background)
- `.chat` — terminal/console style box
- `.big` — huge text (clamp 32px-80px)
- `.stats` / `.stat` — number stats with labels
- `.ach` — achievement unlocked banner (yellow border)
- `.tm` — floating team member (absolute positioned, animated)
- `.vi` — vendor icon with laser animation
- `.xpw` / `.xpf` / `.xpl` — XP progress bar

### Navigation
- Arrow keys left/right
- Number keys 1-6
- Hotbar click at bottom
- Slide counter top-right

---

## CONTENT SOURCES

### Pitch content based on:
- Charles Eastman's 1975 BIM vision (4 pillars)
- Industry failure analysis ($177B McKinsey 2017, productivity stagnation)
- Industry response (ISO 19650, OpenBIM/IFC, Digital Twins)
- Danish construction productivity charts (shared by user)
- Antonio's LinkedIn posts (That Open Company / open-source BIM philosophy)
- DHH philosophy (anti-SaaS, software ownership, open source)
- Patrick MacLeamy quote on BIM as knowledge integration

### Key pitch narrative:
1. The dream was right (1975)
2. The industry broke it (vendors, lock-in, handover death)
3. Current fixes are insufficient (standards without tools)
4. Our solution: open-source + AI + community BIM platform
5. DEMO
6. Your turn to build

---

## OPEN ISSUES / TODO
- [ ] Slide 5 matrix rain: text still hard to read over dense matrix. Needs better solution (tried: text-shadow, dark panels, rgba backgrounds, text-stroke). The matrix rain JS works perfectly — it's just the text visibility.
- [ ] Team member names: 2 members still unnamed (removed earlier, now only 6)
- [ ] Team name "BBB" is placeholder
- [ ] Vendor icons on cover: laser animation works but icons could use real logos
- [ ] Font sizes could be bigger for presentation on large screen (10m viewing distance)
- [ ] The main BIM authoring app is at localhost:4000 (vite dev server from the authoring-main project)

---

## TECH STACK
- Single HTML file (index.html)
- Inline CSS + inline JS
- Google Fonts (Press Start 2P)
- Canvas API for Matrix rain effect
- CSS animations for floating members, laser targeting, vendor destruction
- GitHub Pages for hosting
- No build tools needed — pure static HTML
