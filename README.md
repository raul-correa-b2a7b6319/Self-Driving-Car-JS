# Self-Driving Car JS

A self‑driving car simulation built in JavaScript. It implements:
- **Car mechanics** (acceleration, friction, steering) via `car.js`  
- **User controls & dummy traffic** via `controls.js` and `road.js`  
- **Ray‑casting sensors & collision detection** via `sensor.js` and polygon intersection utilities in `utils.js`  
- **Neural network “brain”** for autonomous driving in `network.js`  
- **Real‑time visualization** of both the car/world (`main.js`) and the network (`visualizer.js`)  
- Styling/layout in `index.html` and `style.css` :contentReference[oaicite:0]{index=0}

## Table of Contents

- [Demo Video](#demo-video)  
- [Features](#features)  
- [File Structure](#file-structure)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Contributing](#contributing)  
- [License](#license)  

## Demo Video

Here’s a walkthrough where I highlight some of my favorite parts of the program:

[![Watch the walkthrough](https://img.youtube.com/vi/DF9A-CowS_U/0.jpg)](https://youtu.be/DF9A-CowS_U)

## Features

- **Physics‑based Car Mechanics** (`car.js`)  
  - Implements acceleration, maximum speed, friction, and turning logic.  
- **Control Schemes** (`controls.js`)  
  - Keyboard input for manual drive and “dummy” mode for traffic cars.  
- **Road Generation & Traffic** (`road.js`)  
  - Draws lanes, borders, and populates dummy cars to navigate around.  
- **Sensor Simulation** (`sensor.js`)  
  - Casts rays to measure distance to road edges and other cars.  
- **Collision Detection & Utilities** (`utils.js`)  
  - Polygon intersections to detect crashes.  
- **Neural Network Driver** (`network.js`)  
  - Feedforward network with configurable layers and genetic‑style mutation.  
- **Visualization** (`visualizer.js`)  
  - Renders the network architecture and live weights/biases.  
- **Main Orchestration** (`main.js`)  
  - Initializes canvases, loads/saves the best brain, runs the animation loop.  

## File Structure

```plain
Self-Driving-Car-JS/
├── index.html       # Canvas setup & script imports  
├── style.css        # Basic page styling  
├── car.js           # Car physics, state, drawing  
├── controls.js      # Keyboard & dummy control logic  
├── road.js          # Road layout, lane centers, drawing  
├── sensor.js        # Ray‑casting sensor class  
├── network.js       # Neural network & level classes  
├── utils.js         # Helper functions (e.g. polygon intersection)  
├── visualizer.js    # Network visualization renderer  
└── main.js          # Initialization, animation loop, save/discard logic  
````

([GitHub][1])

## Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/raul-correa-b2a7b6319/Self-Driving-Car-JS.git
   cd Self-Driving-Car-JS
   ```

2. **Run locally**
   Open `index.html` directly in your browser, or serve via a simple HTTP server for full functionality (for example with Python):

   ```bash
   # Python 3
   python -m http.server 8000
   # then visit http://localhost:8000
   ```

## Usage

* **Manual Mode**

  * Use arrow keys to drive.
* **Autonomous Mode**

  * The AI “brain” takes over. It uses sensor readings to decide when to steer, accelerate, or brake.
* **Save/Load Best Brain**

  * Click the top button to save the current best network to `localStorage`.
  * Click the bottom button to discard it and start fresh.

## Contributing

Pull requests and issues are welcome. Please:

1. Fork the repository.
2. Create a feature branch.
3. Open a pull request detailing your changes.

## License

This project is licensed under the MIT License. Feel free to use and modify it as you see fit.

```
::contentReference[oaicite:2]{index=2}
```

[1]: https://github.com/raul-correa-b2a7b6319/Self-Driving-Car-JS/commit/3d286315f6870ad4c29798769f32d289c328a9b0 "Add files via upload · raul-correa-b2a7b6319/Self-Driving-Car-JS@3d28631 · GitHub"
