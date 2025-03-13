# Interactive Water Ripple Effect

A WebGL-based interactive web animation that creates realistic water ripple effects following cursor movement. The effect distorts both text and background imagery, creating an engaging visual experience.

![Demo Preview](demo.gif)

## Features

-   Real-time water ripple simulation using WebGL shaders
-   Mouse-tracked ripple effect
-   Responsive design that scales with window size
-   Distortion effects on both text and background image
-   Smooth animation with optimized performance

## Technical Implementation

### Core Technologies

-   Three.js for WebGL rendering
-   Custom GLSL shaders for water simulation
-   HTML5 Canvas for text rendering
-   Responsive CSS layout

### How It Works

1. **Wave Simulation**

    - Uses a fragment shader implementing the wave equation
    - Simulates pressure and velocity in a 2D texture
    - Updates at 60fps for smooth animation

2. **Rendering Pipeline**

    - Dual render targets for ping-pong texture updates
    - Combines background image, text, and ripple effect
    - Applies specular lighting for realistic water appearance

3. **Interaction**
    - Tracks mouse movement across the screen
    - Converts cursor position to shader coordinates
    - Creates ripple disturbance at cursor location

## Setup

1. Clone the repository:

```bash
git clone https://github.com/yourusername/water-ripple-effect
```

2. Install dependencies:

```bash
npm install
```

3. Run the development server:

```bash
npm run dev
```

## Project Structure

```
├── index.html          # Main HTML file
├── styles.css          # Global styles
├── script.js          # Main JavaScript with Three.js setup
├── shaders.js         # GLSL shader code
└── images/            # Project images
```

## Customization

### Adjusting Ripple Physics

Modify these values in `shaders.js`:

-   `delta`: Controls wave speed (default: 1.4)
-   `pressure`: Affects ripple intensity
-   `pVel`: Changes wave velocity

### Styling

-   Text color: Modify `ctx.fillStyle` in `script.js`
-   Background: Replace `/images/s5.jpg` with your image
-   UI elements: Adjust styles in `styles.css`

## Performance Considerations

-   Uses `requestAnimationFrame` for optimal rendering
-   Implements texture size scaling based on device pixel ratio
-   Optimizes shader calculations for efficiency

## Browser Support

-   Chrome 90+
-   Firefox 88+
-   Safari 14+
-   Edge 90+

Requires WebGL support and modern JavaScript features.

## Known Limitations

-   High GPU usage on complex backgrounds
-   Mobile performance may vary
-   Limited touch device optimization

## Future Improvements

-   [ ] Add touch support for mobile devices
-   [ ] Implement WebGL2 features for better performance
-   [ ] Add shader quality settings for lower-end devices
-   [ ] Integrate with glslify for better shader management

## Credits

-   Three.js - <https://threejs.org/>
-   Inter Font - <https://rsms.me/inter/>
-   Original concept inspired by various WebGL water simulations

## License

MIT License - feel free to use in your own projects.

---

Created by Khoa Nguyen
