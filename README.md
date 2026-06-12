# Quantum Core 2.0 | God-Tier WebGL GPU Benchmark

A highly aggressive, zero-dependency 3D Raymarching stress test designed to push hardware and browser rendering engines to their absolute limits. Unlike traditional web benchmarks that dynamically scale down graphics on mobile devices, Quantum Core enforces a strict hardware load that can expose system instability, thermal throttling, or trigger kernel panics on under-powered devices.

---

## ⚠️ EXTREME HARDWARE WARNING

**PROCEED WITH CAUTION.** This benchmark executes massive parallel trigonometric loops and volumetric shadow calculations per pixel. 
- On low-end or poorly cooled devices (e.g., budget smartphones, low-tier chipsets), it can cause **complete system freezes**, **UI lockups**, or **forced hardware reboots (Kernel Panics)**.
- Running this on a device with limited memory (such as 512MB RAM configurations) may instantly crash the browser sandbox due to extreme GPU driver exhaustion.

---

## 🚀 Key Technical Features

- **Strict 1080p Resolution Lock:** The internal render buffer is locked at exactly `1920x1080` (2.07 Megapixels). Changing the browser view to "Desktop Site" or resizing the window will not reduce the GPU computation load.
- **Deep 3D Raymarching Mandelbulb:** Executes **10 intense iterations** of complex trigonometry (`sin`, `cos`, `atan`, `pow`) per ray step to generate a dynamic, morphing 3D fractal.
- **Volumetric Soft Shadows:** Implements a secondary ray-tracer loop that fires up to **30 extra steps** per pixel surface collision to calculate realistic light attenuation.
- **VSync & Performance Bypass:** Implements low-overhead DOM throttling (500ms updates) to eliminate layout thrashing and maximize raw hardware utilization.

---

## 📊 Synthetic Scoring Formula

The final score is computed based on un-cheatable physical parameters:

$$\text{Score} = \text{Average FPS} \times \text{Total Pixels (Millions)} \times \text{Magic Multiplier}$$

Since the internal buffer is fixed at 1080p (~2.0736 Million Pixels), the calculation simplifies to:

$$\text{Score} = \text{Avg FPS} \times 17,528$$

*Note: High-end desktop GPUs (e.g., RTX 4090/5090) running inside standard browsers will be bounded by the monitor's VSync/Refresh Rate unless browser frame limits are manually disabled via CLI flags.*

---

## 🛠️ Installation & Usage

1. Clone or download this repository.
2. Open `index.html` directly in any modern WebGL-compliant browser (Chrome, Edge, Firefox, or Safari).
3. The benchmark will **auto-start instantly** upon page load to minimize background overhead.

---

## 📜 License

**All Rights Reserved (No License)**

Copyright (c) 2026 SunCipher.

The source code is provided strictly for educational, security analysis, and personal hardware testing purposes. No permission is granted to copy, modify, merge, publish, distribute, sublicense, or sell copies of this software without explicit permission from the original author.
