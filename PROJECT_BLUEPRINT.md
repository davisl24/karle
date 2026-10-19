# KARLE — Project Blueprint

**State:** Demo V1 implemented · code consistency review completed · visual QA pending.
**Project:** Unofficial KARLE guesthouse demo; not an official property website.
**Authoritative files:** Kestrel 01 Workflow v1.1; Kestrel 02 Visual Direction v1.1; this KARLE-specific blueprint; verified client materials/Booking source. Existing DESIGN_RULES.md is historical guidance; conflicts resolved by user-approved decisions recorded here.

## Approved / LOCKED
- Website: five pages: `/`, `/numuri/`, `/atputa/`, `/par-mums/`, `/kontakti/`.
- Art direction: **C — Refined Hospitality**; calm, legible, restrained.
- Full-width home hero; no generic decorative eyebrow labels. Hero has an explicit photographic placeholder for demo.
- Typography: **Manrope** across headings, copy, navigation and controls. Do not switch to Georgia.
- CTA palette: deep green **#42594f**, white text; one recognizable primary button system.
- Accommodation and leisure amenity icon lists (two columns on desktop, one on narrow phones).
- Real KARLE imagery only with rights to use it. Placeholder blocks are acceptable for internal demo.
- Compact website rather than a bespoke booking engine.
- Approved production updates go to GitHub `main`.
- No unrequested restyling of approved elements.

## Project design tokens — consolidated code baseline
These are actual implementation targets, not universal Kestrel defaults.
- Font family: Manrope / Arial fallback; body approx. 16px; line-height approx. 1.7.
- Inner content max width: **1280px**; responsive horizontal gutter **20–48px**, mobile **18–24px**.
- General section vertical padding: **72–104px desktop**, approx. **64px mobile**.
- Internal-page headings: H1 approx. **48–78px desktop**, **38–54px mobile**; H2 approx. **32–48px desktop**, **30–38px mobile**; H3 approx. **23–30px desktop**, **22–28px mobile**.
- Home full-screen hero typography is a user-approved intentional larger exception (up to approx. 88px desktop).
- Main button minimum height: about 52px. Mobile links/buttons require sufficient touch area, keyboard focus visibly outlined.
- Colors: background #f9f8f5, primary text #252c29, accent #42594f, muted neutral shades.
- Motion: no unnecessary animation; respect reduced-motion. No slider or scroll-jacking.
- Responsive QA targets: 360, 390, 768, 1024, 1440px; these are testing points, not required breakpoints.

## Information architecture and CTA
- Home: hero → about → rooms preview → leisure → location → Booking review link → booking status.
- Rooms: overview, specific room types, amenity list, information CTA.
- Leisure: breakfast, garden/terrace, active activities, families.
- About: place/story, Baltic coast, location, guests' ratings.
- Contacts: Booking reservation limitations, address, arrival/check-out/rules.
- Booking.com currently is not a verified working booking path. Link labelled informationally; do not imply reservation completion is possible.

## Content verification / unresolved
- Property facts derived from previously supplied Booking information; owner verification remains outstanding.
- Pricing/availability/telephone/email are not confirmed. **Do not fabricate**.
- Scores and review counts can change. Check before external presentation.
- Source imagery not licensed for use on a public mockup; continue using explicitly labelled placeholders until permission.
- Mobile touch and visual layout, 404s, performance/contrast checks and live production rendering require real browser QA.
- If a claim about facilities conflicts between sources, qualify it rather than guessing.

## Change and QA discipline
Changes require new evidence, a verified UX problem, a technical defect, or the user's explicit instruction. For each problem, fix only what is necessary, check on mobile and desktop, then lock it. Do not treat GitHub code inspection as visual testing.

## QA status (2026-10-19)
- [x] Five route HTML files present.
- [x] Main navigation paths in source verified.
- [x] Skip link, keyboard escape and focus styles added.
- [x] Shared heading/container/spacing values applied in source.
- [ ] Responsive rendering at 360, 390, 768, 1024, 1440 px inspected manually.
- [ ] Interactive navigation tested in browser with mouse + keyboard.
- [ ] Mobile contrast/overflow, link status, Lighthouse/Core Web Vitals checked.
- [ ] Booking contact/reservation information confirmed with owner.
- [ ] Official property photo permissions received.
- [ ] Demo approved for external public presentation.
