# Symphonic-AI
Symphonic AI allows you to conduct a virtual orchestra using only your web browser &amp; webcam.

It uses [Posenet] to detect your body pose, and from that how fast you are moving your hands. Using this data and the [Tone.js] web audio library, it plays real samples of orchestral instruments playing individual notes at the speed of your conducting, which play live from a score you that can edit.

## Quick Start

```sh
yarn  # Install dependencies
```
```sh
yarn start  # Start a local dev server
```
```sh
yarn build  # Build static site into the /dist folder
```

## Code Structure

Symphonic AI is built in vanilla JS without a framework. Each JS file in the `/scripts` folder contains a class module, with each class controlling one portion of the app (also there are some helper files with useful functions). It's designed so that modules can be used or deleted according to how you want to remix the app.

- `main.js` controls the primary app state & functions, including loading the app and instantiating the other classes
- `renderer.js` handles all the UI/DOM updating
- `orchestra.js` controls the graphic of the orchestra, made with PIXI.js
- `pose-controller.js` uses TFJS to get the pose state from the webcam with Posenet
- `posenet-renderer.js` renders the pose skeleton in the interface
- `audio-player.js` handles the MIDI playback & loading of samples using Tone.js