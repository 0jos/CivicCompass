CHINATOWN CIVIC COMPASS - CLAUDE CODE DEVELOPMENT PROMPT

=== PROJECT OVERVIEW ===

You are building a professional, world-class civic education website for the "Chinatown Civic Compass," a community initiative created by Oliver Josephson (high school senior at The Ross School) to empower residents with knowledge about their rights and civic engagement opportunities.

**Mission:** Provide free, accessible, multilingual civic education that could literally save lives by helping people understand their constitutional rights, especially around immigration enforcement.

**Stakes:** This is serious work. The information provided can make the difference in whether or not someone is deported. The site must feel friendly and familiar, but NOT amateur. Professional design, credible sourcing, expert-backed content.

---

=== CURRENT STATE ===

**Completed Files:**
- index.html: Home page with hero, 4 learning modules, about section, footer
- faq.html: Separate FAQ page with search and category filters

**Design Foundation:**
- Sharp, angular aesthetic (clip-path polygons, not rounded corners)
- Warm color palette bleeding throughout (reds, golds, warm creams)
- No lantern decorations, but compass elements present
- Professional, vibrant, alive energy (inspired by Chinatown street photography)
- Accessible for elderly users (large fonts, high contrast, clear hierarchy)
- Trilingual capability: English (default), Simplified Chinese, Traditional Chinese
- Language selection via popup (cookie-persisted)
- All text marked with [TRANSLATING, THX! -OLIVER] for easy translation

**Color Palette:**
- Primary Red: #c41e3a (action, authority)
- Gold/Accent: #f4a460 (warmth, energy)
- Green/Secondary: #2a5f4a (stability, community)
- Warm Gradients: Cream to tan throughout
- Dark Footer: #1a1a1a with gradient

**Key Features:**
- Module cards with expandable credibility boxes (for attorney names, sources, dates)
- Modal system for module content
- No account required, no sign-ups
- Analytics-ready (event tracking hooks in place)
- Responsive mobile design

---

=== THE FOUR LEARNING MODULES ===

1. **Know Your Rights** (⚖️)
   - Constitutional rights regardless of immigration status
   - What ICE can/cannot do
   - How to protect yourself

2. **Local Resources** (🤝)
   - Community organizations
   - Legal aid services
   - Support networks in Chinatown and beyond

3. **Voting & Elections** (🗳️)
   - Voter registration
   - Polling locations
   - Making your voice heard

4. **Getting in Touch** (📞)
   - Contacting elected representatives
   - Civic engagement pathways

---

=== FREELANCE IDEAS TO IMPLEMENT ===

**PRIORITY 1 (Start Here):**

1. **Chinatown Photo Hero Integration**
   - Integrate the Chinatown street photography as subtle background in hero section
   - Dark overlay to keep text readable
   - Creates sense of place, feels lived-in and real
   - Alternative: Carousel of community photos (arotates, humanizes project)

2. **Browser-Based Progress Tracking**
   - Use localStorage to track which modules users have viewed
   - Show progress bar: "You've explored 2 of 4 modules"
   - Unlock badges as they complete modules (visual reward, no login)
   - Satisfying UX without requiring accounts

3. **Print-Friendly Resources**
   - "Print Guide" button on each module that generates clean PDF
   - Downloadable "wallet cards" with emergency numbers and key rights
   - QR codes linking back to modules (physical-digital bridge)
   - Critical for elderly users who want tangible materials

---

**PRIORITY 2 (High Impact):**

4. **Attorney Names & Credibility**
   - Credibility boxes already built; need placeholders Oliver can fill in
   - Format: "Reviewed by [Attorney Name], [Organization]"
   - Last updated date on each module
   - Sources citation field
   - Small disclaimer: "Expert-informed, not legal advice"

5. **Emergency Contact Card Generator**
   - Interactive tool that lets users create personalized wallet cards
   - Fields: Local representatives, legal aid hotlines (RAICES, etc.), QR code
   - Printable, shareable
   - Extremely practical for community

6. **Mobile-First Legal Actions**
   - Click-to-call buttons for hotlines (opens phone dialer)
   - Text-to-speech option on content
   - Larger touch targets
   - Make taking action frictionless

7. **Glossary/Translation Helper**
   - Clickable legal terms open popup with simple definition
   - Shows definition in all three languages
   - Sidebar or tooltip system
   - Critical for accessibility

---

**PRIORITY 3 (Nice to Have):**

8. **Video Testimonials Section**
   - 30-second community member videos on home page
   - "This helped me understand my rights"
   - Phone videos are fine, doesn't need to be polished
   - Builds trust, humanizes project

9. **Real Scenario Interactive Modules**
   - Branching scenarios instead of passive info
   - "You're stopped by police. What do you do?" → choose → get feedback
   - Makes it memorable and engaging

10. **"Suggest a Question" Feature**
    - Simple form on FAQ page
    - Community can submit questions
    - Shows people are listening
    - Removes static website feeling

11. **Offline Mode / PDF Downloads**
    - Allow users to download modules as PDFs
    - Offline access for spotty internet areas
    - Service worker for offline reading

12. **Smart Language Detection**
    - Auto-detect browser language preference
    - Suggest it before modal ("We detected Simplified Chinese")
    - Still allow override
    - Smoother UX

13. **Analytics Dashboard**
    - Track which modules get most time
    - Which FAQ questions get searched
    - Identify content gaps
    - Use data to improve over time

14. **Partner Showcase Section**
    - Photos of reviewing attorneys
    - Logos of partner orgs (ACLU, Museum of Chinese in America, etc.)
    - Quotes from partners
    - Massive credibility boost

---

=== TECHNICAL SPECIFICATIONS ===

**Framework:** Pure HTML/CSS/JavaScript (no dependencies)
- Vanilla JS only
- CSS with clip-path for angular design
- localStorage for client-side persistence
- No external libraries unless absolutely necessary

**File Structure:**
- index.html (home page, 4 modules, about)
- faq.html (separate FAQ page)
- Consider adding: offline.html (offline fallback), styles/main.css (optional modular CSS)

**Browser Compatibility:**
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile-first responsive design
- Works on devices with spotty internet

**Accessibility:**
- WCAG 2.1 AA standard
- High contrast (especially important for elderly users)
- Large readable fonts
- Proper heading hierarchy
- Alt text on all images
- Keyboard navigable
- Respects prefers-reduced-motion

**Performance:**
- No external fonts (system fonts optimized)
- Lazy load images if added
- Optimize for mobile first
- Fast load time (< 2s on 3G)

**Internationalization (i18n):**
- All text ready for translation
- Currently marked: [TRANSLATING, THX! -OLIVER]
- Three languages: en, zh-s, zh-t
- Cookie-based language persistence
- Consider: gettext/i18n.js if scaling to many languages

---

=== CONTENT PLACEHOLDERS ===

**Module Content:**
Each module has placeholder: "Add your slideshow, video, or detailed content here."
- Can embed YouTube videos
- Can embed PDFs
- Can embed PowerPoint presentations
- Can add custom HTML

**Credibility Boxes:**
- [Attorney Name - Add Here]
- [Add source citations here]
- Last updated: 2025-01-05 (update as content changes)

**Footer Contact:**
- info@civiccompass.org (update as needed)
- Partner organizations (ACLU, OLA of Eastern Long Island, Museum of Chinese in America, others)

---

=== DESIGN SYSTEM ===

**Color Variables (use throughout):**
```
--primary: #c41e3a (red - authority, action)
--primary-light: #e63946 (lighter red - hovers)
--secondary: #2a5f4a (green - stability)
--accent: #f4a460 (gold - warmth, energy)
--dark: #1a1a1a (almost black)
--light: #faf9f7 (warm off-white)
```

**Typography:**
- Display: Georgia serif (elegant, authoritative)
- Body: Segoe UI (accessible, clean)
- Font sizes: Responsive, large for accessibility

**Angular Elements:**
- Use clip-path for sharp edges: `polygon(0 0, 100% 0, 100% calc(100% - 20px), calc(100% - 20px) 100%, 0 100%)`
- Logo: 8-sided compass shape
- Buttons: Angled bottom corners
- Cards: Diagonal cuts at bottom

**Spacing & Hierarchy:**
- Generous padding for readability
- Clear visual separation between sections
- Color and shadow for depth

---

=== USER JOURNEYS ===

**Journey 1: First-Time Visitor (Elderly User)**
1. Land on home page
2. See language picker modal
3. Select language (stored in cookie)
4. Read hero + features
5. Browse learning modules
6. Click on "Know Your Rights"
7. Read content, see credibility box
8. Print PDF or download wallet card
9. Exit feeling informed and safe

**Journey 2: FAQ Searcher**
1. Click "Resources" in nav
2. Go to faq.html
3. Search for "ICE" or "rights"
4. Get relevant Q&A
5. Click on answer to expand
6. Potentially print or share

**Journey 3: Returning Visitor**
1. Land on home page
2. Progress bar shows: "You've explored 2 of 4 modules"
3. Continues where they left off
4. Completes remaining modules, unlocks badge

---

=== TRANSLATION STRATEGY ===

**Current State:** All text marked with [TRANSLATING, THX! -OLIVER]

**Oliver's Process:**
1. Edit HTML directly
2. Replace English text with Simplified Chinese, Traditional Chinese
3. Keep structure identical
4. Can use Google Translate as starting point, then refine

**Example:**
```html
<h1>Let Your Civic Compass Guide the Way</h1>
<!-- TRANSLATE ABOVE: 
     Simplified Chinese: [TRANSLATING, THX! -OLIVER]
     Traditional Chinese: [TRANSLATING, THX! -OLIVER]
-->
```

Becomes:

```html
<h1>让你的公民指南针指引方向</h1>
<!-- Simplified Chinese version -->
<!-- 讓你的公民指南針指引方向 -->
<!-- Traditional Chinese version -->
```

**Note:** Currently, language selection is built in but not functional (just stores preference). Full i18n implementation can come later once translations are ready.

---

=== SUCCESS METRICS ===

The site is successful when:
- ✅ Adults and elderly users can navigate intuitively
- ✅ Information is accurate and expert-reviewed
- ✅ Users feel informed about their rights
- ✅ Users can take action (call hotline, print guide, contact rep)
- ✅ Site works on mobile and slow internet
- ✅ No login/barriers to access
- ✅ All three languages supported
- ✅ Design feels professional, not amateur
- ✅ Credibility is visible (attorney names, sources, dates)

---

=== DEVELOPMENT PRIORITIES ===

**Phase 1 (Foundation - Already Done):**
- HTML structure ✅
- Responsive design ✅
- Angular aesthetic ✅
- Warm colors throughout ✅
- Module cards + modals ✅
- FAQ page ✅
- Translation placeholders ✅

**Phase 2 (Priority Features - Build Next):**
- Add Chinatown photo to hero
- Progress tracking (localStorage)
- Print/PDF functionality
- Attorney name/credibility fields
- Mobile-optimized action buttons
- Glossary tooltips

**Phase 3 (Enhancement - Build After):**
- Interactive scenarios
- Video testimonials
- Contact card generator
- Offline mode
- Partner showcase

**Phase 4 (Polish - Final):**
- Analytics integration
- Language auto-detection
- Translations (once Oliver completes them)
- Performance optimization

---

=== NOTES FOR OLIVER ===

This is your project. You own it. The design, the code, the content—all of it should reflect your voice and your vision. 

A few key things:
1. **Keep it honest.** No hype. Just solid information.
2. **Optimize for your community.** Elderly users might prefer bigger fonts, simpler language, printable guides.
3. **Get attorney names ASAP.** That credibility is huge.
4. **Test with real people.** Show it to someone in Chinatown. Ask: "Does this help you feel more informed about your rights?"
5. **Update it.** Laws change. Keep dates current. When attorneys review content, record it.

This resource matters. People's lives depend on it. Build it with that in mind.

---

=== QUESTIONS FOR CLAUDE CODE ===

When starting work, ask:
1. Which Priority 1 feature should we build first?
2. Do we need to restructure any HTML for the new features?
3. Should we create a modular CSS file for easier maintenance?
4. What's the best approach for PDF generation (client-side or backend)?
5. Should we add any security considerations (CSP headers, etc.)?

---

Good luck, Oliver. You're building something real. 🧭
