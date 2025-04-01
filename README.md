# Text Animation Studio

A fun, interactive web-based tool to create custom text animations using HTML, CSS, and the powerful Anime.js library. Experiment with various presets, fonts, colors, and export your creations!

**Try it live here:** 👉 [**https://kavindus1.github.io/Text-Animator**](https://kavindus1.github.io/Text-Animator) 👈


![download (4)](https://github.com/user-attachments/assets/7ed81312-6cde-4a54-9a40-a4322336fbbe)

![pixlo_elasticPop](https://github.com/user-attachments/assets/747a7aae-109c-411e-b56f-89e277f4946b)

## ✨ Features

*   **Custom Text Input:** Animate any text you like.
*   **Extensive Animation Presets:** Choose from a wide variety of entrance, exit, and emphasis animations powered by Anime.js (Staggering, Fading, Flipping, Bouncing, Complex Effects, and more!).
*   **Rich Font Selection:** Select from a large collection of Google Fonts (Sans-Serif, Serif, Monospace, Display, Script, etc.).
*   **Color Palette Presets:** Easily apply pre-defined color schemes for text and background (High Contrast, Themed, Monochromatic, etc.).
*   **Letter Spacing Control:** Fine-tune the spacing between characters using a slider.
*   **Toggle Text Effects:** Enable or disable text glow/shadow effects with a simple checkbox.
*   **Live Preview:** See your animation changes reflected instantly in the preview area.
*   **MP4 Export (Experimental):** Export your animation as a `.webm` video file (commonly playable as MP4) using the browser's built-in `MediaRecorder` and Canvas API.
*   **Single File Structure:** The entire application (HTML, CSS, JS) is contained within a single HTML file for simplicity.

## 🚀 How to Use

1.  **Visit the Live Demo:** Go to [https://kavindus1.github.io/Text-Animator](https://kavindus1.github.io/Text-Animator).
2.  **Enter Text:** Type your desired text into the "Logo Text" input field.
3.  **Customize:**
    *   Select an **Animation** preset from the dropdown.
    *   Adjust the **Spacing** using the slider.
    *   Choose a **Font** from the extensive list.
    *   Select **Text Color** and **Background** color palettes.
    *   Check/uncheck **Enable Text Effects** for glow/shadow.
4.  **Preview:** Click the **"Apply & Animate"** button to see the animation applied to your text in the top preview area.
5.  **Export (Optional):**
    *   Click the **"Export MP4"** button.
    *   The tool will render the animation on a hidden canvas and record it. This process takes a few seconds, depending on the animation duration.
    *   A `.webm` video file will be automatically downloaded. *(See Limitations below regarding export quality)*.

## 🛠️ Technologies Used

*   **HTML5:** For structure and semantic markup.
*   **CSS3:** For styling, layout (Flexbox, Grid), transitions, and CSS Variables for theming.
*   **JavaScript (ES6+):** For DOM manipulation, event handling, logic, and controlling the animation/export process.
*   **[Anime.js](https://animejs.com/):** A lightweight and powerful JavaScript animation library used for the DOM-based animations in the preview.
*   **Canvas API:** Used for rendering the animation frames during the MP4 export process.
*   **MediaRecorder API:** Used to capture the canvas stream and create the `.webm` video file for export.

## ⚠️ Limitations & Known Issues

*   **MP4 Export Fidelity:** The MP4/WebM export relies on rendering the animation onto an HTML Canvas. This canvas rendering is a **simplified simulation** of the original Anime.js DOM animation. Complex physics, advanced easing, and some 3D transforms present in the live preview **will not be perfectly replicated** in the exported video. The export aims to capture the *basic concept* of the selected animation.
*   **APNG Export:** Direct client-side APNG export for complex animations is technically challenging and not implemented in this tool.
*   **Browser Support:** Core features work in modern browsers (Chrome, Firefox, Edge, Safari). The MP4 export relies on the `MediaRecorder` and `captureStream` APIs, which might not be available in older browsers.
*   **Animation Preset Complexity:** While efforts were made to ensure presets work correctly, some very complex Anime.js animations or interactions between specific settings might occasionally produce slightly unexpected results in the DOM preview.
*   **Single File Structure:** While convenient for a demo, containing everything in one large HTML file is not standard practice for larger, maintainable web applications.

## 🤝 Contributing

Found a bug or have a suggestion for a new feature or preset? Feel free to open an issue on the [GitHub repository issues page](https://github.com/kavindus1/Text-Animator/issues)!
