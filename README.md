Symphonic AI

Symphonic AI allows you to conduct a virtual orchestra using only your web browser and webcam. It uses [PoseNet] to detect body movements and [Tone.js] for real-time orchestral sound playback. Move your hands to control the tempo and play an interactive symphony!

🚀 Features

🎼 Conduct an orchestra with hand movements

📷 Uses PoseNet for real-time body pose detection

🎵 Plays orchestral instrument samples dynamically

🎹 Customizable score editing

⚡ Built with Vanilla JS, TFJS, PIXI.js, and Tone.js

🛠 Quick Start

yarn  # Install dependencies
yarn start  # Start a local development server
yarn build  # Build the static site into the /dist folder

📁 Code Structure

Symphonic AI is built with vanilla JavaScript, without a framework. The main logic is divided into modular classes in the /scripts folder:

`` – Controls the primary app state and initializes modules.

`` – Manages UI and DOM updates.

`` – Renders the orchestra visualization using PIXI.js.

`` – Uses TensorFlow.js (TFJS) and PoseNet for body tracking.

`` – Displays the detected pose skeleton in the interface.

`` – Handles MIDI playback and orchestral sample loading with Tone.js.




- `audio-player.js` handles the MIDI playback & loading of samples using Tone.js
