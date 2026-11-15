# Semantic HTML Personal Profile

The original Homework 1 profile, expanded for Homework 2 (CSS) and Homework 3 (responsive layout).

- Live page: https://joladele-pg.github.io/semantic-html-profile/
- Repository: https://github.com/joladele-pg/semantic-html-profile

## HTML foundation

The page retains its original semantic header, nav, main, section, article, figure, figcaption, footer, English language, descriptive title, logical h1/h2/h3 outline, descriptive image alternative, and unordered lists.

## Homework 2: styling

The head links to a separate styles.css. Type selectors (body, h1), class selectors (.card, .section), and ID selectors (#main-content) are present. The focus cards, project cards, and illustration card each demonstrate deliberate margin, padding, and border. Navy, blue, slate, and off-white form the palette, with Poppins and Open Sans fonts and system fallbacks.

## Homework 3: responsiveness

Grid creates card and skills layouts; Flexbox creates wrapping navigation. At 640px skills and cards use two columns; at 1024px skills use three columns, the header becomes horizontal, and spacing increases. Mobile remains one column. Fluid image sizing prevents overflow. The page was checked at 320px, 768px, and 1200px.

## Homework 4: accessibility audit

**Original WAVE baseline, November 15, 2026: 0 errors, 0 contrast errors, 0 alerts.** The original page already had alternative text, headings, language, and landmarks. It would be inaccurate to report three WAVE errors.

Manual testing identified and addressed three issues:

| Issue / affected element | WAVE result | User impact | Fix |
|---|---|---|---|
| Navigation linked to missing projects.html and about.html | Not flagged; this scan did not check destination availability | Following navigation led to 404 pages | Replaced missing-file links with working #projects and #education anchors and accurate labels |
| Fixed 640px illustration produced 688px-wide content in a 320px viewport | Not flagged; found through manual viewport testing | Mobile users had to pan horizontally to see the image | Added max-width:100%, height:auto, fluid containers, and responsive layout |
| No direct keyboard bypass of repeated navigation | No alert; landmarks were present | Keyboard users had to traverse repeated navigation before the content | Added a first-focusable skip link, focusable main target, and visible focus styling |

These are three manual findings, not three WAVE findings. The assignment's requirement for three WAVE-reported issues needs instructor clarification because the original page produced none. Baseline screenshots are retained with the submission materials. No defects were introduced to create an artificial before/after result.

## Contrast and verification

Calculated contrast: navy on white 17.85:1; slate on off-white 9.90:1; blue on white 5.17:1; light footer text on navy 12.02:1. Local links and fragments, a single h1, and image alternative text were checked. Published-page WAVE results and evidence appear below.

## Files

index.html is the semantic profile; styles.css contains the external styling and breakpoints; profile-illustration.svg is the original illustration. Open index.html locally or use the live URL above.

## Published-page verification - November 15, 2026

WAVE checks of the published updated pages reported **0 errors and 0 contrast errors**. All 16 text/background pairs also passed normal-text WCAG AA in the official WebAIM Contrast Checker API; the lowest result was 4.93:1. Exact checker responses and source links are saved in [the contrast report](docs/webaim-contrast-checks.json). The earlier calculated ratios above use ordinary rounding; WebAIM displays truncated ratios.

Keyboard activation of the skip link moved focus to main-content. Checks at 320px, 768px, and 1200px found no horizontal overflow. Static link, fragment, heading, and label/reference checks passed. These checks cover the tested states and do not establish complete WCAG conformance.

### Before/after evidence

- [Original WAVE scan: no errors or alerts](docs/evidence/wave-profile-before.png)
- [Original mobile page](docs/evidence/profile-mobile-before.png)
- [Original navigation link leading to a 404](docs/evidence/profile-broken-link-before.png)
- [Revised mobile page](docs/evidence/profile-mobile-after.png)

During development, WAVE identified a possible-heading alert on the styled brand paragraph. The brand is a site identifier rather than a heading, so it was changed to a span while preserving the document outline. This development alert is separate from the original zero-alert baseline.

The [final published WAVE scan](docs/evidence/wave-profile-after.png) reports **0 errors, 0 contrast errors, and 0 alerts**. [Recorded scan summary](docs/wave-final-results.json).
