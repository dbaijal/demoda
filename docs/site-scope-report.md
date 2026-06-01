# Thermo Fisher Scientific US/EN Site Scope Analysis Report

**Site:** thermofisher.com/us/en/home  
**Total URLs Analyzed:** 39,543  
**Date:** 2026-06-01  
**Source CMS:** Adobe Experience Manager (AEM Sites - Classic/Touch UI)

---

## 1. Page Template Distribution

| # | Template Type | URL Count | % of Site |
|---|---|---|---|
| 1 | Life Science Product Pages | 7,558 | 19.1% |
| 2 | Form Pages (lead gen/gated content) | 7,247 | 18.3% |
| 3 | Confirmation/Thank-You Pages | 4,896 | 12.4% |
| 4 | Industrial Product Pages | 2,803 | 7.1% |
| 5 | Learning Center Articles | 2,287 | 5.8% |
| 6 | Promotional Landing Pages | 1,932 | 4.9% |
| 7 | Virtual Tours / 3D Product Demos | 1,329 | 3.4% |
| 8 | Event Pages | 1,322 | 3.3% |
| 9 | Clinical Product Pages | 1,129 | 2.9% |
| 10 | Promo Cart Modals | 1,016 | 2.6% |
| 11 | Protocol/Method Pages | 735 | 1.9% |
| 12 | Promo Modals | 723 | 1.8% |
| 13 | Cell Line Database Entries | 621 | 1.6% |
| 14 | Technical Reference Library | 580 | 1.5% |
| 15 | Electron Microscopy Pages | 516 | 1.3% |
| 16 | Brand Pages | 526 | 1.3% |
| 17 | Tech Support Articles | 402 | 1.0% |
| 18 | Blog Posts | 304 | 0.8% |
| 19 | Materials Science Pages | 105 | 0.3% |
| 20 | Handbook Chapters | 292 | 0.7% |
| 21 | Newsletter/Journal Articles | 268 | 0.7% |
| 22 | Bioprocessing Pages | 241 | 0.6% |
| 23 | Services Pages | 228 | 0.6% |
| 24 | Press Releases | 228 | 0.6% |
| 25 | News Gallery Pages | 135 | 0.3% |
| 26 | About Us / Corporate Pages | 173 | 0.4% |
| 27 | New Ideas/Innovation Pages | 138 | 0.3% |
| 28 | Software Download Pages | 116 | 0.3% |
| 29 | Chemicals Pages | 87 | 0.2% |
| 30 | Digital Solutions Pages | 63 | 0.2% |
| 31 | Semiconductor Pages | 47 | 0.1% |
| 32 | B2B Pages | 48 | 0.1% |
| 33 | CSR (Corporate Social Responsibility) | 31 | 0.1% |
| 34 | Other/Misc | ~500 | 1.3% |

**Distinct Page Templates Identified: 34**

---

## 2. Consolidated Template Groups (for Development Scope)

After analyzing structural patterns, pages can be consolidated into **15 distinct development templates**:

| Template Group | Constituent Types | Combined Count | Notes |
|---|---|---|---|
| **Product Category/Landing** | Life Science, Industrial, Clinical, EM, Materials Science, Bioprocessing, Chemicals, Semiconductor | 12,466 | Common hero + section + card layout |
| **Form/Lead-Gen** | Form Pages + Confirmation/Thank-You | 12,143 | Form container + hero + sidebar image |
| **Learning Center / Article** | Learning Center, Protocol, Handbook, Newsletter, Tech Support | 3,984 | Long-form content + sidebar nav |
| **Promotional Landing** | Promo Landing + Promo Modal + Cart Modal | 3,671 | Campaign-focused hero + product cards |
| **Event** | Event Pages | 1,322 | Hero + agenda + speakers + registration |
| **Virtual Tour / 3D** | Virtual Tours | 1,329 | 3D viewer + hotspots + product info |
| **Cell Line Database** | Cell Line DB entries | 621 | Structured data + table layout |
| **Technical Reference Library** | Tech Ref Library | 580 | Support docs + getting started/troubleshooting |
| **Brand** | Brand Pages | 526 | Brand hero + product showcase |
| **Blog** | Blog Posts | 304 | Article layout + social + related |
| **Press / News** | Press Releases + News Gallery | 363 | Article + date + media |
| **Services** | Services Pages | 228 | Service description + CTA |
| **About / Corporate** | About Us + CSR | 204 | Custom components (CEO letter, highlights) |
| **Software Download** | Software Downloads | 116 | Download cards + system requirements |
| **B2B / Digital Solutions** | B2B, Digital Solutions, New Ideas | 249 | Specialized landing pages |

---

## 3. Complete Block/Component Inventory

### 3.1 Core AEM Components (cmp-* prefix)

| Block/Component | Purpose | Variants/Modifiers |
|---|---|---|
| **pageheadinghero** | Full-width hero banner with heading, description, CTAs, and background image | `m--dark`, `m--dark m--small-hero` |
| **textimage** | Flexible text + image component (most versatile block) | `m--teaser`, `m--teaser m--teaser-no-border`, `m--teaser-full`, `m--one-third-img`, `m--title-over-img`, `m--text-overlay-dark`, `m--learning-center` |
| **text** | Rich text content block | `m--condensed` |
| **title** | Section/page title | (standard) |
| **image** | Standalone image | (standard) |
| **ctaitem** | Call-to-action button/link | `m--btn-primary`, `m--btn-secondary`, `m--btn-outline`, `m--btn-info`, `m--btn-white`, `m--btn-link`, `m--video`, `m--resource`, `m--icon-reverse`, `m--mini`, `m--small`, `m--large`, `m--block`, `m--center`, `m--left-icon`, `m--lc-cta`, `m--lc-cta-left`, `m--sticky-lc` |
| **container** | Layout container for grid columns | `m--match-height`, `m--no-gutters`, `m--border`, `m--learning-center-container-border`, `container-fluid` |
| **sectioncontainer** | Page section wrapper | `m--indent-l1` |
| **separator** | Visual divider/horizontal rule | (standard) |
| **videoplayer** | Embedded video player | (standard) |
| **experiencefragment** | Reusable content fragment (shared across pages) | (standard) |
| **breadcrumb** | Navigation breadcrumb trail | (standard) |
| **sectiontitle** | Section heading with anchor ID | (standard) |
| **textoverlay** | Text overlay on images/backgrounds | (standard) |
| **ctalist** | List of CTA links | (standard) |
| **manualnav** | Manual sub-navigation component | (standard) |
| **autonavigation** | Auto-generated child page navigation | `child` variant |
| **anchorlist** | In-page anchor/sticky navigation | (standard) |
| **testimonial** | Customer quote/testimonial block | (standard) |

### 3.2 Form Components

| Block/Component | Purpose | Variants |
|---|---|---|
| **form-container** | Wraps entire form | (grid-based layout) |
| **form-input** | Text/email/tel input fields | `m--hideonload` (conditional) |
| **form-options** | Dropdowns, checkboxes, radios | `--drop-down`, `--checkbox`, `--radio`, `m--hideonload` |
| **form-textarea** | Multi-line text input | (standard) |
| **form-hidden** | Hidden form fields (tracking) | (standard) |
| **form-button** | Submit button | (standard) |
| **form-recaptcha** | reCAPTCHA verification | (standard) |
| **form-xfinclusion** | Experience Fragment in form (opt-in, org type, tracking) | `--MSD-Opt-in`, `--msd-mql`, `--msd-standard-form`, `--msd-tracking-codes` |

### 3.3 Specialized/Custom Components

| Block/Component | Purpose | Used On |
|---|---|---|
| **about-hero** | Custom About Us hero with company mission | About Us landing |
| **leadership** | Executive leadership cards/grid | About Us |
| **our-brands** | Brand logo grid/showcase | About Us |
| **ourmission** | Mission statement block | About Us |
| **ceoletter** | CEO letter/message block | CSR pages |
| **csr-commitment** | CSR commitment statement | CSR pages |
| **csr-internaltext** | Internal CSR content block | CSR pages |
| **herotext** | Text-only hero variant | CSR pages |
| **highlights** | Key metrics/highlights grid | CSR pages |
| **endnote** | Page endnotes/footnotes | CSR pages |
| **rte** | Rich text editor (general) | CSR pages |
| **footer-block** | Footer content section | CSR/About pages |
| **header** | Custom page header | CSR pages |

### 3.4 Dynamic/Storefront Components

| Block/Component | Purpose | Used On |
|---|---|---|
| **kmd-card** | Kameleon Design System product card | Product category pages |
| **kmd-dm-card** | Data-managed product card (dynamic) | Product listings |
| **kmd-dm-fbt** | "Frequently Bought Together" widget | Product pages |
| **pragma-toggle-component** | Toggle/expand-collapse interaction | Header, footer, nav |
| **promos** | Promotional content area | Product pages |

---

## 4. Block Variant Details

### 4.1 TextImage Variants (Most-Used Block)

| Variant | Visual Pattern | Used On Templates |
|---|---|---|
| `m--teaser` | Card-style: image top, title, description below | Product, Event, EM pages |
| `m--teaser m--teaser-no-border` | Borderless card variant | Product category pages |
| `m--teaser-full` | Full-width teaser card | Bioprocessing, Product pages |
| `m--one-third-img` | 33% image, 67% text side-by-side | Product, Flow Cytometry |
| `m--title-over-img` | Title overlaid on image | Product, Event, Bioprocessing |
| `m--text-overlay-dark` | Dark text overlay on image | Event, EM product pages |
| `m--learning-center` | Learning center article card | Bioprocessing, Learning Center |

### 4.2 CTA Button Variants

| Variant | Visual Style | Usage Context |
|---|---|---|
| `m--btn-primary` | Solid red/brand-color button | Primary actions (Buy, Contact, Register) |
| `m--btn-secondary` | Solid dark gray button | Secondary actions |
| `m--btn-outline` | White with border | Tertiary actions |
| `m--btn-white` | Transparent with white border | Dark background CTAs (hero) |
| `m--btn-link` | Text link with icon | Inline navigation, "Learn more" |
| `m--btn-info` | Gray/info styled button | Informational actions |
| `m--video` | Video play button (red circle) | Video content triggers |
| `m--resource` | Resource card with border | Document downloads |

### 4.3 Page Hero Variants

| Variant | Layout | Used On |
|---|---|---|
| `m--dark` | Dark background with light text + CTAs | Standard across most pages |
| `m--dark m--small-hero` | Reduced-height dark hero | Bioprocessing, sub-category pages |
| `about-hero` | Custom About Us hero with company video | About Us landing page only |
| `herotext` | Text-only hero (no image) | CSR pages |
| `--hasForegroundImage` | Hero with foreground product image overlay | Cell Line DB, product detail |

---

## 5. Template-to-Block Mapping

| Template | Hero | TextImage | CTA | Form | Container | Video | Navigation | Special |
|---|---|---|---|---|---|---|---|---|
| Product Category | pageheadinghero (dark) | teaser, one-third-img, title-over-img | primary, link, outline | - | match-height | videoplayer | anchorlist, autonavigation | kmd-card |
| Form/Lead-Gen | pageheadinghero (dark) | - | primary (submit) | Full form suite | - | videoplayer | - | form-xfinclusion |
| Learning Center | pageheadinghero (dark/small) | learning-center, teaser-full | lc-cta, sticky-lc, btn-link | - | learning-center-border | - | manualnav | - |
| Promotional Landing | pageheadinghero (dark) | teaser, title-over-img | primary, white | - | match-height | - | - | promos |
| Event | pageheadinghero (dark) | teaser, text-overlay-dark, title-over-img | primary, outline, btn-link | inline form | match-height | - | sectioncontainer | - |
| Virtual Tour | (custom 3D) | - | primary | - | - | - | sectiontitle | 3D viewer/hotspots |
| Cell Line Database | pageheadinghero (foreground) | - | primary, white | - | - | - | breadcrumb, sectiontitle | textoverlay |
| Blog | pageheadinghero (dark) | - | primary | - | - | - | breadcrumb | text (long-form) |
| About/Corporate | about-hero | - | primary, link | - | - | - | - | leadership, our-brands, ourmission |
| CSR | header (custom) | - | - | - | - | - | - | ceoletter, highlights, csr-commitment, endnote |
| Press Release | (minimal) | - | primary | - | - | - | breadcrumb | text (article) |
| Services | pageheadinghero (dark) | teaser | primary | - | match-height | videoplayer | manualnav | - |
| Brand | pageheadinghero (dark) | teaser, title-over-img | primary, link | - | - | - | autonavigation | our-brands |
| Software Download | pageheadinghero (dark) | - | primary (download) | - | - | - | breadcrumb | text |
| Tech Ref Library | pageheadinghero (dark/small) | - | primary | - | - | - | autonavigation | text (structured) |

---

## 6. Development Scope Summary

### Templates to Build: 15
### Total Unique Blocks: 36
### Block Variants: 45+

### Priority Tiers (by volume)

**Tier 1 - High Volume (covers ~72% of pages):**
- Product Category Landing template (12,466 pages)
- Form/Lead-Gen template (12,143 pages)
- Learning Center/Article template (3,984 pages)

**Tier 2 - Medium Volume (covers ~17% of pages):**
- Promotional Landing template (3,671 pages)
- Event template (1,322 pages)
- Virtual Tour template (1,329 pages)
- Clinical Product template (1,129 pages)

**Tier 3 - Low Volume (covers ~11% of pages):**
- Cell Line Database (621 pages)
- Tech Ref Library (580 pages)
- Brand Pages (526 pages)
- Blog (304 pages)
- Protocol/Handbook (1,027 pages)
- Press/News (363 pages)
- About/Corporate/CSR (204 pages)
- Services, Software, B2B, etc. (593 pages)

### Key Architectural Notes

1. **AEM Responsive Grid** - All pages use AEM's 12-column responsive grid system (`aem-Grid--default--12`, `aem-Grid--tablet--12`, `aem-Grid--phone--12`)
2. **Kameleon Design System (kmd-)** - Product catalog cards use a dynamic design system for product data display
3. **Experience Fragments** - Shared content (header, footer, promotional banners) uses AEM Experience Fragments
4. **Form XF Inclusions** - Forms leverage modular Experience Fragments for opt-in, tracking, and organization fields
5. **Anchor Navigation** - Product/category pages use data-anchor-nav for in-page sticky navigation
6. **Spacing System** - Consistent utility classes for margins/padding (`mt-l1` through `mt-l5`, `p-l1` through `p-l5`)
7. **Virtual Tour Pages** - Unique template using 3D viewer technology, may require special handling

---

## 7. Recommended Migration Approach

1. **Start with Tier 1** - Product Category + Form templates cover 72% of site
2. **Shared Components First** - Build hero, textimage (all variants), CTA, container as reusable blocks
3. **Form template** - Standardize on EDS form block patterns for lead-gen
4. **Virtual Tours** - May need custom embed solution or third-party integration
5. **CSR/About** - Custom one-off components, low volume, can be last
6. **Cell Line DB** - Structured data; consider spreadsheet-based approach in EDS
