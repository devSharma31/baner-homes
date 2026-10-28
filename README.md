# Baner Homes by Rohan — real estate landing page (concept)

A mobile-first landing page for a fictional independent property agent in Baner–Balewadi, Pune, handling rentals and resale flats. It's built around one action: **share your budget, BHK and move-in date in a short form that opens WhatsApp with those details filled in.**

**Live:** [baner-homes.vercel.app](https://baner-homes.vercel.app) · [GitHub Pages](https://devsharma31.github.io/baner-homes/)

> Concept project for my design portfolio. The agent, listings, prices, ratings, MahaRERA number and phone number are fictional or placeholders, and the reviews are labelled as samples.

---

## The brief

| | |
|---|---|
| **Business** | Independent agent: rentals and resale flats |
| **Customers** | IT professionals relocating to Pune; young couples buying a first flat |
| **Goal** | Submit a short requirement form that opens WhatsApp with the details prefilled |
| **Price level** | Premium service, fee shown upfront |
| **Brand feel** | Trustworthy, modern, straightforward |

## The real problems, and how the page solves them

Real estate has the biggest trust gap of the three projects, so **trust carries this page.**

| Problem | Fix on the page |
|---|---|
| **People expect hidden broker fees** | The fee comes right after the hero, before any flats: renting is 15 days' rent + GST, paid only after signing; buying is 1% + GST. A dark "What I never charge" box rules out registration fees, visit charges and token money handled by the agent. |
| **People expect fake listings** | Every flat card shows a **"Verified [date]" badge** and what was checked (owner ID, society NOC, title documents). A "wasted-visit promise" takes ₹1,000 off the fee if a flat is already gone. A MahaRERA box invites visitors to check the registration number themselves. |
| **The agent gets vague enquiries with no budget or timeline** | The hero form requires budget and move-in date, with budget ranges that switch between rent and buy. Each flat's "Ask about this flat" button attaches that listing's reference number. Rohan gets a complete brief in one message. |

## Design decisions

- **Section order:** requirement form (hero) → *what will it cost?* (fees) → *are the listings real?* (verified flats + area snapshot) → 3 steps → four written promises and MahaRERA → reviews → office hours → FAQ → final CTA.
- **Colour:** cool off-white `#F5F7FA` with navy `#0F1B2D` text (16.6:1). **Blue `#1E4FD8` is used only on buttons** (6.4:1). Green is reserved for "verified" badges.
- **Type:** Manrope for headings and Inter for body text, for a clean fintech feel that says modern and no-nonsense rather than flashy property ads.
- **For people relocating from another city:** a ₹4,999 remote shortlist (live video walkthroughs and a commute check), deducted from the final fee.

## Conversion review (second pass)

I reviewed the first version from two sides: a busy customer on a phone with a slow connection, and the agent who wants better leads.

| Issue found | Change |
|---|---|
| Main CTA was **far below the fold** (ended at 1,322px on a 375×667 screen) | Removed badges, shortened the headline, cut the Area and Name fields (WhatsApp already shows the name), and moved the trust line under the button. **The button now ends at 567px.** |
| "Find me on" cards linked to 99acres and MagicBricks, which are full of competing agents | Turned into non-clickable rating badges; only Google reviews stay clickable |
| Google Fonts blocked the first paint on slow connections | Fonts load in the background; the hero photo now loads only when it's near the screen |
| Generic copy ("The opposite of the broker experience you're expecting") | Replaced with specific lines ("Four promises, in writing") |

## Accessibility and performance

- Semantic HTML, labelled fields, inline error messages linked to their fields (`aria-describedby`, `aria-invalid`), visible focus ring
- All text passes WCAG AA contrast
- Images below the fold are lazy-loaded, with styled fallbacks if an image fails
- No frameworks: one HTML file with inline CSS and vanilla JavaScript
- SEO: meta description, Open Graph tags, and `RealEstateAgent` JSON-LD structured data

## What I'd test next with real customers

1. **Fee shown upfront.** Does it bring fewer enquiries but more signed deals?
2. **Required vs optional budget.** Which gets more people to finish the form, and which gives better leads?
3. **The ₹4,999 remote shortlist vs a free first video call** for people moving from another city.

## Stack

HTML · CSS · vanilla JavaScript · Google Fonts · Unsplash photos · Simple Icons (CC0) · deployed on GitHub Pages and Vercel

## How this was built

I built this with Claude (Anthropic's AI assistant) as a design and coding partner.

**My part:** I wrote the business brief, chose to put trust signals (an upfront fee, verified listings, the MahaRERA box) at the centre, reviewed every version, commissioned the conversion review above, and published the site to GitHub and Vercel.

**Claude's part:** it wrote the HTML, CSS, JavaScript and copy to that brief.

---

Concept design by Devashish Sharma. Fictional business.
