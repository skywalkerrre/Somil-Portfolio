# Somil Singh — Portfolio


--- FILE: README.md ---


<p align="center">
<img src="./assets/banner.png" alt="Somil Portfolio Banner" style="max-width:100%;height:auto;" />
</p>


# Somil Singh — Personal Portfolio


[![Vercel](https://img.shields.io/badge/deploy-vercel-000000?logo=vercel)](https://vercel.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Made with ❤️](https://img.shields.io/badge/made%20with-%E2%9D%A4-red)](#)


## What this repo contains
A polished, single-page portfolio for **Somil Singh** — responsive, accessible, and deploy-ready. Features:


- Fast, lightweight HTML/CSS/JS template
- Dark / Light mode toggle (persisted to user preference)
- Clean, modern layout inspired by the OnePercent example
- Screenshot banner, badges, and an easy README for Vercel deploy


---


## Demo
Open `index.html` locally or deploy to Vercel for a live URL.


---


## Key files
- `index.html` — main page
- `styles.css` — minimal, modern styling + dark mode variables
- `script.js` — interactivity + theme persistence
- `assets/banner.png` — screenshot / hero banner placeholder
- `README.md` — this file


---


## Features
- Minimal & fast: no frameworks required
- Responsive: mobile-first layout
- Accessible: semantic HTML & proper contrast
- Customizable: easy to personalize with your projects


---


## Quickstart (local)
1. Clone: `git clone https://github.com/<you>/somil-portfolio.git`
2. Open: `cd somil-portfolio && open index.html` (or serve with `npx http-server`)


---


## Deploy to Vercel (recommended)
1. Push repo to GitHub.
2. Sign into Vercel and click "Import Project" → choose your GitHub repo.
3. Use default settings and click "Deploy". Vercel builds and provides a live production URL.


---


## Customization
Edit `index.html` to update name, bio, links, experiences and projects. Replace `assets/banner.png` with a screenshot banner of your site.


---

<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Somil Singh — Portfolio</title>
<link rel="stylesheet" href="styles.css">
<meta name="description" content="Somil Singh — Software Engineer | AI Enthusiast | State-level footballer | Guitarist">
</head>
<body>
<header class="hero">
<div class="container">
<div class="hero-left">
<h1>Somil Singh</h1>
<p class="lead">Software Engineer · AI Enthusiast · State‑level Footballer · Guitarist</p>
<p class="cta">I build scalable frontends, integration tests and clean, maintainable solutions.</p>
<div class="actions">
<a class="btn primary" href="#contact">Hire / Contact</a>
<a class="btn ghost" href="#projects">Projects</a>
</div>
</div>
<div class="hero-right">
<img class="banner" src="assets/banner.png" alt="Somil Portfolio Banner">
</div>
