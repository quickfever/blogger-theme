<div align="center">

# Quickfever Modern Magazine Theme for Blogger

**A clean, responsive, high-performance magazine theme for Blogger (Blogspot).**  
Designed for technology publications, software reviews, tutorials, and editorial blogs.

[![Blogger](https://img.shields.io/badge/Blogger-Layouts%20v3-orange.svg?style=flat-square&logo=blogger)](https://www.blogger.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Vanilla JS](https://img.shields.io/badge/JavaScript-Vanilla-yellow.svg?style=flat-square&logo=javascript)](https://developer.mozilla.org)
[![Responsive](https://img.shields.io/badge/Layout-Responsive-success.svg?style=flat-square)](#features)
[![Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen.svg?style=flat-square)](#tech-stack)

[Features](#features) • [Installation](#installation) • [Layout Setup](#customizing-via-blogger-layout) • [Authoring Guide](#post-authoring-guide)

</div>

---

## Overview

This theme brings a clean, multi-column editorial magazine design to the Google Blogger platform, featuring:
- A horizontal **Top 5 Ranked Stories** section with bold numbering.
- A split **Articles Grid** (large featured story on the left, 2x2 grid on the right).
- A focused **Single Article View** with red category breadcrumbs, a prominent headline, an introductory deck, a framed hero showcase container, and a custom sidebar.

---

## Features

- **Lightweight & Fast**: Built with pure CSS (Grid + Flexbox) and vanilla JavaScript. Zero dependencies on jQuery or external UI libraries.
- **Mobile Responsive**: Fully responsive layout with an off-canvas slide-out navigation drawer for mobile and tablet visitors.
- **Ranked Featured Row**: Displays top trending posts with automatic numbered badges (`1` to `5`) powered by CSS counters.
- **Editorial Homepage Grid**:
  - **Left**: 1 prominent hero story with wide artwork, category tag, headline, and excerpt.
  - **Right**: 2x2 grid for tutorials, downloads, and secondary articles.
- **Framed Hero Image**: Single post featured images are centered inside a soft pastel rounded container to highlight screenshots and review graphics.
- **Interactive Search**: Modal search dialog connected directly to Blogger's search route (`/search?q=`).
- **Dropdown Menus**: Easily create dropdown navigation in Blogger Layout using simple underscore prefixes (e.g., `_Submenu Item`).
- **Discover More Sidebar**: Navigation card with right-arrow chevrons and hover transitions.
- **Clean Layout Editor**: Includes `<b:template-skin>` so the Blogger dashboard **Layout** tab displays an organized, non-overlapping grid.

---

## Repository Structure

```
├── Quickfever-Blogger-Theme.xml   # Complete Blogger Layouts Version 3 XML theme
├── preview.html                   # Local interactive preview (open in any web browser)
└── README.md                      # Documentation and setup guide
```

---

## Installation

1. Download or clone this repository.
2. Open your **[Blogger Dashboard](https://www.blogger.com)**.
3. In the left sidebar, click **Theme**.
4. Next to the **CUSTOMIZE** button, click the dropdown arrow (**▾**) and select **Restore**.
5. Click **Upload** and select `Quickfever-Blogger-Theme.xml`.
6. Blogger will apply the template immediately.

---

## Customizing via Blogger Layout

Configure your blog directly from **Blogger Dashboard → Layout** without editing code:

### 1. Main Navigation (`LinkList1`)
- Go to **Layout → Main Navigation → Edit**.
- Add your main links (e.g., `Home`, `Software`, `Guides`, `Operating Systems`).
- **To create a dropdown menu**: Prefix the title of sub-links with an underscore (`_`):
  - `Operating Systems` → `/search/label/OS`
  - `_Windows` → `/search/label/Windows`
  - `_Linux` → `/search/label/Linux`
  - `_Android` → `/search/label/Android`
  The theme automatically builds a hover dropdown under the parent link.

### 2. Header Action Button (`LinkList99`)
- Go to **Layout → Header Button → Edit**.
- Update the title and URL (e.g., `Follow Us`, `Instagram`, `Newsletter`, or `Subscribe`).

### 3. "Discover More" Sidebar (`LinkList2`)
- Go to **Layout → Article Sidebar → Discover more → Edit**.
- Add topics, tags, or curated links. Each item automatically receives a right chevron arrow icon.

### 4. Ranked Posts Row (`PopularPosts1`)
- Go to **Layout → App Directory 5 Ranked Posts → Edit**.
- Choose your preferred time window (*All time*, *Last 30 days*, or *Last 7 days*).
- The theme formats the top 5 articles with rank numbers `1` through `5`.

---

## Post Authoring Guide

### Category Tag
Assign labels under **Post Settings → Labels** (e.g., `SOFTWARE` or `HOW-TO`). The theme displays the label in bold uppercase red text preceded by `> `.

### Subtitle / Deck
To include an introductory summary beneath the post title, add your lead paragraph in the post editor:
```html
<p class="qf-single-deck">
  A practical guide to modern productivity workflows and software tools.
</p>
```

### Framed Hero Screenshot
Upload your primary image at the top of your post or set it as the featured image. On single post pages, it is automatically displayed inside a pastel rounded card.

---

## Tech Stack

| Component | Implementation |
| :--- | :--- |
| **Platform** | Blogger Layouts Version 3 (`b:layoutsVersion='3'`) |
| **Typography** | Inter via Google Fonts |
| **Icons** | Inline SVG (zero extra HTTP requests) |
| **Rank Counter** | Pure CSS (`counter()`) |
| **Scripts** | Vanilla JavaScript |

---

## License

This project is open-source under the [MIT License](LICENSE).
