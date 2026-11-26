# Vanguard Esports website — deployment notes

## Included update
- Rebuilt `matches.html` from the previously empty schedule placeholder.
- Added the supplied CyberClash Season 3 and NLK League tournament banners under `assets/images/tournaments/`.
- Added three confirmed schedule entries: NLK / Vanguard Academy vs FGS Academy; NLK / Vanguard United vs Veil Team; CyberClash Season 3 Open Qualifier #1 / Vanguard Academy.
- Added working Upcoming / Live / Results filters and accessible mobile navigation behavior on the Matches page.
- Standardized the primary navigation across the site's main pages so the Awards page is not omitted on selected pages.

## Publish
Upload the contents of this folder to the root of the existing static website, preserving the `assets/` directory. The homepage should remain `index.html`.

## Important data notes
- NLK matches: 26–27 November 2026, start time not yet specified, Round of 16 (1/8 final), Round 1, BO1.
- CyberClash: 29 November 2026 at 18:00 MSK, Open Qualifier #1. No match format or opponent has been added because those details were not supplied.
- Live and Results currently show honest empty states; no unverified match results were invented.

## Audit scope
Local HTML links and image/script references were checked, duplicate HTML IDs were checked, and inline JavaScript passed `node --check`. This is a static-file audit; it does not replace a live browser/device test or hosting/CDN configuration check.

## Media library
All new website images should be stored inside `assets/images/`:
- `tournaments/` — tournament and league banners
- `news/` — news article images
- `rosters/` — roster announcement graphics
- `players/` — player portraits and profile images
- `logos/` — organization, team, and partner logos
- `backgrounds/` — page and section backgrounds

Add new images to the appropriate folder and reference them by their relative path in HTML. You do not need to re-upload or replace other images when adding a new one; upload the new image and the page/code that references it. Keep filenames stable and descriptive. Do not delete an image while any page still references it.

## Safe update procedure
1. Keep a backup of the currently published website before replacing files.
2. Extract this ZIP locally and inspect the `vanguard-esports-main/` folder.
3. For a full deployment, upload the *contents* of `vanguard-esports-main/` to the hosting document root and allow matching files to be overwritten. Preserve the existing domain/hosting configuration.
4. Do not manually delete the hosting root or unrelated hosting files. If the host requires a clean deployment, first make a backup and confirm the document root contains only this website.
5. After upload, open the homepage and Matches page, then test on desktop and mobile.
