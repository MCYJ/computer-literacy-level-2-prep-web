# 컴퓨터활용능력 2급 Prep marketing site context

## Identity and scope

- Service ID: `KOR-0008`
- Android package / iOS bundle: `app.mcyj.examprep.kor0008`
- Public repository: `MCYJ/computer-literacy-level-2-prep-web`
- Production URL: `https://mcyj.github.io/computer-literacy-level-2-prep-web/ko/`
- Scope is public marketing and useful exam-study content for the currently released app only. The source app remains read-only.

## Store state verified 2026-09-18

- Google Play exact package page returned HTTP 200 and is the only active download destination.
- The expected App Store public URL returned HTTP 404 and Apple lookup returned no public result for the exact bundle. The website therefore presents App Store as a disabled “coming soon” label with no link.
- The site describes the released Play build and does not claim that a private/internal draft is publicly available.

## Current official exam facts used

- Level 2 written: Computer Fundamentals and Spreadsheet Fundamentals, 40 multiple-choice questions, 40 minutes.
- Level 2 practical: Spreadsheet Practice, computer task, 40 minutes.
- Passing: written requires at least 40 in each subject and 60 average; practical requires 70.
- The 2024–2026 specification uses Microsoft Office LTSC Professional Plus 2021. The announced 2027–2029 specification applies from 2027-01-01 and is not presented as current.
- KCCI says continuous question-bank items are not public. Site and app materials are described as independently authored practice, never as live exam items.
- Registration, schedules, fees, software and venue rules are directed to current KCCI pages because they can change.

## Product and design

- Korean primary locale plus useful English localization.
- 10 substantive guides per locale, FAQ, privacy, terms, support and contact routes.
- Powder-blue spreadsheet-cell visual system derived from the app palette: `#F8FBFC`, `#E7F1F5`, `#6F9FB3`, `#3E7187`, `#B9D7E2`, `#20313D`, with a restrained orange marker accent.
- Global typography uses `word-break: keep-all` and `overflow-wrap: break-word`; only long email/source links use `overflow-wrap: anywhere`.
- App claims are limited to the current listing: 500 independently authored questions, five mock exams, local progress and no required RushLabs account.

## Build and QA

- `npm run build` generates static files under `dist/` with canonical, hreflang, Open Graph, JSON-LD, sitemap, robots and custom 404 metadata.
- `npm run check` verifies internal routes, required metadata, output count, global keep-all, exact Play identity, disabled App Store state and absence of an App Store link.
- GitHub Actions publishes `dist/` to GitHub Pages.

## Work log

- 2026-09-18: Created the bilingual marketing/study site for released KOR-0008, using a distinct spreadsheet worksheet design and verified Level 2 facts. Production deployment evidence will be appended after GitHub Pages publication.
- 2026-09-18: GitHub Pages deployment run `35355743134` passed. Production QA returned HTTP 200 for all 34 sitemap routes and sampled assets, HTTP 404 for a missing route, confirmed the deployed `word-break: keep-all`, exact Play package link, disabled App Store label and absence of any App Store URL.
- 2026-09-18: Normalized the live Play badge and disabled App Store control to a shared 194×75 frame; local build and check passed.
