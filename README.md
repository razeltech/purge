# PURGE — Metadata & Content Credentials (C2PA) Sanitizer

[![Live Studio](https://img.shields.io/badge/Live-PURGE%20App-emerald?style=flat-square)](https://razeltech.github.io/purge/)
[![Engineering](https://img.shields.io/badge/Engineered%20by-Razel%20Tech-indigo?style=flat-square)](https://razeltech.github.io)
[![PWA](https://img.shields.io/badge/PWA-100%25%20Offline-amber?style=flat-square)](https://razeltech.github.io/purge/)
[![License](https://img.shields.io/badge/License-MIT%20Attribution-blue?style=flat-square)](LICENSE)

**PURGE** is a 100% client-side privacy tool designed to inspect, detect, and neutralize invisible provenance payloads, C2PA manifests (Content Credentials), EXIF markers, GPS coordinates, and AI generator watermarks from images, video, audio, and documents directly in your browser.

Zero uploads. Zero servers. Zero cloud processing.

---

## The Problem: Invisible AI Labels & Metadata Leakage

Modern social media platforms (LinkedIn, Instagram, Meta, TikTok, X, and search engines) actively parse media files for **C2PA (Coalition for Content Provenance and Authenticity)** JUMBF boxes and AI generator tags (Midjourney, DALL-E, Stable Diffusion, Adobe Firefly).

When these invisible cryptographic markers are present in your image files:
1. **Automated AI Flags:** Platforms automatically slap permanent "Made with AI" or "AI Info" tags onto your posts.
2. **Organic Reach Suppression:** Algorithmic ranking systems frequently downrank or deprioritize AI-tagged media in algorithmic feeds.
3. **Privacy Exposure:** Unsanitized photos contain precise GPS coordinates, device serial numbers, camera lens models, timestamps, and edit history.

**PURGE neutralizes these payloads at the binary level before you publish.**

---

## Detection Engine & Capabilities

PURGE parses and sanitizes media across all standard formats:

| Category | Targeted Markers & Payload Signatures |
| :--- | :--- |
| **C2PA & Provenance** | JUMBF boxes, `c2pa` markers, `c2ma` manifests, cryptographic signatures, provenance assertions |
| **AI Generator Tags** | Midjourney parameters, DALL-E signatures, Stable Diffusion prompts, Adobe Firefly metadata |
| **Camera & Device EXIF** | GPS altitude/latitude/longitude, camera model, lens serial, exposure, date taken, software version |
| **Editor Signatures** | Photoshop 8BIM blocks, Adobe XMP namespaces, Lightroom presets, color profiles |
| **Audio & Video** | QuickTime MP4/MOV `moov` atoms, user data `udta` boxes, ID3v1/ID3v2 tags, artist/comment fields |
| **Documents** | PDF author metadata, producer software, modification dates, embedded thumbnails |

---

## Key Features

- **Real-Time Detection Alerts:** Explicitly flags `Detected (Will Trigger AI Label)` whenever C2PA or generative AI markers are present.
- **Deep Inspection Accordion:** Review every single EXIF, XMP, and binary tag payload before choosing to sanitize.
- **Lossless & Optimized Output:** Preserves pristine visual fidelity without unnecessary quality recompression.
- **Bulk Processing & ZIP Export:** Drop dozens of files simultaneously and export all sanitized media in a single click.
- **Progressive Web App (PWA):** Installs as a standalone native app on Android, iOS, Windows, and macOS. Operates completely without an active internet connection.
- **Zero Cloud Architecture:** All byte slicing, HTML5 Canvas rendering, and ArrayBuffer transformations happen exclusively inside your device's memory.

---

## Supported Formats

- **Images:** JPEG, PNG, WebP
- **Video:** MP4, MOV (QuickTime), WebM
- **Audio:** MP3, WAV
- **Documents:** PDF

---

## PWA Installation

### Android & Desktop (Chrome / Edge)
Click the **INSTALL APP** button in the top banner or header to install PURGE directly to your desktop or home screen.

### Apple iOS / iPadOS (Safari)
1. Open [https://razeltech.github.io/purge/](https://razeltech.github.io/purge/) in Safari.
2. Tap the **Share** button in the bottom navigation bar.
3. Scroll down and select **Add to Home Screen**.

---

## Verification & Integrity

To verify that C2PA manifests have been completely eliminated:
1. Process an AI-generated image through PURGE.
2. Download the sanitized file.
3. Inspect the sanitized output at [verify.contentcredentials.org](https://verify.contentcredentials.org).
4. Result: **No Content Credentials found**.

---

## Author & Attribution

- **Engineering:** Razel Tech ([https://razeltech.github.io](https://razeltech.github.io))
- **Systems Architect:** Raja Vamsi Dhar Vallabhapurapu
- **License:** [MIT License with Mandatory Author Attribution](LICENSE)
