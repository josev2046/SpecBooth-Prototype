# SpecTape (Prototype)

> **⚠️ NOTE: RAPID PROTOTYPE / PROOF OF CONCEPT**
> This repository contains a "quick and dirty" HTML/JS implementation designed to validate the User Experience (UX) for a future native iOS application. The code prioritises immediate visual feedback over clean architecture. It is not intended for production use.

## The vision

**SpecTape** is an exploration of "slow photography" through the lens of 1980s computing nostalgia.

In an era of instant, high-definition photography, SpecTape forces the user to wait. It recreates the visceral, tactile, and often anxious experience of loading software from a cassette tape on a ZX Spectrum.

**The core loop:**
1.  **Capture:** The user takes a photo.
2.  **The wait (the "Tape Loading" experience):** The app does not show the image immediately. Instead, it simulates a 2-minute tape loading sequence, complete with:
    * Generative square-wave audio (Pilot tones and Data crunching).
    * Accurate border colour flashing (Red/Cyan for pilot, Blue/Yellow for data).
    * Line-by-line raster rendering of the image.
3.  **The Result:** A mathematically accurate ZX Spectrum graphical conversion (256x192 pixels, 2 colours per 8x8 block).

## Tech stack (Prototype)

This POC is built as a single-file Progressive Web App (PWA) to allow for installation on iOS devices without TestFlight.

* **Engine:** Vanilla JavaScript.
* **Image Processing:** Custom block-processing logic mimicking the ZX Spectrum ULA chip + `Pixels.js` for vintage filtering.
* **Audio:** Web Audio API (Oscillators) for real-time generative sound synthesis (no audio files used).
* **Composite Rendering:** A multi-layered canvas approach (Attributes + Bitmap) flattened into a scanline buffer.


## Future roadmap (Native app)

The final version of this application will be rewritten in **Swift** and **Metal** for iOS.

* **Real-time viewfinder:** Using Metal shaders to preview the Spectrum effect live before capture.
* **Haptic integration:** Using CoreHaptics to vibrate the phone in sync with the "data crunching" audio.
* **Social export:** Generating `.gif` or `.mp4` video of the loading sequence to share on social media.

