# Pixlo Animation Studio ✨

A web-based tool to create and preview cool text animations using Anime.js, all within a single HTML file! Experiment with various presets for text, fonts, colors, and animation styles, and even export your creations as WebM video or basic Lottie JSON.

**(Add a Screenshot or GIF Here!)**

![Screenshot/GIF of the Studio Interface](placeholder.gif)
*Replace `placeholder.gif` with an actual image or GIF showcasing the interface and an animation.*

---

## Features

*   **Live Text Input:** Enter any text you want to animate.
*   **Extensive Animation Presets:** Choose from a wide variety of entrance, exit, and emphasis animations powered by [Anime.js](https://animejs.com/).
*   **Font Variety:** Select from a large list of Google Fonts (Sans-Serif, Serif, Monospace, Display, Script, etc.).
*   **Color Palettes:** Apply preset color schemes for text/glow and background.
*   **Letter Spacing Control:** Adjust the spacing between letters using a slider.
*   **Text Effects Toggle:** Enable or disable a configurable text glow/shadow effect.
*   **Live Preview:** See your animation and style changes instantly in the top panel.
*   **WebM Video Export:** Record the animation preview as a high-resolution (1080p) `.webm` video file using the `MediaRecorder` API and Canvas rendering.
*   **Basic Lottie Export:** Generate a `.json` Lottie file for simpler animations (opacity, position, scale, basic rotation).
*   **Single File:** The entire application (HTML, CSS, JavaScript) is contained within a single file for easy sharing and use.

## How to Use

1.  **Download:** Get the main `.html` file from this repository.
2.  **Open:** Open the downloaded `.html` file in a modern web browser (like Chrome, Firefox, Edge, Safari).
3.  **Customize:**
    *   Use the **"Text & Animation"** controls at the bottom to:
        *   Enter your desired text.
        *   Select an animation preset.
        *   Adjust letter spacing.
    *   Use the **"Appearance"** controls to:
        *   Choose a font family.
        *   Select text and background color palettes.
        *   Toggle text effects (glow/shadow).
4.  **Preview:** See the animation play in the top section of the page.
5.  **Apply & Replay:** Click the **"Apply & Animate"** button to apply all current settings and replay the animation.
6.  **Export:**
    *   Click **"Export WebM"** to record the animation playing on a hidden canvas and download it as a `.webm` video file. (Recording takes a few seconds).
    *   Click **"Export Lottie (Basic)"** to generate and download a `.json` Lottie file representation of simpler animations.

## Technology Stack

*   **HTML5**
*   **CSS3:** Including CSS Variables (Custom Properties) for theming.
*   **JavaScript (ES6+):** For all the logic, DOM manipulation, and export features.
*   **Anime.js:** A lightweight JavaScript animation library used for the core DOM animations.
*   **Web APIs:**
    *   `MediaRecorder` and `Canvas.captureStream()` for WebM video export.
    *   `Blob`, `URL.createObjectURL`, and `<a>` download attribute for file generation.

## Export Details & Limitations

*   **WebM Export:**
    *   Uses the browser's `MediaRecorder` API to record frames drawn onto a hidden `<canvas>`.
    *   The canvas animation is a **simulation** of the selected DOM animation. It aims to capture the *concept* but **will not be a pixel-perfect replica** of complex Anime.js easing, physics, filters (like blur), or advanced 3D transforms. Simpler animations (fades, basic translates, scales) will translate better.
    *   Export resolution is fixed at **1920x1080 (1080p)** for better quality.
    *   The output format is `.webm` (using VP8 or VP9 codec), which is well-supported in modern browsers but might require conversion for use in some video editors.
*   **Lottie Export:**
    *   This feature is **basic and experimental**.
    *   It generates a Lottie JSON structure representing the text, font (requires font availability on the rendering system), colors, and *simplified* keyframes for **opacity, position (translate), scale, and Z-axis rotation**.
    *   It **cannot** replicate complex Anime.js easing (e.g., elastic, bounce), physics, filters, masks (for wipes), advanced 3D transforms (X/Y rotation, skew), or text animator features found in After Effects.
    *   **Font Dependency:** The exported Lottie file relies on the **exact font name** being available on the system or player rendering the animation. For guaranteed display, fonts usually need to be embedded or text converted to shapes (typically done via After Effects plugins).
*   **APNG Export:** Not implemented due to the complexity of client-side animated PNG generation without specialized libraries or server-side processing.

## Future Ideas

*   More animation presets and types.
*   Improved Lottie export fidelity (map more properties, basic easing curves).
*   More accurate Canvas animation simulation for WebM export.
*   Ability to save and load user-created presets (using LocalStorage).
*   More text styling options (e.g., stroke, gradients).
*   Refactoring the code into separate HTML, CSS, and JS files for better maintainability.
*   Add option to choose export resolution/bitrate.

## Contributing

Contributions, issues, and feature requests are welcome! Please feel free to open an issue or submit a pull request.
