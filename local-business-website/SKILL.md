---
name: local-business-website
description: Find well-reviewed local service businesses with broken, outdated, non-mobile or missing websites, verify the problem, build an honest mobile-first preview site from their real public info, and prepare a voice note + Loom pitch and pricing for a monthly website service. Use when the user wants to sell websites/hosting to local businesses, find website leads, or build a preview site for a specific business.
---

# Local Business Website Skill

Help a freelancer or small studio find local businesses that deserve a better website, show them a free preview, and offer a fair setup + monthly hosting/maintenance plan, **ethically and legally**.

## Non-negotiable rules
1. **Real data only.** Every name, phone, rating, review count, service, address and hour comes from a public source you actually opened (Google Maps/listing aggregators, directories, the business's own site/socials). Record the source link. If you couldn't verify something, leave it out or mark it `[placeholder]`.
2. **No fake proof.** Never invent reviews, testimonials, awards, years in business, certifications, prices or stats. Don't copy customers' reviews into the preview without the owner's permission. Show only the aggregate rating with its source.
3. **No copyrighted media.** No photos scraped from the business, Google or stock sites without a licence. Use CSS gradients/patterns or clearly marked photo placeholders.
4. **Never claim affiliation.** The preview carries a visible "concept preview by <studio>, not the official site" banner and `noindex`. Never imply you're from Google, their host, or that you already work for them.
5. **The user approves and sends all outreach.** The agent drafts; the human reviews and sends from their own accounts. The agent never contacts businesses, never logs into anything to do so, and never automates bulk messaging.
6. **Respect anti-spam and privacy law** in the user's country (e.g. POPIA + ECTA in South Africa, GDPR/PECR in UK/EU, CAN-SPAM/TCPA in US, CASL in Canada). Use only publicly listed business contact details, identify yourself, include an opt-out, send at most one follow-up, and honour "no" immediately.
7. **Don't publish previews** to public URLs without the user's say-so. Prefer local files, a screen recording, or a private/expiring link.

## Workflow

### 1. Find leads
- Pick an area and 4–8 service niches (plumbers, electricians, locksmiths, garage doors, salons, barbers, panel beaters, mechanics, cleaners, detailers, upholsterers...).
- Search public sources: web search for "<niche> <suburb> reviews", map-listing aggregators, local directories (Yelp, Snupit, Hellopeter, Yellow Pages-type sites).
- Keep businesses with **rating ≥ 4.3 and a meaningful review count** (≈20+; note it if lower). Skip national chains and franchises.

### 2. Verify the website problem (actually fetch it)
For each candidate, open the URL (HTTPS first, then HTTP) and record a concrete, factual problem:
- **Missing:** no website, or listing points to a directory/Facebook page only.
- **Broken:** error page (PHP/DB error, 5xx, DNS error, default server page like IIS/Apache/"coming soon"/"under maintenance").
- **Insecure:** no working HTTPS.
- **Not mobile:** no `<meta name="viewport">`, tiny text, no tap-to-call.
- **Outdated:** very old copyright year, ancient CMS version, Flash/ASP-era page, missing hours/phone.
Note the date you checked. Be prepared for sites to be fixed later; re-check before pitching.

Save `leads.csv` with: `name, niche, area, phone, rating, review_count, current_url, website_problem, source_link, verified_on`.

### 3. Build the preview (best 3–5 leads)
Choose leads with the strongest reviews + clearest problem + a mobile number (for WhatsApp). For each, create `previews/<slug>/index.html` (static, no build step) using `assets/preview-template.html` as a starting point:
- Hero with name, area, one-line value statement from their own wording, the aggregate rating with count.
- **Click-to-call** (`tel:`), **WhatsApp** (`https://wa.me/<intl-number>?text=...`), and a **sticky mobile call bar**.
- Sections: Services (from their site/listing), About (facts only), Contact (address, hours, map link).
- `[placeholder]` highlights for anything unknown (photos, prices, bio).
- Mobile-first, fast, accessible (contrast, 48px tap targets, semantic headings).
- Screenshot at ~390px width (e.g. `google-chrome --headless=new --window-size=390,1800 --screenshot=preview.png file://.../index.html`), check it, and fix layout bugs.

### 4. Pitch kit (`outreach.md`)
- **Voice note (30–45 s):** who you are → genuine compliment (their rating) → the specific website problem → you made a free preview → video coming → easy opt-out.
- **Loom (60–90 s):** current site/problem → why it costs them calls → preview walkthrough (call button, WhatsApp, sticky bar, placeholders) → offer → CTA + opt-out.
- **One text follow-up** 3–4 days later, then stop.
- Personalise each message from the lead row; never mass-send.

### 5. Pricing
Suggest a setup fee + monthly plan in local currency, benchmarked against local web-plan and freelancer prices, e.g. Starter (1 page, hosting, SSL, small updates), Growth (multi-page, SEO basics, form, monthly updates), Pro (booking integration, reporting). Explain the rationale: cost to serve, local willingness to pay, and value of one extra job per month. Offer a no-setup longer-term option.

## Output checklist
- [ ] `leads.csv` with only verified data and source links
- [ ] `previews/<slug>/index.html` + `preview.png` for the top leads
- [ ] `outreach.md` with voice note, Loom script, follow-up, pricing, legal notes
- [ ] Clear summary for the user: top leads and why, anything uncertain, reminder that they send everything themselves
