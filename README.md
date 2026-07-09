# 🌍 Global Wind Patterns in the Atmosphere
### IEEE SciVis 2026 Contest — Interactive Atmospheric Dashboard

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![Contest](https://img.shields.io/badge/IEEE-SciVis%202026-red)](https://sciviscontest2026.github.io)

---

## 📌 Overview

An interactive Jupyter Notebook dashboard for exploring global atmospheric dynamics using the **DYAMOND C1440-LLC2160** climate simulation dataset, streamed live from NASA's National Research Data Fabric (NSDF) via **OpenVisus**.

The dashboard provides real-time visualization of 9 atmospheric variables across 20 geographic regions, 12 pressure levels, and 10,366 hourly time steps spanning 14 months (January 2020 – March 2021).

---

## ✨ Features

- **7 toggleable map layers:** Temperature, Wind Vectors (U/V), Vertical Velocity (W), Cloud Fraction (FCLD), Geopotential Height (H), Hydrometeors (QI+QL), Convective Tendency (DTHDT)
- **20 geographic regions:** Global, Mexico, USA, Europe, South/East Asia, Arctic, Antarctic, and more
- **12 pressure levels:** 100–1000 hPa (surface to upper troposphere)
- **Full animation:** Play through 10,366 hourly steps with a single button
- **Live cloud streaming:** No local data download required — OpenVisus handles everything
- **Adaptive resolution:** Quality and subsampling auto-adjust based on region size

---

## 🗂 Repository Structure

```
scivis2026-atmospheric-dashboard/
├── scivis2026_dashboard.ipynb   # Main notebook — run this
└── README.md                    # This file
```

---

## ⚙️ Requirements

| Package | Purpose |
|---------|---------|
| `numpy` | Array operations |
| `matplotlib` | Plotting engine |
| `cartopy` | Geospatial map projections |
| `OpenVisus` | Cloud data streaming from NSDF |
| `ipywidgets` | Interactive controls |
| `scipy` | NaN interpolation, array zoom |

---

## 🚀 How to Run

### Option A — Google Colab (recommended, no install needed)

1. Open [Google Colab](https://colab.research.google.com)
2. File → Open notebook → GitHub tab
3. Paste this repository URL and open `scivis2026_dashboard.ipynb`
4. Run all cells (Runtime → Run all)

### Option B — Local Jupyter

```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/scivis2026-atmospheric-dashboard
cd scivis2026-atmospheric-dashboard

# 2. Install dependencies
pip install cython cartopy OpenVisus ipywidgets scipy

# 3. Launch Jupyter
jupyter notebook scivis2026_dashboard.ipynb
```

> **Note:** Cell 1 (Installation) runs `pip install` automatically. If running locally, restart the kernel after the first cell completes.

---

## 🌐 Dataset

| Property | Value |
|----------|-------|
| **Name** | DYAMOND C1440-LLC2160 |
| **Models** | NASA GEOS (atmosphere) + MITgcm (ocean) |
| **Atm. resolution** | ~7 km horizontal |
| **Ocean resolution** | 2–4 km horizontal |
| **Period** | 2020-01-20 → 2021-03-27 |
| **Cadence** | 1 hour |
| **Time steps** | 10,366 |
| **Source** | [NASA NSDF](https://nationalresearchplatform.org) via OpenVisus |

---

## 📊 Variables

| ID | Full Name | Units | Colormap |
|----|-----------|-------|---------|
| T | Air Temperature | K | RdYlBu_r |
| U / V | Eastward / Northward Wind | m/s | — (quiver arrows) |
| W | Vertical Velocity | Pa/s | RdBu_r |
| FCLD | Cloud Fraction | 0–1 | Greys |
| H | Geopotential Height | m | Gold contours |
| QI + QL | Hydrometeors (ice + liquid) | kg/kg | GnBu |
| DTHDT | Convective Tendency | K/s | YlOrRd / PuBu_r |

---

## 🏆 Contest

**IEEE SciVis 2026 Contest** · Submission deadline: July 19, 2026  
[https://sciviscontest2026.github.io](https://sciviscontest2026.github.io)

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.
