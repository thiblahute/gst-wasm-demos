# GStreamer WASM demos

GStreamer and GStreamer Editing Services (GES) running in the browser through
WebAssembly (Emscripten): WebCodecs for decoding, WebGL for compositing.

- [GES GL compositing](https://thiblahute.github.io/gst-wasm-demos/ges-launch.html?validate-test=ges/gl_compositing.validatetest):
  a multi-layer timeline with animated overlays, keyframes and GL effects
  (fisheye, glow, bulge, blur), composited through `glvideomixerelement`
- [Simple compositing](https://thiblahute.github.io/gst-wasm-demos/ges-launch.html?validate-test=ges/gl_compositing_simple.validatetest):
  two layers, a bouncing ball animated with keyframes

Use a recent Chrome. The page reloads once to enable cross-origin isolation
(`coi-serviceworker.js`), which the threaded WebAssembly build needs.

This is a build of GStreamer (LGPL-2.1-or-later), see
https://gitlab.freedesktop.org/gstreamer/gstreamer. The demos are `.validatetest`
files run by the GstValidate runner built for the browser.
