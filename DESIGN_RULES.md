# KARLE — Design Direction & Anti-AI-Slop Rules

Status: approved design direction. Applies to all subsequent work on `davisl24/karle`.
Sources: KESTREL WEBSITE PROJECT WORKFLOW v1.0 and the Seven-Principle Premium Site Checklist.
This is a practical implementation brief, not permission to change approved content or structure.

## 1. What we are building
- Unofficial compact demo for KARLE, a guesthouse near the Baltic Sea in Vitrupe.
- Approved concept: **C — Refined Hospitality**.
- Goal: show the place clearly, build trust, help guests explore accommodation and find a reservation route.
- Six existing sections remain: hero, rooms, leisure, surroundings, reviews, reservation/contact.
- Avoid developing a custom booking system for this demo.
- Work in `main` for approved revisions, as requested by the project owner.

## 2. Non-negotiable anti-template rules
- No generic SaaS-style card grids, repetitive 3-column icon features, arbitrary labels, counters, gradients, glassmorphism, or decorative animations.
- No purple/blue gradients, gratuitous rounded pills, emoji headings, generic placeholder copy, or filler sections to make the page longer.
- No AI-generated or unrelated stock photos pretending to show KARLE. Only authentic, approved photos; otherwise clearly marked placeholders.
- Do not claim amenities, pricing, quotes, scores, booking availability, or contact information without confirmation.
- Do not confuse minimalism with large empty areas: every gap must support hierarchy.
- Do not make all section layouts identical. Set a deliberate rhythm with restrained, consistent alignment.

## 3. Page composition to implement
### Navigation
- Quiet, precise navigation; strong KARLE wordmark.
- One visually dominant action: accommodation / reservation.
- On mobile, navigation must be clear, accessible and easy to close.

### Hero
- One strong real property or coastal image, once image rights are secured.
- Clear guesthouse and location context, concise meaningful headline and one obvious CTA in first screen.
- Avoid text collisions and illegible overlays, especially at 375px width.
- The hero must answer: where am I, what is offered, why does it matter, what next?

### Rooms
- Treat photos as evidence, not decoration.
- Display room types with readable differences; use editorial rows, not a uniform collection of cards.
- Don't invent prices, bed types, bathroom details or views without confirmation.

### Leisure & surroundings
- Show verified facilities and authentic surroundings without excessive iconography.
- Make the place itself visually distinctive; no unrelated aspirational imagery.

### Reviews
- Real source, accurate attributed ratings. Prefer a direct path to original reviews over invented quotations.
- Position proof where it helps a decision, not only because the template expects a testimonials block.

### Reservation
- One unambiguous action; clearly indicate if the external Booking page is only informational or bookings are unavailable.
- Avoid simulated calendars, availability or checkout.

## 4. Seven visual checks — required on desktop and mobile
1. **Hero:** headline + context + trust + one action legible without scrolling.
2. **Hierarchy:** the intended first, second and third focal points are visually clear.
3. **Whitespace:** purposeful breathing room; no giant dead zones.
4. **Contrast:** legible body text and a clearly differentiated primary CTA.
5. **Proof:** reviews and ratings appear near the relevant decision.
6. **Typography:** one or two coordinated font families, clear scale, legible body copy.
7. **Mobile:** check actual 375px (and 768px, 1440px) layouts, tap targets, no overflow.

## 5. Visual review / acceptance process
- Before code, state which approved element the proposed change affects, and why.
- After code, inspect rendered desktop AND phone, not just syntax/commit success.
- Report specific failures: element, viewport, issue and fix.
- Test navigation, booking links, image loading, horizontal overflow, text contrast and keyboard focus.
- Do not call a release visually finished while the real-property photos are missing.
- Change only the part that failed. Do not restart the whole design without new evidence.

## 6. Source of truth
- `KESTREL_WEBSITE_PROJECT_WORKFLOW_v1.0`: project research, options and approval discipline, design QA.
- `seven-principle-checklist`: hero, hierarchy, whitespace, contrast, proof, typography, mobile.
- User-approved decisions override exploratory options. No unrequested changes to approved parts.

## 7. KARLE typography, spacing and labels — approved implementation baseline

These are project-specific design tokens, not arbitrary universal KESTREL rules. Keep the approved full-width hero and six-section structure.

### Type scale
- Display/H1: Georgia, regular 400; desktop fluid 64–96px, mobile fluid 44–58px; line-height 1.06; modest negative tracking. Only one H1.
- H2: Georgia, regular 400; desktop 40–58px, mobile 34–42px; line-height 1.14.
- H3: Georgia, regular 400; 26–36px; line-height 1.18.
- Main body: Arial or system sans, 16px, line-height 1.7; ideally max 60–70 characters per line.
- Meta/supplemental text: 13–14px, never 10–11px for essential information.
- Navigation/buttons: 14px; normal-to-medium weight, at least 44px comfortable click/tap target.
- Typography families: Georgia for editorial headlines; Arial/system sans for interface and paragraphs. Never more than two families in this demo.

### Spacing system
- 8px base rhythm with tokens: 8, 16, 24, 32, 48, 64, 96px.
- Section vertical padding desktop: ~88–104px; mobile ~64–72px, intentional exceptions only for hero.
- Paragraph to action: 24–32px; eyebrow to heading (when needed): 12–16px; heading to description: 20–24px.
- Use consistent container padding and text measure. Avoid arbitrary repeated 112px padding.

### Meta labels and punctuation
- Do not place a label above every heading: only show labels that add new useful context (e.g. source/Booking attribution, location, room category).
- Prefer natural Latvian sentence case for meaningful labels; no forced ALL CAPS headings.
- Do not use decorative "01 / SECTION" labels, slash-heavy breadcrumbs, or ornamental periods after headline fragments.
- Headlines should be concrete and coherent; avoid duplicated information in kicker + heading + paragraph.
- Retain punctuation when required for natural Latvian grammar, not as decoration.

### QA gates
- Confirm that sizes and text density remain legible at widths 375px, 768px, 1440px.
- Check line breaks and CTA visibility in the hero against the eventual real image; for the demo, placeholders are intentionally neutral.
- Check all sections use the same typographic scale rather than individual one-off heading values.
- Do not claim browser visual validation from code inspection alone.

## 8. Updated KARLE type and CTA decision (2026-10-19)
- Previous Georgia/Arial pairing in section 7 is superseded for this demo by **Manrope** for headings, body, navigation and controls. Fallback: Arial/Helvetica/sans-serif.
- H1 53–88px desktop and ~41–57px mobile, weight 500. H2 35–54px desktop and 32–40px mobile, weight 500. H3 25–34px. Prioritize readable proportions over ornamental display styling.
- All primary CTA buttons, including header, hero and final reservation, share the same dark-green background (#42594f), white text, 52px minimum height and hover color. On image backgrounds keep enough contrast to distinguish button edges.
- Headings must explain the actual section: accommodation types, facilities, geographic surroundings, review source, booking action. Reject generic lifestyle slogans and repeated information across heading and paragraph.
- A font or copy change does not authorize changing the user-approved full-width hero composition or six-section information architecture.
- Check headings, truncation, CTA contrast and content at 375/768/1440px in a browser before calling the design finished.
