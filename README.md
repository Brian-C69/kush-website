# KUSH — Kumpulan Usahawan Landing Page

## Overview

This repo contains the single–page marketing site for **KUSH (Kumpulan Usahawan)**, a founder‑first entrepreneur community facilitated by Rafi Ansari. The page is designed to clearly explain what KUSH is, who it’s for, how it works, and how to join – with a strong focus on readability, mobile UX, and low‑friction registration.

There is no build step or framework; the site is a **static HTML/CSS/JS** page intended to be dropped into any PHP/XAMPP or generic web hosting environment. All styling and behavior live in `index.html`, with a small image folder under `assets/`.

## What Problems Does It Solve?

KUSH as a community is built to solve a specific set of problems for founders, and this site is structured around those problems:

- **Lack of clarity in business direction** – Sections like “What is KUSH?”, “Why founders join KUSH” and “How KUSH works” explicitly frame KUSH as a clarity‑first space, making it easy for overwhelmed founders to understand what they can expect.
- **Distrust of hype‑driven coaching funnels** – The copy emphasizes “no upsell, no glamour” and “business coach, not influencer”, positioning KUSH as an alternative to high‑pressure, upsell‑heavy ecosystems.
- **Difficulty finding a serious peer network** – Chapters, events and “Chill With Coach” sessions highlight that KUSH is built around real conversations and peer learning rather than just content consumption.
- **Confusion about how to get started** – The “How KUSH works” and “Register for KUSH” sections break down the onboarding flow into clear steps, so a first‑time visitor knows exactly what to do next.
- **Language accessibility for Malaysian founders** – A built‑in EN/BM language toggle lets visitors switch between English and Malay copy without reloading, so the same link can serve mixed‑language audiences.
- **Mobile‑first access** – Responsive layout, a burger navigation menu, and a floating “back to top” button make the site easy to use on phones (where most founders will likely discover it).

## Key Features

- **Hero section** that communicates KUSH’s core promise (“We build beyond boundaries”) and main benefits at a glance.
- **About & Benefits cards** with Font Awesome icons, describing community‑first culture, clarity, support network, and funding readiness.
- **Chapters & locations** list showing current and future hubs (Johor Bahru, KL/Bangsar, Cyberjaya, etc.).
- **How It Works steps** that walk through: join list → attend sessions → apply & grow.
- **Coach profile** for Rafi Ansari with real‑world case study framing (e.g., Straits Cattle Trading Co).
- **Events & highlights** block to showcase upcoming sessions and past activity.
- **Register section** designed to embed a Zoho Form (or similar) so registrations flow directly into CRM.
- **FAQ** covering typical first‑time questions (pricing, upsell concerns, who should join, and how sessions are announced).
- **Language toggle (EN / BM)** powered by a small JS i18n layer (no external libraries).
- **Responsive navigation** with a burger menu on mobile and smooth scroll behavior.
- **Floating mobile FAB** (“back to top”) for thumb‑reachable navigation on small screens.
- **Scroll‑in animations** for hero, cards, images and FAQ details using `IntersectionObserver`.

## Tech Stack

- **HTML5** – semantic single‑page layout (`index.html`).
- **CSS** – inline `<style>` block using CSS variables, responsive grids, and light animation.
- **JavaScript** – vanilla JS for:
  - i18n text switching between English and Malay,
  - mobile nav toggle,
  - scroll‑reveal animations,
  - floating “back to top” behavior,
  - dynamic current year in the footer.
- **Assets** – images in `assets/img/` (hero poster, coach portrait, logo).
- **Icons** – [Font Awesome](https://fontawesome.com) included via CDN for section/card icons and UI elements.

## Getting Started

1. **Clone or copy** this folder into your web root (e.g. `C:\xampp\htdocs\kush`).
2. Ensure the assets directory is preserved:
   - `assets/img/KUSH_LOGO.png`
   - `assets/img/kush-hero.jpg`
   - `assets/img/Rafi_Ansari.jpg`
3. Open `index.html` directly in a browser, or visit the site via your web server (e.g. `http://localhost/kush/` on XAMPP).

No build tools, package managers, or back‑end setup are required.

## Customising Content

- **Text & copy** – Most copy can be edited directly in `index.html`. For any text managed by the language toggle, update the `translations.en` and `translations.ms` objects in the `<script>` block near the end of the file.
- **Images** – Replace the assets in `assets/img/` (keep filenames or adjust `src` paths in `index.html`).
- **Branding / colors** – Global colors and panel backgrounds are defined via CSS variables near the top of the `<style>` block (`:root { --bg, --accent, ... }`).
- **Registration form** – Swap the Zoho Form placeholder iframe in the Register section with your actual embed code.

## Folder Structure

```text
.
├─ index.html        # Main landing page (HTML, CSS, JS)
└─ assets/
   └─ img/
      ├─ KUSH_LOGO.png
      ├─ kush-hero.jpg
      └─ Rafi_Ansari.jpg
```
