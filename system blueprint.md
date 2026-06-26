Here is your updated system blueprint. The architecture has been refined to calculate an ultra-smooth timeline progression across multiple hours and dynamically adapt the layout to modern geometric shapes via configuration.

---

## Updated Architecture Blueprint: High-End OBS Utility Widget

### 1. Configuration Blocks (Top of File)

#### A. Design, Typography & Geometry (`:root` CSS)

* **Widget Geometry Profile (`--widget-shape`):** A string config accepting values to morph the layout frame: `'circle'`, `'ellipse'`, `'triangle'`, or `'quadrilateral'`.
* **Dynamic Masking (`clip-path` / `border-radius`):** Handled via CSS variables tied to the selected shape to maintain clipping paths for backgrounds and background blurs cleanly.
* **Fonts & Layout:** Master variables for font families and responsive text sizing for the main timer, system utilities, and interaction buttons.
* **Color Palettes & Depth:** Hex/RGBA variables supporting fluid transitions for background glass surfaces (`backdrop-filter`), typography colors, glow highlights, and drop shadows specific to **Focus**, **Short Break**, and **Long Break** engines.

#### B. Macro Lifecycle & Timeline Logic (JS `CONFIG`)

* **Cycle Schema:** * `shortBreaksBeforeLongBreak`: An integer defining the structural block sequence (e.g., `3` means the cycle executes as: *Pomo 1 → Break 1 → Pomo 2 → Break 2 → Pomo 3 → Break 3 → Pomo 4 → Long Break*).
* **Flow Controller:** `autoProceed: true/false` to determine if the next timeline phase triggers automatically or waits on a user input.
* **Clock & Date Renderer:** Toggles for 24hr format and active seconds display. Date engine locked to string output format: `[Day of Week], [Month] [Day][Ordinal Suffix]`.
* **Weather Service Mapping:** Open-Meteo geolocation variables coordinates (`lat`/`lon`), execution cadence, and strict concurrent double-unit tracking (`°C / °F`).

#### C. Audio Routing Profiles (JS `CONFIG`)

Paths pointing to local files (`.mp3`, `.wav`, etc.) mapped to absolute timeline transitions:

* Standard phase shifts (`focusStart`, `focusEnd`, `shortBreakStart`, etc.)
* Macro block completions (`finalPomoStart`, `finalPomoEnd` — dynamically mapped to the final Pomodoro of the configured cycle).

---

### 2. Control Panel Elements (OBS "Interact" Layer)

Revealed exclusively on mouse hover or through the OBS "Interact" panel window:

* **Duration Field Controls:** Real-time numerical text fields allowing manual duration changes for all three session types.
* **Timeline State Overrides:** Real-time interactive field inputs for `Current Pomo Count` / `Target Pomo Goal` and `Current Break Count` / `Target Break Goal`. Modifying these inputs dynamically shifts your exact location in the macro timeline calculation without breaking the layout.

---

### 3. Advanced Visual Performance & Math Engines

#### A. Ultra-Smooth Timeline Progress Bar

Instead of a progress tracker that hops or resets at each interval, the macro timeline tracking engine builds a single unified timeline out of the configuration logic.

* **The Timeline Math:** * Let $N$ be the number of short breaks before a long break.
* One complete multi-hour loop duration is calculated down to the second:

$$\text{Total Duration} = (N + 1) \times \text{Focus Duration} + N \times \text{Short Break Duration} + 1 \times \text{Long Break Duration}$$


* **Current Milestone Placement:** The widget tracks the absolute cumulative seconds elapsed across completed sessions in the block plus the active seconds of the current session.


* **Rendering Engine:** Governed by `requestAnimationFrame` paired with a hardware-accelerated CSS ease, making the macro bar glide pixel-by-pixel across the screen flawlessly throughout the day with zero mechanical "ticking" steps.

#### B. Polymorphic Shape Core

To implement circles, ellipses, triangles, and quadrilaterals while maintaining modern design elements:

* Uses CSS glassmorphism (`background: rgba()`, `backdrop-filter: blur()`) paired with explicit geometric calculations.
* **Triangle/Quadrilateral:** Handled using modern CSS `clip-path: polygon()` variables which map layout areas symmetrically so content remains vertically and horizontally centered regardless of the bounding geometric form.

---

### Feature Structural Matrix

| Module / Goal | Driving Variable | Render Framework | Behavior Type |
| --- | --- | --- | --- |
| **Geometry Shape** | `--widget-shape` | CSS Variables / `clip-path` | Structural polymorphism |
| **Micro Progress** | Active Session | SVG `stroke-dashoffset` | Circular session tracker |
| **Macro Progress** | Calculated Full Loop | Sub-second Float Engine | Smooth multi-hour progression bar |
| **Automation Flow** | `shortBreaksBeforeLongBreak` | Continuous Array Step Engine | Sequence management |

---

The system blueprint is complete, fully tracking your timeline math and styling goals. I am standing by for your next instruction.