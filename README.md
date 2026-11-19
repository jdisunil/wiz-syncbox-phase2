# WiZ Sync Box — Phase 2

A free iPhone Safari prototype for camera-based colour sampling of a TV screen. No lights are controlled in this phase.

## Publish
1. Open the `wiz-syncbox` GitHub repository.
2. Replace the root `index.html` with this version and commit to `main`.
3. Wait for GitHub Pages deployment, then refresh the existing HTTPS URL on your iPhone (close/reopen Safari if needed).

## Test
1. Start camera and allow permission.
2. Place the iPhone facing the TV with all four corners visible.
3. Tap the four TV picture corners on the camera preview in this exact order: top-left, top-right, bottom-right, bottom-left.
4. Watch the eight colour tiles while a colourful video plays. Change update interval and smoothing.
5. Recalibrate if the iPhone moves. Calibration is saved locally in Safari.

## Technical notes
- Colour sampling uses a bilinear mapping between the four selected corners. It approximates perspective but does not perform full homography correction.
- The eight colour zones sample small areas near screen edges, not the entire image.
- Browser video processing stops when the page is backgrounded.
- Safari cannot directly transmit WiZ local UDP commands; Phase 3 requires a separate validated communication method.
