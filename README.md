# Electromagnetic Spectrum Explorer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-26.3.3.1-indigo.svg)](https://jordonhgriffin.com)
[![Live](https://img.shields.io/badge/Live-jordonhgriffin.com-blue.svg)](https://jordonhgriffin.com)

An interactive 3D visualization of the full electromagnetic spectrum — from cosmic gamma rays at 10⁻¹⁶ m to planetary-scale radio waves at 10⁴ m — built with Three.js and rendered in real time in the browser.

---

## Overview

The electromagnetic spectrum spans over 20 orders of magnitude in wavelength and frequency. This explorer maps that entire range onto a navigable 3D ribbon, giving each band a physical presence and a set of human-readable data — wavelength, frequency, energy, emitters, detectors, and scale analogues.

The spectrum is structured logarithmically. Moving left along the ribbon takes you into shorter wavelengths and higher energies (X-rays, gamma rays, cosmic rays). Moving right descends into longer wavelengths and lower energies (microwaves, radio waves, ELF).

### Spectral Regions

| Region | Wavelength | Frequency |
|---|---|---|
| Cosmic / Gamma Rays | < 10 pm | > 30 EHz |
| X-Rays | 0.01 – 10 nm | 30 PHz – 30 EHz |
| Ultraviolet | 10 – 400 nm | 750 THz – 30 PHz |
| Visible Light | 400 – 700 nm | 430 – 750 THz |
| Infrared | 700 nm – 1 mm | 300 GHz – 430 THz |
| Microwave | 1 mm – 1 m | 300 MHz – 300 GHz |
| Radio / ELF | > 1 m | < 300 MHz |

### Fiber Optic Telecom Bands (NIR)

The fiber optic telecommunications window (1260–1675 nm) is labeled with standard ITU bands:

| Band | Name | Wavelength |
|---|---|---|
| O-Band | Original | 1260 – 1360 nm |
| E-Band | Extended | 1360 – 1460 nm |
| S-Band | Short-wavelength | 1460 – 1530 nm |
| C-Band | Conventional | 1530 – 1565 nm |
| L-Band | Long-wavelength | 1565 – 1625 nm |
| U-Band | Ultra-long | 1625 – 1675 nm |

---

## Features

- **3D Ribbon Navigation** — A 400-unit logarithmic ribbon rendered in WebGL. Click-drag to pan, scroll to zoom. Scene markers label each major spectral domain.
- **Real-Time HUD** — Wavelength (λ), frequency (ν), and energy (E) are calculated live from camera position and updated instantly in the right-side info panel.
- **Band Jump Navigation** — Left panel lists all spectral bands and fiber telecom sub-bands. Clicking any entry animates the camera to that region and displays an info panel.
- **Band Info Panels** — Each band has a dedicated info card: summary description, wavelength/frequency range, emitter, detector, energy level, and a scale analogue (e.g., "DNA strand", "Human hair", "Football field").
- **Physical Concepts Panel** — Right column surfaces the wave phenomena that apply across the spectrum: Reflection, Refraction, Diffraction, and Interference — each linking to external resources.
- **Atmospheric Opacity Indicator** — Shows whether the current band is transparent, partially absorbed, or opaque/reflected by Earth's atmosphere.
- **Mobile Optimized** — Collapsible bottom-drawer navigation, touch-scroll support, full-width top info banner, and hamburger FAB button for mobile viewports.
- **Wikipedia Integration** — Every band info card includes a direct Wikipedia link. The main title links to the Electromagnetic spectrum article.

---

## Technical Stack

| Layer | Technology |
|---|---|
| 3D Rendering | [Three.js](https://threejs.org/) r169 (WebGL 2) |
| Camera Controls | `OrbitControls` from Three.js addons |
| Animations | Native `requestAnimationFrame` with cubic-ease |
| Shaders | Custom GLSL ribbon with logarithmic wave oscillation |
| UI | Vanilla HTML/CSS — glassmorphism, CSS custom properties |
| Fonts | Google Fonts: Outfit, Space Mono |
| Hosting | GitHub Pages via [jordonhgriffin.com](https://jordonhgriffin.com) |

No build step. No framework. Single `index.html`.

---

## How to Use

1. **Jump to a band** — Open the left navigation panel and click any spectral band or telecom sub-band. The camera will animate to that region and an info card will appear.
2. **Pan freely** — Click and drag anywhere on the 3D scene to pan along the spectrum.
3. **Zoom** — Scroll or pinch to zoom in and out.
4. **Read the HUD** — The right column updates in real time with physical data for your current position.
5. **Reset** — Click **Reset View** (top of the nav panel) to return to the full-spectrum overview and dismiss any open info panel.
6. **Mobile** — Tap ☰ (bottom-left) to open the nav drawer. Tap any band to jump; the drawer closes automatically.

---

## Background

The physics of the electromagnetic spectrum was established over roughly a century:

- **1820s–1860s** — Faraday and Maxwell unified electricity, magnetism, and optics. Maxwell's equations predicted EM waves traveling at the speed of light.
- **1887** — Hertz experimentally confirmed radio waves, confirming Maxwell's theory.
- **1895–1900** — Röntgen (X-rays), Villard (gamma rays), and Becquerel completed the high-energy end of the spectrum.
- **1900–1905** — Planck and Einstein introduced quantization: E = hν. Photons carry discrete energy proportional to frequency.
- **Modern** — Wave-particle duality is established. Every photon exhibits both wave and particle behavior depending on how it is observed.

---

## License

MIT — see [LICENSE](LICENSE).

---

**Made by [JHG](https://jordonhgriffin.com)** · Version 26.3.3.1
