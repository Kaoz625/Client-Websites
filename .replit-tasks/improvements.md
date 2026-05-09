# Replit Agent Task: Client-Websites

## Goal
Modernize and standardize the Client-Websites repository — which currently contains a portfolio hub (index.html) and individual client site HTML files (cpainting.html, titan.html) plus preview files — by establishing a consistent design system and upgrading each client page to modern standards.

## Tasks
1. **Audit all files**: read index.html, cpainting.html, titan.html, and all *-preview.html files; document what each contains (is it a full site? a component? a placeholder?); the storybook/ dir may contain design tokens — read it
2. **Create a shared design system file** (`shared/design-system.css`): CSS custom properties for colors, typography, spacing, and border-radius that all client pages import; use a professional neutral palette with gold accent (#C9A84C) as the brand color for NYC Tailblazers work
3. **Standardize cpainting.html**: apply the shared design system, ensure it matches the live CPaintingServices site structure (hero, services, gallery, contact), add missing SEO meta tags, fix any broken layout issues
4. **Standardize titan.html**: same treatment — apply shared CSS variables, ensure it has all required sections (hero, services, gallery, estimate form CTA), add LocalBusiness schema JSON-LD
5. **Preview files** (claritycoachingpro-preview.html, luxeandcohair-preview.html, peakprohvac-preview.html): for each, add a consistent preview banner at the top ("NYC Tailblazers — Client Preview — [Site Name]") with client name, preview date, and a "View Live Site" button; use the shared design system
6. **Update index.html** (the portfolio hub): ensure it lists ALL client sites found in this repo with accurate descriptions and working links; add a "Standardized" badge to sites that now use the shared design system; the existing dark theme is good — keep it
7. **Add a `storybook/` component showcase** if not already present: a simple HTML page listing all reusable components (nav, hero, card, form, footer) with live previews and the CSS variable values used — acts as a visual style guide for the team
8. **README update**: document the folder structure, how to add a new client site (copy template, import shared CSS, fill in content), and the deploy workflow (push to main → Cloudflare Pages picks it up)
9. Ensure all HTML files pass basic validation (no unclosed tags, all images have alt attributes, forms have labels)
10. Add a `_headers` file for Cloudflare Pages with security headers (X-Frame-Options, Content-Security-Policy basic, X-Content-Type-Options)

## Tech Stack
- Vanilla HTML5 / CSS3 / JavaScript (repository standard — no build tool)
- Shared CSS custom properties design system
- No external JS libraries (inline scripts only if needed)

## Deploy Target
Cloudflare Pages (static). Never Vercel.

## Done When
- [ ] `shared/design-system.css` exists with full set of CSS custom properties
- [ ] cpainting.html and titan.html import shared CSS and look polished
- [ ] All *-preview.html files have the preview banner with "View Live Site" link
- [ ] index.html portfolio hub lists all client files with correct links
- [ ] `storybook/` contains a visual component guide
- [ ] `_headers` file with security headers present
- [ ] README documents folder structure and "add new client" workflow
- [ ] No broken links or missing alt attributes across all HTML files
