---
title: Jan Lebar — Web Developer
theme: league
transition: slide
css: presentation.css
---

<!-- .slide: class="title-slide centered" -->
# <span class="icon-blue"></span> Jan Lebar
## Web Developer

<div style="margin-top: 2em; font-size: 1.3em; color: #bdc3c7; font-style: italic;">
Graphic Designer & Developer — Application for Viaduct
</div>


---

## <span class="icon-blue"></span> About Me

<div class="highlight-box">
<strong>Graphic designer and developer</strong> with a passion for modern technologies, web application development, and optimization.
</div>

- <span class="icon-blue"></span> Experience in both <b>front-end and back-end</b> development
- <span class="icon-blue"></span> Working with Python, Flask, FastAPI, Next.js, React, Vue.js and other modern web technologies
- <span class="icon-blue"></span> A combination of <b>technical and design skills</b> for a valuable contribution to your team

### Education
- <span class="icon-green"></span> Faculty of Natural Sciences
- <span class="icon-green"></span> Master's degree — Liverpool, United Kingdom

---

## <span class="icon-blue"></span> Why Viaduct

<div class="highlight-box">
Viaduct is growing rapidly in the <b>connected vehicle space</b> — at the forefront of connected cars and AI.
</div>

- <span class="icon-blue"></span> World's leading end-to-end <b>machine learning and data analytics</b> platform for connected vehicle data
- <span class="icon-blue"></span> Helping major vehicle manufacturers make smarter decisions for vehicles and fleets
- <span class="icon-blue"></span> Recently acquired by <b>Sumitomo Rubber Industries (SRI)</b>
- <span class="icon-blue"></span> Core stack: AWS, Go, Python, SQL · Amazon RDS, Postgres, ClickHouse · REST APIs · HTML, JavaScript, TypeScript, CSS

---

## <span class="icon-blue"></span> Key Skills — Web & Frameworks

<div class="feature-grid">

<div class="feature-card">
<h3><span class="icon-blue"></span> Web Technologies</h3>
HTML, CSS, JavaScript
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Programming & Frameworks</h3>
Python, Flask, FastAPI, React, Next.js, Angular, Vue.js, Nuxt
</div>

</div>

---

## <span class="icon-blue"></span> Key Skills — Backend & Data

<div class="feature-grid">

<div class="feature-card">
<h3><span class="icon-blue"></span> Backend & APIs</h3>
Web application and API development using Python, Flask, and FastAPI
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> Databases</h3>
SQL, PostgreSQL, SQLite, and SQLAlchemy
</div>

</div>

---

## <span class="icon-blue"></span> Key Skills — SEO & AI

<div class="feature-grid">

<div class="feature-card">
<h3><span class="icon-blue"></span> SEO & Optimization</h3>
Basic and technical SEO, web application optimization, and vector databases for Slovenian-language content
</div>

<div class="feature-card">
<h3><span class="icon-blue"></span> AI & Data</h3>
AI integration, data processing, and web scraping using Python and Cheerio
</div>

</div>

---

## <span class="icon-blue"></span> Project — Handyman Platform

A web platform connecting <b>service providers and customers</b> through a user-friendly application.

- <span class="icon-blue"></span> <b>Backend:</b> Python, Flask
- <span class="icon-blue"></span> <b>ORM:</b> SQLAlchemy
- <span class="icon-blue"></span> <b>Database:</b> PostgreSQL
- <span class="icon-blue"></span> <b>CSS:</b> Tailwind CSS
- <span class="icon-blue"></span> <b>Security:</b> UUID4 and ItsDangerous
- <span class="icon-blue"></span> <b>Platform:</b> Fly.io
- <span class="icon-green"></span> Includes vector-based functionality for Slovenian-language content

---

## <span class="icon-blue"></span> Project — Side-Effect

A React/Next.js application for visualizing information about <b>medication side effects</b>.

- <span class="icon-blue"></span> <b>Frontend:</b> React, Next.js, Tailwind CSS
- <span class="icon-blue"></span> <b>Data Visualization:</b> Chart.js
- <span class="icon-blue"></span> <b>Web Scraping:</b> Cheerio and Python
- <span class="icon-blue"></span> <b>Database:</b> SQLite
- <span class="icon-blue"></span> <b>AI:</b> Gemini 2.0 Flash
- <span class="icon-blue"></span> <b>Platform:</b> AWS Amplify
- <span class="icon-green"></span> Python scripts collect and process data — works with local SQLite and external websites

---

## <span class="icon-blue"></span> Project — Portfolio Website

<div class="highlight-box">
A portfolio website built with <b>Vue.js</b> and <b>Nuxt</b>.
</div>

---

## <span class="icon-blue"></span> What I Bring

- <span class="icon-blue"></span> A strong background in <b>graphic design</b>, problem-solving, and communication
- <span class="icon-blue"></span> Development approached through <b>user experience</b> and <b>visual design</b>
- <span class="icon-blue"></span> Continuously expanding knowledge of modern web development
- <span class="icon-green"></span> Python, FastAPI, APIs, databases, AI integration, and web application optimization

---

## <span class="icon-blue"></span> Let's Talk

<div class="highlight-box">
I would welcome the opportunity to discuss my experience and projects in more detail.
</div>

- <span class="icon-blue"></span> <b>Phone:</b> +386 31 581 040
- <span class="icon-blue"></span> <b>Email:</b> janstefanlebar@gmail.com
- <span class="icon-blue"></span> <b>Portfolio & CV</b> available on request

<div style="margin-top: 1em; text-align: center; color: #95a5a6; font-style: italic;">
Thank you — Jan Lebar, Web Developer
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
