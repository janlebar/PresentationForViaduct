---
title: Expanding the Real Estate App
theme: league
transition: slide
css: presentation.css
---

<!-- .slide: class="title-slide centered" -->
# <span class="icon-blue"></span> Expanding the Real Estate App
## From Land Registry Search to include Rental Platform

<div style="margin-top: 2em; font-size: 1.3em; color: #bdc3c7; font-style: italic;">
Building a Trusted Rental Ecosystem
</div>


---
## <span class="icon-blue"></span> Why expand?

1. To increase platform traffic which is necessary for real estate agencies to advertise.
2. Real problem: Property owners do not wish to rent out because they cannot see who is applying to rent and have issues with previous rental agreements.

---

## <span class="icon-blue"></span> Proposed Platform Expansion

<div class="highlight-box">
<strong>Goal:</strong> Extend from a <b>property lookup tool</b> into a <b>trusted rental ecosystem</b>
</div>

### Key Features:

<div style="color: #ecf0f1; margin-top: 0.2em; font-size: 0.9em;">
- <span class="icon-blue"></span> Enable <b>both renters and landlords</b> to create accounts
- <span class="icon-blue"></span> Allow them to <b>interact, rate experiences, and build trust</b>
- <span class="icon-blue"></span> Create transparency in the rental market
</div>

---

## <span class="icon-blue"></span> User Roles

<div class="two-column">

<div class="feature-card">
<h3><span class="icon-blue"></span> Renters</h3>
- People looking to rent apartments or houses
- Can create profiles and verify identity
- Can review rental experiences
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Landlords (Rentees)</h3>
- Property owners offering rental units
- Can manage property listings
- Can review renters after agreements
</div>

</div>

---

## <span class="icon-blue"></span> Authentication and Verification

<div class="highlight-box">
<strong>Goal:</strong> Improve trust and reduce fraud
</div>

### Facebook Integration

<div style="color: #ecf0f1; margin-top: 0.2em; font-size: 0.9em;">
- <span class="icon-green"></span> Implement <b>Facebook login authentication</b>
- <span class="icon-green"></span> Verify user identity
- <span class="icon-green"></span> Import profile photos for identification
- <span class="icon-blue"></span> Helps reduce <b>fake profiles and scams</b>
</div>

---

## <span class="icon-blue">★</span> Reputation System

<div class="centered" style="margin: 0.3em 0;">
<h2 style="border: none; color: #3498db; font-size: 1.6em;">Two-Way Reputation System</h2>
<p style="font-size: 1em; color: #ecf0f1;">Building transparency through mutual feedback</p>
</div>

---

## <span class="icon-blue"></span> Landlord → Renter Feedback

<div class="feature-grid">

<div class="feature-card">
<h3><span class="icon-blue"></span> Payment Reliability</h3>
Track payment history and consistency
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Property Care</h3>
Monitor how renters maintain properties
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Communication</h3>
Assess responsiveness and clarity
</div>

</div>

---

## <span class="icon-blue"></span> Renter → Landlord Feedback

<div class="feature-grid">

<div class="feature-card">
<h3><span class="icon-blue"></span> Property Condition</h3>
Rate the quality and maintenance of properties
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Contract Fairness</h3>
Evaluate the fairness of rental agreements
</div>

</div>

---

## <span class="icon-blue"></span> Reputation System Benefits

<div class="benefit-list">

- <span class="icon-green"></span> Creates <b>transparency</b> in the rental market
- <span class="icon-green"></span> Encourages <b>responsible behavior</b> from both sides
- <span class="icon-green"></span> Helps users make <b>safer rental decisions</b>
- <span class="icon-green"></span> Builds long-term <b>trust and credibility</b>

</div>

---

## <span class="icon-blue"></span> Long-Term Vision

<div class="highlight-box">
The platform could evolve into a <b>trusted Slovenian rental network</b>
</div>

### Users can:

<div class="two-column" style="margin-top: 0.2em; font-size: 0.9em;">

- <span class="icon-blue"></span> Search properties
- <span class="icon-green"></span> Verify landlords and renters
- <span class="icon-blue"></span> Review past experiences
- <span class="icon-blue"></span> Build trustworthy rental histories

</div>

---

## <span class="icon-blue"></span> Behandier Specification

<div class="spec-table">

| Layer | Technology |
| --- | --- |
| Edge / CDN | Cloudflare — proxied A records, origin cert for Full (strict) |
| Load balancing / proxy | Traefik v3.7.6 (host binary, Go 1.25) |
| App server | Next.js 15 (App Router) + React 19, TypeScript, Node.js 20, next start on :3000, systemd unit nextjs-app |
| Database | PostgreSQL 18-alpine (Docker, docker-compose.yml, port 5432, volume pgdata) |
| ORM | Prisma 6 |
| Auth | Better Auth (auth.ts, middleware.ts) + JWT, OAuth (Google/Facebook), Expo plugin for mobile |
| Payments | Stripe (checkout + webhooks at app/api/stripe/*) |
| Email | Mailgun (lib/mail.ts) |
| Storage | S3 / Wasabi / Vercel Blob (STORAGE_PROVIDER) |
| i18n | next-intl (i18n/, messages/) |
| UI | Tailwind 4, Radix UI, Leaflet maps, jotai |
| Mobile | Expo integration (Expo_integration/), hits /api/mobile/* |
| Health check | GET /api/mobile/health — no auth/DB, returns {ok: true} (good Traefik LB healthCheck target) |
| Testing/tooling | Jest, ESLint, oxfmt |

</div>