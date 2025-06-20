# Dynamic Window Algorithm - Interactive Visualization

A modern, interactive web-based visualization of the Dynamic Window Algorithm (DWA) for robot path planning and obstacle avoidance.

## 🚀 Live Demo

Open `index.html` in any modern web browser to start the interactive simulation immediately. No installation or setup required!

## ✨ Features

### 🎮 Interactive Controls
- **Click-to-Set Goal**: Simply click anywhere on the canvas to set a new target destination
- **Dynamic Obstacle Placement**: Switch to obstacle mode and click to add static or moving obstacles
- **Real-time Parameter Adjustment**: Use sliders to modify algorithm parameters during simulation
- **Mode Switching**: Toggle between goal-setting and obstacle-placement modes

### 🎨 Visual Elements
- **Animated Robot**: Green circle with directional indicator showing current heading
- **Goal Visualization**: Blue target with animated halo effect
- **Obstacle Types**: 
  - Red circles for static obstacles
  - Orange circles for moving obstacles with velocity vectors
- **Path Tracking**: Semi-transparent green trail showing robot's actual path
- **Predictive Planning**: Blue dashed line showing the algorithm's planned trajectory
- **Interactive Grid**: Coordinate grid for precise positioning

### ⚙️ Configurable Parameters
- **Robot Constraints**: Max velocities, robot radius
- **Planning Parameters**: Prediction horizon, time step
- **Obstacle Properties**: Default radius and velocity settings
- **Real-time Updates**: All parameters can be adjusted during simulation

### 🎯 Algorithm Visualization
- **Dynamic Window Planning**: Visual representation of trajectory evaluation
- **Collision Avoidance**: Real-time obstacle detection and avoidance behavior
- **Goal-Oriented Navigation**: Optimized pathfinding toward target destinations

## 🛠️ Technical Implementation

### Core Algorithm
- **JavaScript Implementation**: Faithful port of the Java Dynamic Window Algorithm
- **Real-time Planning**: 60 FPS simulation with smooth animations
- **Collision Detection**: Circular collision boundaries with predictive checking
- **Trajectory Evaluation**: Multi-criteria scoring (goal distance, collision avoidance)

### Modern Web Technologies
- **Pure HTML5/CSS3/JavaScript**: No external dependencies
- **Canvas API**: High-performance 2D rendering
- **CSS Grid & Flexbox**: Responsive layout design
- **Modern CSS**: Gradients, blur effects, and smooth animations

## 📁 File Structure

```
dwa-visualization/
│
├── index.html          # Main HTML file with embedded CSS and JavaScript
│
└── README.md          # This documentation file
```

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional software installation required

### Running the Visualization

1. **Download the HTML file**
2. **Open in browser**: Double-click `index.html` or drag it into your browser
3. **Start exploring**: The simulation is ready to use immediately!

### Basic Usage

1. **Set a Goal**:
   - Ensure "Set Goal" mode is selected (default)
   - Click anywhere on the canvas to place the blue goal marker

2. **Add Obstacles**:
   - Click "Add Obstacle" mode button
   - Click on the canvas to place obstacles
   - Obstacles will have random velocities (orange = moving, red = static)

3. **Adjust Parameters**:
   - Use the sliders in the right panel to modify algorithm behavior
   - Changes take effect immediately

4. **Run Simulation**:
   - Click "Start Simulation" to begin robot navigation
   - Use "Pause/Resume" to control playback
   - "Reset" returns robot to starting position

## 🎛️ Control Panel Guide

### Mode Selector
- **Set Goal**: Click canvas to place target destination
- **Add Obstacle**: Click canvas to add circular obstacles

### Robot Parameters
- **Max Linear Velocity** (0.1 - 2.0 m/s): Maximum forward speed
- **Max Angular Velocity** (0.1 - 2.0 rad/s): Maximum turning rate
- **Robot Radius** (0.1 - 1.0 m): Size for collision detection

### Planning Parameters
- **Prediction Time** (0.5 - 5.0 s): How far ahead the algorithm plans
- **Time Step** (0.05 - 0.2 s): Temporal resolution of predictions

### Obstacle Parameters
- **Default Radius** (0.1 - 1.0 m): Size of new obstacles
- **Default Velocity** (0.0 - 0.5 m/s): Speed range for moving obstacles

### Control Buttons
- **Start Simulation**: Begin robot navigation
- **Pause/Resume**: Toggle simulation playback
- **Reset**: Return robot to starting position and clear path
- **Clear Obstacles**: Remove all obstacles from environment

## 🎨 Visual Legend

| Element | Color | Description |
|---------|-------|-------------|
| 🟢 **Robot** | Green | Current robot position with heading indicator |
| 🔵 **Goal** | Blue | Target destination with animated halo |
| 🔴 **Static Obstacle** | Red | Stationary circular obstacles |
| 🟠 **Moving Obstacle** | Orange | Dynamic obstacles with velocity vectors |
| 🟢 **Robot Path** | Light Green | Historical trail of robot movement |
| 🔵 **Predicted Path** | Dashed Blue | Algorithm's planned trajectory |
| ⚪ **Grid** | Light Gray | Coordinate reference grid |

## ⚡ Performance Features

### Optimization
- **Efficient Rendering**: Canvas-based graphics with optimized drawing
- **Smooth Animation**: 60 FPS simulation loop
- **Memory Management**: Limited path history to prevent memory leaks
- **Responsive Design**: Adapts to different screen sizes

### Browser Compatibility
- **Chrome**: Full support with hardware acceleration
- **Firefox**: Complete functionality
- **Safari**: Full compatibility
- **Edge**: Modern Edge versions supported

## 🔧 Customization

### Modifying Algorithm Parameters
Edit the JavaScript `params` object in the HTML file:

```javascript
let params = {
    maxV: 1.0,                    // Maximum linear velocity
    maxOmega: Math.PI / 4,        // Maximum angular velocity
    dt: 0.1,                      // Time step
    predictTime: 2.0,             // Prediction horizon
    robotRadius: 0.5,             // Robot radius
    obstacleRadius: 0.5,          // Default obstacle radius
    obstacleVelocity: 0.1         // Default obstacle velocity
};
```

### Styling Customization
Modify the CSS section for visual appearance:

```css
/* Robot color */
.robot { fill: #4CAF50; }

/* Goal color */
.goal { fill: #2196F3; }

/* Background gradient */
body { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
```

### Adding New Features

1. **Custom Obstacle Shapes**: Extend the obstacle drawing function
2. **Different Robot Types**: Modify robot visualization
3. **Environment Elements**: Add walls, corridors, or terrain
4. **Data Export**: Save simulation data or screenshots

## 📊 Algorithm Details

### Dynamic Window Implementation
- **Velocity Sampling**: Discretized search space of feasible velocities
- **Trajectory Prediction**: Forward simulation over prediction horizon
- **Multi-Criteria Evaluation**: Balanced scoring of goal proximity and safety
- **Real-time Optimization**: Continuous replanning at high frequency

### Performance Characteristics
- **Planning Frequency**: ~60 Hz (browser dependent)
- **Trajectory Samples**: ~400 velocity combinations evaluated per cycle
- **Prediction Steps**: 20-50 steps per trajectory (parameter dependent)
- **Obstacle Handling**: Unlimited dynamic obstacles supported

## 🐛 Troubleshooting

### Common Issues

1. **Slow Performance**:
   - Reduce prediction time or increase time step
   - Limit number of obstacles
   - Close other browser tabs

2. **Robot Won't Move**:
   - Check if goal is set (blue circle visible)
   - Ensure simulation is started (green status)
   - Verify robot isn't trapped by obstacles

3. **Parameters Not Updating**:
   - Sliders update immediately - try moving them
   - Reset simulation if behavior seems stuck

4. **Browser Compatibility**:
   - Use modern browser versions
   - Enable JavaScript if disabled
   - Try different browser if issues persist

## 🔮 Future Enhancements

### Planned Features
- **Multi-Robot Simulation**: Support for multiple robots
- **Environment Editor**: Advanced obstacle placement tools
- **Data Analytics**: Performance metrics and statistics
- **Export Functionality**: Save simulations and parameters
- **3D Visualization**: Three.js integration for 3D environments

### Community Contributions
- **Algorithm Variants**: Different planning algorithms
- **Visualization Modes**: Alternative display options
- **Performance Optimizations**: WebGL rendering, Web Workers
- **Educational Features**: Step-by-step algorithm explanation

## 📚 Educational Use

### Learning Objectives
- **Path Planning Concepts**: Understanding local planning algorithms
- **Real-time Systems**: Visualization of continuous planning
- **Parameter Tuning**: Effects of different algorithm settings
- **Robotics Applications**: Practical autonomous navigation
---
**Enjoy exploring the Dynamic Window Algorithm! 🤖✨**
