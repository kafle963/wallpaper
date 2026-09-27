# 🌌 Drift Wallpaper: Master Physics Engine & Code Map

This document serves as the permanent registry and architectural guide for all real-time physics simulations running inside [`index.html`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html).

---

## 🗺️ Master Physics Code Map & Line Index

| Physics Module | Functionality & Simulation Details | CSS / Styling Location | JavaScript Logic Location | Key State & Physics Variables |
| :--- | :--- | :--- | :--- | :--- |
| **1. Clock & Date Display Dynamics** | Viewport clamping, rubber-band wall bounce, inertial throwing friction & 3D gyroscopic cursor tilt | [`index.html:L210-L245`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L210-L245) | [`index.html:L3629-L3838`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L3629-L3838) | `textVx`, `textVy`, `textInertiaId`, `targetTiltX`, `targetTiltY`, `getClampedTextPos` |
| **2. Celestial Gravitational Well** | Multi-body particle stardust with Newtonian gravity wells, orbital vortex swirl & aerodynamic drag | [`index.html:L2298-L2308`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L2298-L2308) | [`index.html:L5586-L5760`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L5586-L5760) | `G = 1200`, `DRAG = 0.985`, `mousePhys`, `particles` |
| **3. 2D Fluid Wave Ripple Physics** | Dynamic wave propagation, harmonic refraction rings & exponential energy dissipation | [`index.html:L2298-L2308`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L2298-L2308) | [`index.html:L5650-L5670`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L5650-L5670), [`index.html:L5765-L5804`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L5765-L5804) | `ripples`, `spawnFluidRipple`, `strength`, `decay` |
| **4. Aerodynamic Clouds & Buoyancy** | Atmospheric buoyancy harmonic oscillation & drag physics | [`index.html:L475-L520`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L475-L520) | [`index.html:L5488-L5525`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L5488-L5525) | `cloudDefs`, `makeDraggable`, `cloud-float` |
| **5. Spotify Glass Widget Momentum** | Inertial gliding with kinetic friction, magnetic boundary bounce & edge docking | [`index.html:L2345-L2400`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L2345-L2400) | [`index.html:L4860-L4940`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L4860-L4940) | `spVx`, `spVy`, `isDraggingSpotify`, `setSpotifyPosition` |
| **6. Companion Spring Elasticity** | Jiggle dynamics, squash-and-stretch on poke/click, ear/tail pendulum physics | [`index.html:L710-L860`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L710-L860) | [`index.html:L5550-L5613`](file:///c:/Users/a/Desktop/ai/wallpaper1/index.html#L5550-L5613) | `triggerCatIdle`, `catEarL`, `catEarR`, `catTail` |

---

## 🔬 Mathematical Formulations & Simulation Mechanics

### 1. Clock & Date Elastic Dynamics & Clamping
* **Invariant Viewport Clamping**:
  $$\text{clampedX} = \max\Big(\text{margin}, \min\big(\text{window.innerWidth} - \text{width} - \text{margin}, x\big)\Big)$$
  $$\text{clampedY} = \max\Big(\text{margin}, \min\big(\text{window.innerHeight} - \text{height} - \text{margin}, y\big)\Big)$$
* **Elastic Wall Collision Bounce**:
  $$v_x' = -e \cdot v_x, \quad v_y' = -e \cdot v_y \quad (e = 0.55)$$
* **Kinetic Drag & Friction**:
  $$\vec{v}_{t+1} = \vec{v}_t \cdot \mu \quad (\mu = 0.90)$$
* **3D Gyroscopic Perspective Hover Tilt**:
  $$\theta_x = -\left(\frac{y - y_{\text{center}}}{h/2}\right) \cdot \theta_{\max}, \quad \theta_y = \left(\frac{x - x_{\text{center}}}{w/2}\right) \cdot \theta_{\max}$$

---

### 2. Celestial Newtonian Gravity Well & Particle Flow
* **Newtonian Gravitational Attraction**:
  $$\vec{F}_g = \frac{G \cdot m \cdot M_{\text{cursor}}}{r^2 + \epsilon^2} \hat{r}, \quad (\epsilon = 48.9\text{px}, G = 1200)$$
* **Tangential Orbital Vortex Swirl**:
  $$\vec{F}_{\text{vortex}} = \langle -\hat{r}_y, \hat{r}_x \rangle \cdot (0.35 \cdot |\vec{F}_g|)$$
* **Atmospheric Thermal Convection & Brownian Jitter**:
  $$a_y = -\frac{0.012}{m}, \quad a_x = \sin(\phi_t) \cdot 0.02$$
* **Aerodynamic Air Drag**:
  $$\vec{v}_{t+1} = \vec{v}_t \cdot \gamma \quad (\gamma = 0.985)$$

---

### 3. Interactive 2D Fluid Wave Ripple Propagation
* **Radial Wave Growth**:
  $$r(t) = r_0 + v_{\text{wave}} \cdot t$$
* **Exponential Energy Dissipation**:
  $$A(t) = A_0 - \lambda \cdot t$$
* **Harmonic Refraction Rings**:
  Renders primary wavefront at $r(t)$ and secondary harmonic refraction ring at $0.72 \cdot r(t)$ with adaptive color palettes synchronized to the sky time period (morning, afternoon, evening, night).

---

## ⚡ Key Updates Applied in This Release
1. **Resolved Clock & Date Screen-Escape Bug**: Fixed coordinate jumping by removing CSS transition conflicts during interaction, applying absolute viewport clamping ($16\text{px}$ margin), and adding rubber-band boundary collision physics.
2. **Added 3D Gyroscopic Micro-Physics**: Hovering over the date/time display smoothly tilts the widget in 3D space according to cursor position without altering its screen layout position.
3. **Integrated Fullscreen Physics Canvas**: High-performance Canvas 2D engine with real-time Newtonian gravity stardust and click/drag wave ripples.
