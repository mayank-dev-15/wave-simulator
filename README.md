# 🌊 Wave Simulator

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Canvas](https://img.shields.io/badge/Canvas-FF6B6B?logo=canvas&logoColor=white)](#)
[![Physics](https://img.shields.io/badge/Physics-⚛️-blue)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A real-time physics-based wave simulator that demonstrates interference, diffraction, superposition, and standing waves — all rendered in your browser. Perfect for students, teachers, and anyone who wants to *see* wave mechanics in action.

---

## ✨ Features

- **Multiple wave sources** — add point sources anywhere on the canvas with adjustable frequency, amplitude, and phase
- **Real-time interference patterns** — watch constructive and destructive interference emerge instantly
- **Built-in presets**: Double Slit, Doppler Effect, Resonance, Standing Waves, Circular Waves
- **Side-by-side comparison** — run two independent simulations simultaneously
- **Parameter sliders** for frequency, amplitude, wavelength, and damping
- **Slow-motion mode** (0.1x to 2x speed) to observe fast phenomena
- **Measurement tools** — click to read amplitude and phase at any point
- **Color-mapped amplitude visualization** with 3 color schemes

---

## 🌊 Wave Types

### Circular Waves

The simplest — a single point source radiating outward. Amplitude decreases with distance:

```
A(r) = A₀ / √r
```

This 2D inverse-square-root decay models how energy spreads radially.

### Plane Waves

Uniform waves traveling in one direction. Great for demonstrating pure interference when combined with another source at a slight angle.

### Standing Waves

Two identical waves traveling in opposite directions interfere to create nodes (zero amplitude) and antinodes (maximum amplitude). The resulting pattern:

```
y(x,t) = 2A · sin(kx) · cos(ωt)
```

Nodes occur at `kx = nπ` — positions where the displacement is always zero.

---

## 🔬 Presets

### Double Slit Experiment

The famous quantum mechanics demo, classically simulated. Waves pass through two narrow slits and interfere on a distant screen.

- Adjustable slit width, slit separation, and wavelength
- Intensity pattern on the "detection screen" drawn in real time
- Watch how wider slits blur the interference fringes

### Doppler Effect

A moving source emits waves that bunch up ahead and stretch behind — just like a passing ambulance.

- Drag the source to move it, or set a velocity vector
- Frequency shift: `f' = f · v_sound / (v_sound ± v_source)`
- Visual wave-front compression and expansion in real time

### Resonance

Drive a system at its natural frequency and watch amplitude grow dramatically.

- Adjustable driving frequency — sweep through to find resonance peaks
- Quality factor (Q) control to tune damping
- Amplitude vs. frequency response curve plotted live

---

## 📐 Physics Explanation

### The Superposition Principle

This is the core concept that makes interference possible. When two or more waves occupy the same point in space, the **net displacement** is the algebraic sum of individual displacements:

```
y_total(x,t) = y₁(x,t) + y₂(x,t) + ... + yₙ(x,t)
```

Each wave passes through the others as if they weren't there. The waves don't interact with each other — they simply add.

### Constructive vs. Destructive Interference

- **Constructive**: Waves arrive **in phase** (phase difference = 0, 2π, 4π, ...). Amplitudes add: `A_total = A₁ + A₂`
- **Destructive**: Waves arrive **out of phase** (phase difference = π, 3π, ...). Amplitudes subtract: `A_total = |A₁ - A₂|`

The intensity (energy) goes as amplitude squared, so constructive interference gives **4×** the intensity of a single source when amplitudes are equal.

### Path Difference and Phase

The key to predicting interference:

```
Phase difference φ = (2π/λ) · Δr
```

where `Δr` is the path-length difference between two sources to the observation point:

- When `Δr = mλ` (integer multiple) → **bright fringes**
- When `Δr = (m + ½)λ` → **dark fringes**

---

## 🎮 Controls

| Action | Control |
|--------|---------|
| Add wave source | Click anywhere on canvas |
| Move source | Drag existing source |
| Remove source | Right-click on source |
| Adjust frequency | Slider or `F` key |
| Adjust amplitude | Slider or `A` key |
| Cycle presets | Press `P` |
| Toggle slow-mo | Press `S` |
| Toggle measurement | Press `M` |
| Clear all sources | Press `C` |
| Pause or Resume | Spacebar |
| Reset simulation | Press `R` |
| Screenshot | Press `X` |

---

## 🚀 Installation

```bash
git clone https://github.com/mayank-dev-15/wave-simulator.git
cd wave-simulator
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

Or with a local server:

```bash
python3 -m http.server 8080
# Visit http://localhost:8080
```

No dependencies. No build step. Just HTML, CSS, and JavaScript.

---

## 📖 Usage

1. **Start with the Double Slit preset** — the classic experiment. Watch the interference pattern form.
2. **Adjust slit separation** — wider spacing gives tighter fringes. Narrower spacing gives wider fringes.
3. **Try the Doppler preset** — drag the source around and watch wavefronts compress and stretch.
4. **Resonance demo** — slowly increase the driving frequency and watch amplitude peak at the natural frequency.
5. **Add your own sources** — click to place sources and watch complex interference patterns emerge.

---

## 📄 License

MIT License — use freely for learning, teaching, or building upon. See [LICENSE](LICENSE) for details.

---

*Visualize the invisible. Understand waves by watching them.* 🌊