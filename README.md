#  Pupil Dynamics Calculator

An interactive, real-time simulation of human pupil response to **light intensity (luminance)** and **focus distance (accommodative near response)**. Built with pure HTML5 Canvas, CSS, and vanilla JavaScript.

![Pupil Calculator Demo](https://via.placeholder.com/800x400?text=Eye+Pupil+Simulation+Preview)

##  Overview

This tool visualizes how the human pupil constricts and dilates based on two primary physiological factors:

1. **Pupillary Light Reflex** – Pupils constrict in bright light and dilate in darkness.
2. **Near Triad (Accommodation)** – When focusing on nearby objects, pupils constrict slightly to increase depth of field.

Both eyes respond symmetrically, and the pupil size is displayed both visually (on canvas) and numerically (radius in pixels & area in mm²).

##  Features

- **Real-time pupil rendering** – Smooth, high-quality eye illustrations with dynamic pupil size.
- **Luminance slider** – Adjust from 0.1 lux (deep darkness) to 10,000 lux (bright sunlight).
- **Focus distance slider** – Set from 10 cm (very near) to 500 cm (far distance).
- **Physiological model** – Based on established pupil diameter ranges (2.0 mm – 8.0 mm).
- **Live metrics** – Displays current pupil radius (px), area (mm²), and effective diameter (mm).
- **Reset button** – Quickly return to typical indoor conditions (500 lux / 50 cm).
- **Fully responsive** – Works on desktop, tablet, and mobile devices.
- **No dependencies** – Pure HTML/CSS/JS, no external libraries.

##  Physiological Model Explained

### Luminance → Pupil Diameter
The model maps luminance (lux) to pupil diameter using a logarithmic response curve:

| Luminance Level | Typical Diameter |
|-----------------|------------------|
| 0.1 lux (dark)  | ≈ 7.5 mm         |
| 500 lux (indoor)| ≈ 4.0 mm         |
| 10,000 lux (sun)| ≈ 2.5 mm         |

A non-linear transfer function simulates the rapid constriction at moderate light levels.

### Focus Distance Modifier
Near focus causes additional constriction (miosis) as part of the **near triad**:
- Up to **22% reduction** in diameter when focusing at 10 cm.
- No additional constriction beyond 400 cm.

### Final Diameter Range
- **Minimum:** 2.0 mm (bright light + far focus)
- **Maximum:** 8.0 mm (darkness + far focus, or dark + near focus with limited constriction)

All values stay within physiological boundaries.

##  Live Demo

You can try the calculator online here:  
**[Pupil Dynamics Calculator – Live Demo](https://your-username.github.io/pupil-calculator)**  
*(Replace with actual GitHub Pages link after deployment)*

##  Usage

1. **Adjust Luminance** – Drag the "Luminance (lux)" slider to simulate different lighting environments.
2. **Adjust Focus Distance** – Drag the "Focus Distance (cm)" slider to simulate looking at near or far objects.
3. **Observe Changes** – The eyes update instantly. Numerical values show precise pupil radius and area.
4. **Reset** – Click the "Reset" button to return to standard indoor lighting and desk distance.

##  Project Structure

```
pupil-calculator/
├── index.html          # Main application file (HTML/CSS/JS)
└── README.md           # This file
```

##  Installation & Local Development

To run this project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pupil-calculator.git
   ```
2. Navigate to the project folder:
   ```bash
   cd pupil-calculator
   ```
3. Open `index.html` in any modern web browser.
   - No build steps, servers, or dependencies required.

##  Customization

You can easily tweak the physiological model by editing the JavaScript functions in `index.html`:

- `luminanceToDiameter(lux)` – Modify the luminance response curve.
- `focusModifier(distanceCm)` – Adjust near-response constriction strength.
- `MIN_PUPIL_RADIUS_PX` and `MAX_PUPIL_RADIUS_PX` – Change visual scaling.

## 📊 Example Scenarios

| Scenario               | Luminance | Focus Distance | Pupil Diameter |
|------------------------|-----------|----------------|----------------|
| Dark room, far object  | 0.1 lux   | 500 cm         | ≈ 7.8 mm       |
| Reading under lamp     | 500 lux   | 30 cm          | ≈ 3.4 mm       |
| Bright sunlight        | 10,000 lux| 200 cm         | ≈ 2.3 mm       |
| Night driving          | 5 lux     | far (500 cm)   | ≈ 6.5 mm       |

##  Contributing

Contributions are welcome! If you have ideas for improving the model, adding new features (e.g., anisocoria simulation, pharmacological effects), or enhancing the UI, feel free to:

- Open an issue to discuss changes.
- Submit a pull request with your improvements.

##  License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute it for personal or commercial purposes.

##  Contact

Om Gedam

GitHub: [https://github.com/itsomg134](https://github.com/itsomg134)

Email: [omgedam123098@gmail.com](mailto:omgedam123098@gmail.com)

Twitter (X): [https://twitter.com/omgedam](https://twitter.com/omgedam)

LinkedIn: [https://linkedin.com/in/omgedam](https://linkedin.com/in/omgedam)

Portfolio: [https://ogworks.lovable.app](https://ogworks.lovable.app)
