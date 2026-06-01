# Thermo Fisher Scientific US/EN — Complete Site Scope Analysis

**Site:** thermofisher.com/us/en/home  
**Total URLs Cataloged:** 89,355  
**Estimated Unique Content Pages:** ~61,500 (after exclusions)  
**Date:** 2026-06-01  
**Source CMS:** Adobe Experience Manager (AEM Sites - Classic/Touch UI)  
**Target Platform:** AEM Edge Delivery Services (EDS)

---

## 1. URL Inventory & Distribution

### 1.1 Overall Breakdown

| Pattern Group | URL Count | % of Total | Status |
|---|---|---|---|
| Forms (global/forms/) | 18,763 | 21.0% | Mostly decommissioned (404) |
| Promotions (products-and-services/promotions/) | 13,418 | 15.0% | Active |
| Life Science (life-science/) | 10,594 | 11.9% | Active |
| Industrial (industrial/) | 7,185 | 8.0% | Active |
| Technical Resources (technical-resources/) | 6,902 | 7.7% | Active |
| About Us (about-us/) | 6,832 | 7.6% | Mixed (events active, news migrated) |
| References (references/) | 2,187 | 2.4% | Active |
| Clinical (clinical/) | 1,510 | 1.7% | Active |
| Virtual (virtual/) | 1,337 | 1.5% | Active |
| Brands (brands/) | 729 | 0.8% | Active |
| Electron Microscopy (electron-microscopy/) | 657 | 0.7% | Active |
| Communities/Blog (communities-social/) | 643 | 0.7% | Migrated to WordPress |
| Bioprocessing (bioprocessing/) | 436 | 0.5% | Active |
| Materials Science (materials-science/) | 346 | 0.4% | Active |
| Support (support/) | 324 | 0.4% | Active |
| Digital Solutions (digital-solutions/) | 75 | 0.1% | Active |
| Semiconductors (semiconductors/) | 57 | 0.1% | Active |
| Other (misc, lab-solutions, order, etc.) | ~17,360 | 19.4% | Mixed |

### 1.2 Excluded Pages (not requiring unique templates)

| Category | Count | Reason |
|---|---|---|
| Thank-you/confirmation pages | 11,971 | Simple utility pages, 1 template |
| Cart modal overlays | 2,735 | E-commerce UI components |
| Test/staging pages | 6,984 | Non-production content |
| Duplicate sections (promotions1/2, brands1/2, pcr1, etc.) | 11,451 | Copies of primary content trees |
| **Total excluded** | **33,141** | |

### 1.3 Active Migratable Content

**~56,214 pages** across active sections (after exclusions and platform migrations)

---

## 2. Page Templates Identified

### 2.1 Template Inventory (15 distinct templates)

| # | Template Name | Est. Page Count | Description |
|---|---|---|---|
| 1 | Product Category Landing | ~12,500 | Hub pages: hero + sticky anchor nav + product card grid + left sidebar |
| 2 | Product Sub-Category / Topic | ~20,000 | Deep content: text+image columns, resources, video, related products |
| 3 | Promotional Landing | ~13,418 | Campaign pages: hero + offer cards + CTAs + promo modals |
| 4 | Event Page | ~4,919 | Event hero + agenda accordion + speakers + registration CTA |
| 5 | Learning Center / Article | ~2,300 | Long-form article with sidebar nav + sticky CTA |
| 6 | Technical Resource / App Note | ~1,900 | Document-style with download CTA + related resources |
| 7 | Protocol / Handbook | ~1,030 | Step-by-step procedures with numbered steps + reagent tables |
| 8 | Virtual / 3D Tour | ~1,337 | Chromeless page wrapping Kaon Interactive 3D iframe |
| 9 | Corporate (About Us) | ~200 | Mission, leadership grid, brand showcase, CSR highlights |
| 10 | Brand Microsite | ~530 | Brand-specific hub: brand hero + product categories |
| 11 | Cell Line Database | ~620 | Structured data: properties table + media + ordering info |
| 12 | Services Directory | ~630 | Service listing: category cards + CTA banners |
| 13 | Blog Post | ~640 | Article + author bio + related posts (now WordPress) |
| 14 | Press Release / News | ~360 | Text article + financial tables (now Q4 Inc platform) |
| 15 | Confirmation / Thank-You | ~12,000 | Simple confirmation message (single reusable template) |

### 2.2 Template Consolidation for Development

After analyzing structural patterns, templates share significant block overlap:

| Template Group | Shares Structure With | Unique Elements |
|---|---|---|
| Product Category + Sub-Category | — (base template) | Left sidebar nav, sticky anchor nav |
| Promotional Landing | Product Category | Promo modal, cart-modal |
| Event | — | Accordion (schedule/tracks), event hero |
| Learning Center + App Note + Protocol | Shared "article" layout | Sidebar nav, sticky CTA, step numbering |
| Virtual / 3D Tour | None (chromeless) | Full-screen embed only |
| Corporate | None (bespoke) | Leadership, brands, mission, highlights |
| Blog | — | Author bio, related posts, comments |
| Cell Line Database | — | Structured property tables |

---

## 3. Source-Side AEM Component Inventory

**Total: 38 distinct AEM components with 50+ variants**

### 3.1 Layout & Content Components (17)

| # | AEM Component | Purpose | Variants/Modifiers | Frequency |
|---|---|---|---|---|
| 1 | **pageheadinghero** | Full-width hero banner | `m--dark`, `m--dark m--small-hero`, `--hasForegroundImage` | Very High |
| 2 | **textimage** | Flexible text + image (most used component) | `m--teaser`, `m--teaser-no-border`, `m--teaser-full`, `m--one-third-img`, `m--title-over-img`, `m--text-overlay-dark`, `m--learning-center` | Very High |
| 3 | **text** | Rich text content block | `m--condensed` | Very High |
| 4 | **title** | Section/page title component | (standard) | Very High |
| 5 | **image** | Standalone image | (standard) | High |
| 6 | **ctaitem** | Call-to-action button/link | `m--btn-primary`, `m--btn-secondary`, `m--btn-outline`, `m--btn-info`, `m--btn-white`, `m--btn-link`, `m--video`, `m--resource`, `m--icon-reverse`, `m--mini`, `m--small`, `m--large`, `m--block`, `m--center` | Very High |
| 7 | **ctalist** | List/group of CTA buttons | (standard) | Medium |
| 8 | **container** | Layout container (grid columns) | `m--match-height`, `m--no-gutters`, `m--border`, `m--learning-center-container-border`, `container-fluid` | Very High |
| 9 | **sectioncontainer** | Page section wrapper | `m--indent-l1`, `m--well-blue-light`, `m--well-dark` | Very High |
| 10 | **separator** | Visual divider / horizontal rule | (standard) | High |
| 11 | **videoplayer** | Embedded Brightcove video player | (standard) | Medium |
| 12 | **experiencefragment** | Reusable content fragment | (standard) | Very High |
| 13 | **sectiontitle** | Section heading with anchor ID | (standard) | High |
| 14 | **textoverlay** | Text overlay on images/backgrounds | (standard) | Medium |
| 15 | **testimonial** | Customer quote/testimonial | (standard) | Low |
| 16 | **anchorlist** | In-page sticky anchor navigation | (standard) | Medium |
| 17 | **breadcrumb** | Navigation breadcrumb trail | (standard) | Very High |

### 3.2 Navigation Components (3)

| # | AEM Component | Purpose | Variants | Frequency |
|---|---|---|---|---|
| 18 | **manualnav** | Manual sub-navigation (sidebar) | (standard) | High |
| 19 | **autonavigation** | Auto-generated child page nav | `child` variant | High |
| 20 | **pragma-toggle-component** | Toggle/expand-collapse for nav items | (standard) | High |

### 3.3 Form Components (8)

| # | AEM Component | Purpose | Variants | Frequency |
|---|---|---|---|---|
| 21 | **form-container** | Wraps entire form | (grid-based layout) | Medium |
| 22 | **form-input** | Text/email/tel input fields | `m--hideonload` (conditional visibility) | Medium |
| 23 | **form-options** | Dropdowns, checkboxes, radios | `--drop-down`, `--checkbox`, `--radio`, `m--hideonload` | Medium |
| 24 | **form-textarea** | Multi-line text input | (standard) | Medium |
| 25 | **form-hidden** | Hidden tracking/utm fields | (standard) | Medium |
| 26 | **form-button** | Submit button | (standard) | Medium |
| 27 | **form-recaptcha** | Bot protection | (standard) | Medium |
| 28 | **form-xfinclusion** | Experience Fragment in form | `--MSD-Opt-in`, `--msd-mql`, `--msd-standard-form`, `--msd-tracking-codes` | Medium |

### 3.4 Corporate/Custom Components (7)

| # | AEM Component | Purpose | Used On | Frequency |
|---|---|---|---|---|
| 29 | **about-hero** | Custom About hero with mission video | About Us landing | Very Low |
| 30 | **leadership** | Executive leadership cards/grid | About Us | Very Low |
| 31 | **our-brands** | Brand logo grid/showcase | About Us, Brand pages | Low |
| 32 | **ourmission** | Mission statement block | About Us | Very Low |
| 33 | **ceoletter** | CEO message/letter | CSR pages | Very Low |
| 34 | **csr-commitment** | CSR commitment statement | CSR pages | Very Low |
| 35 | **highlights** | Key metrics/stats grid (number + label) | CSR, About pages | Very Low |

### 3.5 Dynamic/Storefront Components (3)

| # | AEM Component | Purpose | Variants | Frequency |
|---|---|---|---|---|
| 36 | **kmd-card** | Kameleon Design System product card | (data-driven) | High |
| 37 | **kmd-dm-card** | Data-managed dynamic product card | (data-driven) | High |
| 38 | **kmd-dm-fbt** | "Frequently Bought Together" widget | (data-driven) | Medium |

---

## 4. Target EDS Block Architecture

**Total EDS blocks to build: 21 blocks with 47 variants**

### 4.1 Core Content Blocks (8 blocks, 30 variants)

| # | EDS Block | Source AEM Components | Variants | Complexity |
|---|---|---|---|---|
| 1 | **hero** | pageheadinghero, about-hero | 6: promo, category, banner, hub, minimal, event | Medium |
| 2 | **cards** | textimage (teaser variants), kmd-card, leadership, our-brands | 10: product, compact, workflow, resource, callout, category, teaser, icon, team, brand | High |
| 3 | **columns** | textimage (non-teaser), container (multi-col) | 8: intro, product, event, feature, diagnostic, mission, leadership, promo | Medium |
| 4 | **accordion** | pragma-toggle-component, sectioncontainer (collapsible) | 2: event, contact | Medium |
| 5 | **embed** | videoplayer, 3D tour iframe | 2: standard (Brightcove/YouTube), 3dtour (Kaon) | Low |
| 6 | **table** | (custom financial rendering) | 1: financial | Low |
| 7 | **tabs** | anchorlist | 1: jumplinks (sticky anchor nav) | Medium |
| 8 | **fragment** | experiencefragment | 1: standard | Low (framework) |

### 4.2 Specialized Blocks (7 blocks, 10 variants)

| # | EDS Block | Source AEM Components | Variants | Complexity |
|---|---|---|---|---|
| 9 | **form** | form-container + all form-* components | 3: contact, lead-gen, survey | High |
| 10 | **testimonial** | testimonial | 2: quote, video-quote | Low |
| 11 | **highlights** | highlights | 2: stats-grid, key-metrics | Medium |
| 12 | **text-overlay** | textoverlay, textimage (m--text-overlay-dark) | 1: dark-overlay | Low |
| 13 | **cta-banner** | ctaitem (m--block), ctalist | 2: primary, secondary | Low |
| 14 | **product-card** | kmd-card, kmd-dm-card, kmd-dm-fbt | 3: standard, dynamic, fbt | High |
| 15 | **download** | ctaitem (m--resource) | 1: resource-download | Low |

### 4.3 Navigation/Chrome Blocks (4 blocks, 5 variants)

| # | EDS Block | Source AEM Components | Variants | Complexity |
|---|---|---|---|---|
| 16 | **header** | (global header/mega-nav) | 1: mega-nav | High |
| 17 | **footer** | (global footer) | 1: standard | Medium |
| 18 | **sidebar-nav** | manualnav, autonavigation | 2: manual, auto-taxonomy | Medium |
| 19 | **breadcrumb** | breadcrumb | 1: standard | Low |

### 4.4 Template-Specific Blocks (2 blocks, 2 variants)

| # | EDS Block | Source AEM Components | Variants | Complexity |
|---|---|---|---|---|
| 20 | **cell-line-table** | (structured data rendering) | 1: properties | Medium |
| 21 | **step-list** | text (numbered protocol steps) | 1: protocol | Low |

---

## 5. Template → Block Mapping (Comprehensive)

### 5.1 Product Category Landing (~12,500 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-promo, hero-banner | 2-3 |
| cards | cards-product, cards-compact, cards-workflow, cards-resource, cards-callout | 5-7 |
| columns | columns-intro | 1 |
| tabs | tabs-jumplinks | 1 |
| embed | standard (Brightcove) | 0-1 |
| sidebar-nav | auto-taxonomy | 1 |
| breadcrumb | standard | 1 |
| fragment | standard | 1-2 |
| product-card | dynamic | 0-4 |
| cta-banner | primary | 1-2 |

### 5.2 Product Sub-Category / Topic (~20,000 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-category | 1 |
| cards | cards-resource, cards-product | 2-4 |
| columns | columns-product | 2-5 |
| tabs | tabs-jumplinks | 0-1 |
| embed | standard (Brightcove) | 0-2 |
| sidebar-nav | auto-taxonomy | 1 |
| breadcrumb | standard | 1 |
| testimonial | quote | 0-1 |
| fragment | standard | 1-2 |

### 5.3 Promotional Landing (~13,418 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-promo | 1 |
| cards | cards-product, cards-teaser | 2-4 |
| columns | columns-feature, columns-promo | 1-3 |
| form | lead-gen | 0-1 |
| cta-banner | primary, secondary | 1-2 |
| fragment | standard | 1-2 |

### 5.4 Event Page (~4,919 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-event | 1 |
| accordion | accordion-event | 2-3 |
| columns | columns-event | 1-2 |
| embed | standard (Brightcove) | 0-1 |
| form | lead-gen (registration) | 0-1 |
| fragment | standard | 1 |

### 5.5 Learning Center / Article (~2,300 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-category (small) | 1 |
| columns | columns-product | 1-3 |
| cards | cards-resource | 1-2 |
| sidebar-nav | manual | 1 |
| embed | standard | 0-1 |
| cta-banner | primary (sticky) | 1 |
| breadcrumb | standard | 1 |
| fragment | standard | 1-2 |

### 5.6 Technical Resource / App Note (~1,900 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-category | 1 |
| cards | cards-resource | 1-2 |
| columns | columns-product | 0-2 |
| download | resource-download | 1-3 |
| breadcrumb | standard | 1 |
| fragment | standard | 1 |

### 5.7 Protocol / Handbook (~1,030 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| step-list | protocol | 1-3 |
| table | financial (data tables) | 0-2 |
| sidebar-nav | manual | 1 |
| breadcrumb | standard | 1 |
| fragment | standard | 1 |

### 5.8 Virtual / 3D Tour (~1,337 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| embed | embed-3dtour (full-screen Kaon) | 1 |

### 5.9 Corporate / About Us (~200 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-minimal | 1 |
| cards | cards-team, cards-brand | 2-3 |
| columns | columns-mission, columns-leadership | 2-3 |
| highlights | stats-grid | 0-1 |
| fragment | standard | 1 |

### 5.10 Brand Microsite (~530 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-promo | 1 |
| cards | cards-product, cards-teaser | 2-4 |
| sidebar-nav | auto-taxonomy | 1 |
| breadcrumb | standard | 1 |
| fragment | standard | 1 |

### 5.11 Cell Line Database (~620 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-category (foreground image) | 1 |
| cell-line-table | properties | 1 |
| text-overlay | dark-overlay | 0-1 |
| product-card | standard | 1-2 |
| breadcrumb | standard | 1 |

### 5.12 Services Directory (~630 pages)

| Block | Variants Used | Instances/Page |
|---|---|---|
| hero | hero-minimal | 1 |
| cards | cards-category | 1-2 |
| columns | columns-promo | 1-2 |
| cta-banner | primary | 1 |
| fragment | standard | 1 |

---

## 6. Design System & Content Patterns

### 6.1 AEM Source Architecture

| Pattern | Details |
|---|---|
| Grid System | 12-column responsive: `aem-Grid--default--12`, `aem-Grid--tablet--12`, `aem-Grid--phone--12` |
| Spacing System | Utility classes: `mt-l1` through `mt-l5`, `p-l1` through `p-l5` |
| Color Wells | Section backgrounds: `well-blue-light`, `well-dark`, `well-grey` |
| Dynamic Cards | Kameleon Design System (kmd-*) for product catalog rendering |
| Fragments | Experience Fragments for shared: header, footer, promotional banners |
| Anchor Nav | Data attribute `data-anchor-nav` for in-page sticky navigation |
| Forms | Marketo-integrated lead-gen forms with conditional field visibility |

### 6.2 Key Visual Patterns

1. **Cards-first design** — The `textimage` component with teaser variants is the most-used component across the entire site. Maps to 10+ card variants in EDS.
2. **Hero + Sticky Anchor Nav + Sectioned Cards** — Standard product page pattern used by ~35,000 pages
3. **Section colored backgrounds** — Light blue "wells" and dark navy sections create visual rhythm
4. **Dual CTA pattern** — Primary (solid brand red) + Secondary (outline/link with arrow icon)
5. **Mondrian promotional tiles** — Side-by-side offer cards with background images + text overlay
6. **Left sidebar taxonomy nav** — Persistent on all product/category pages, auto-generated from page tree
7. **Product data cards** — Dynamic kmd-* cards powered by product catalog API, not static content

### 6.3 Third-Party Integrations

| Platform | Usage | Integration Type |
|---|---|---|
| Brightcove | Video hosting (all video content site-wide) | Embed (player.js) |
| Kaon Interactive | 3D product tours (virtual pages) | Full-screen iframe |
| Marketo | Form submissions and lead routing | Form action endpoints |
| Google reCAPTCHA | Bot protection on forms | JavaScript widget |
| Kameleon (kmd) | Dynamic product catalog cards | Client-side JS + API |
| Adobe Target | Personalization / A/B testing | AT.js |
| Adobe Analytics | Tracking | AppMeasurement/alloy.js |

### 6.4 Platform Migrations Already Completed

| Content Type | Migrated To | Pages Affected | Impact on Scope |
|---|---|---|---|
| Blog | WordPress (thermofisher.com/blog/) | ~643 | OUT OF SCOPE |
| Press Releases | Q4 Inc (newsroom.thermofisher.com) | ~1,574 | OUT OF SCOPE |
| Forms (global/forms/) | Decommissioned | ~18,763 | OUT OF SCOPE (404) |
| Contact/Support | React app (store/v2/contact-us) | Unknown | OUT OF SCOPE (redirect) |

---

## 7. Development Scope Summary

### 7.1 Blocks to Build

| Category | Block Count | Variant Count | Complexity | Effort (days) |
|---|---|---|---|---|
| Core Content (hero, cards, columns, accordion, embed, table, tabs, fragment) | 8 | 30 | High | 18-22 |
| Specialized (form, testimonial, highlights, text-overlay, cta-banner, product-card, download) | 7 | 14 | Medium | 10-14 |
| Navigation/Chrome (header, footer, sidebar-nav, breadcrumb) | 4 | 5 | High | 8-12 |
| Template-Specific (cell-line-table, step-list) | 2 | 2 | Low | 2-3 |
| **TOTAL** | **21 blocks** | **51 variants** | | **38-51 days** |

### 7.2 Additional Development Work

| Item | Effort (days) |
|---|---|
| Page templates / content models (15 templates) | 5-7 |
| Design tokens & global styles (typography, colors, spacing) | 3-4 |
| Section metadata configurations (wells, backgrounds) | 1-2 |
| Dynamic product card integration (kmd-* replacement) | 5-8 |
| Third-party integrations (Brightcove, Kaon, reCAPTCHA) | 3-5 |
| Import infrastructure (parsers, transformers for content migration) | 8-12 |
| Testing & QA (cross-browser, accessibility, performance) | 7-10 |
| **TOTAL** | **32-48 days** |

### 7.3 Grand Total Estimated Effort

| Phase | Effort |
|---|---|
| Block development (21 blocks, 51 variants) | 38-51 days |
| Templates, styles, integrations, infrastructure | 32-48 days |
| **Total project effort** | **70-99 days** |
| **With 2-person team** | **35-50 days** |

---

## 8. Migration Priority Recommendation

### Phase 1 — Foundation (covers ~70% of active pages)
**Blocks:** hero (6), cards (6 of 10), columns (4 of 8), tabs, sidebar-nav, breadcrumb, fragment, cta-banner  
**Templates:** Product Category Landing, Product Sub-Category/Topic, Promotional Landing  
**Effort:** ~30-40 days

### Phase 2 — Expansion (covers ~20% more)
**Blocks:** accordion (2), embed (2), cards (+4 remaining), columns (+4 remaining), form, download  
**Templates:** Event, Learning Center, Technical Resource, Services Directory, Brand Microsite  
**Effort:** ~20-30 days

### Phase 3 — Specialized (remaining ~10%)
**Blocks:** testimonial, highlights, text-overlay, product-card, cell-line-table, step-list, table  
**Templates:** Corporate, Protocol/Handbook, Virtual/3D Tour, Cell Line Database  
**Effort:** ~15-25 days

### Out of Scope
- Blog (WordPress — separate platform)
- Press Releases (Q4 Inc — separate platform)
- Forms/global/forms/ (decommissioned — all 404)
- Contact/Support (React SPA — redirect)
- Thank-you/confirmation pages (trivial single template, migrate last)

---

## 9. Risk Factors & Considerations

| Risk | Impact | Mitigation |
|---|---|---|
| Dynamic product cards (kmd-*) require API integration | High | May need custom EDS block with fetch() to product catalog API |
| Kameleon Design System is proprietary | Medium | Must reverse-engineer card rendering or find replacement |
| 89K URLs includes significant dead content | Low | Pre-filter with HTTP status checks before migration |
| Left sidebar nav is taxonomy-driven | Medium | Build auto-navigation block reading from page index |
| Personalization (Adobe Target) content | Medium | Decide: drop personalization or implement EDS experimentation |
| Form submissions routed to Marketo | Medium | Need Marketo endpoint mapping for any active forms |
| Brightcove video IDs may change | Low | Verify video availability during content migration |

---

## Appendix A: Pages Analyzed During This Assessment

| Template Type | URL Analyzed | Key Findings |
|---|---|---|
| Product Category Landing | /life-science/pcr.html | 14 sections, 8 block variants, cards-dominant |
| Product Sub-Category/Topic | /life-science/pcr/real-time-pcr.html | 10 sections, 5 card variants, columns for product detail |
| Event | /events/asms.html (ASMS 2026) | 8 sections, 3 accordions (25 items), columns+video |
| Clinical / Diagnostic | /clinical/diagnostic-testing.html | 7 sections, columns-dominant, colored wells |
| Electron Microscopy Products | /electron-microscopy/products.html | 11 sections, repeating columns-product pattern |
| Corporate (About Us) | corporate.thermofisher.com/about.html | 4 sections, bespoke (mission, leadership, brands) |
| Services Directory | /products-and-services/services.html | 5 sections, cards-category grid, minimal blocks |
| Bioprocessing Hub | /life-science/bioproduction.html | 8 sections, cards-teaser + cards-icon patterns |
| Virtual / 3D Tour | /virtual/1500-series-biosafety-cabinet-3d-tour.html | Chromeless, single full-screen Kaon embed |
| Blog Post | thermofisher.com/blog/ (WordPress) | WordPress platform, 9 sections, text-heavy |
| Press Release | newsroom.thermofisher.com | Q4 Inc platform, financial tables |
| Forms / Contact | Redirects to /store/v2/contact-us | Decommissioned, accordion-based routing |

## Appendix B: Block Variant Quick Reference

| Base Block | All Variants |
|---|---|
| hero | promo, category, banner, hub, minimal, event |
| cards | product, compact, workflow, resource, callout, category, teaser, icon, team, brand |
| columns | intro, product, event, feature, diagnostic, mission, leadership, promo |
| accordion | event, contact |
| embed | standard (Brightcove/YouTube), 3dtour (Kaon) |
| table | financial |
| tabs | jumplinks |
| fragment | standard |
| form | contact, lead-gen, survey |
| testimonial | quote, video-quote |
| highlights | stats-grid, key-metrics |
| text-overlay | dark-overlay |
| cta-banner | primary, secondary |
| product-card | standard, dynamic, fbt |
| download | resource-download |
| header | mega-nav |
| footer | standard |
| sidebar-nav | manual, auto-taxonomy |
| breadcrumb | standard |
| cell-line-table | properties |
| step-list | protocol |
