<<<<<<< HEAD
# Diamond Frenzy

A 2D arcade-style game built using OpenGL and Python where players catch falling diamonds to score points.

## Description

Diamond Frenzy is an interactive graphics game developed as part of CSE423 Computer Graphics Lab. The game features smooth animations, collision detection, and progressively increasing difficulty. Players control a catcher to collect colorful diamonds falling from the sky while avoiding game-ending misses.

## Features

- Real-time diamond catching gameplay
- Progressive difficulty scaling with score
- Smooth OpenGL-rendered graphics using Bresenham's line algorithm
- Interactive game controls (play, pause, restart)
- Dynamic color generation for diamonds
- Collision detection system
- Score tracking and display

## Technical Implementation

### Graphics Rendering
- Custom implementation of Bresenham's line drawing algorithm
- Zone-based coordinate conversion for optimal line rendering
- OpenGL point and line primitives for shape construction
- Double buffering for smooth animation

### Game Mechanics
- Physics-based diamond falling animation
- Boundary collision detection
- Real-time input handling for player movement
- Game state management (playing, paused, game over)

### Libraries Used
- **PyOpenGL**: OpenGL bindings for Python
- **PyOpenGL_accelerate**: Performance optimization for OpenGL operations
- **random**: Random number generation for diamond positioning and colors

## Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/nihal-kabir/CSE423-Computer-Graphics-Lab.git
cd "CSE423-Computer-Graphics-Lab/Solo Project 2"
```

2. Create a virtual environment (recommended):
```bash
python -m venv .venv
```

3. Activate the virtual environment:
- Windows: `.venv\Scripts\activate`
- macOS/Linux: `source .venv/bin/activate`

4. Install required dependencies:
```bash
pip install PyOpenGL PyOpenGL_accelerate
```

## Usage

Run the game using Python:
```bash
python "solo 2.py"
```

## Game Controls

### Keyboard Controls
- **Left Arrow Key**: Move catcher left
- **Right Arrow Key**: Move catcher right

### Mouse Controls
- **Top-left corner**: Restart the game
- **Top-center**: Toggle pause/resume
- **Top-right corner**: Exit the game

## Gameplay

1. **Objective**: Catch falling diamonds with your catcher to earn points
2. **Scoring**: Each successfully caught diamond increases your score by 1
3. **Difficulty**: Game speed increases with each point scored
4. **Game Over**: Missing a diamond (letting it fall past the bottom) ends the game
5. **Features**: 
   - Diamonds appear in random colors and positions
   - Catcher movement is constrained within game boundaries
   - Real-time score display in console

## Code Structure

### Core Components

- **Line Drawing Algorithm**: Custom Bresenham's implementation with zone conversion
- **Display Function**: Handles all rendering operations and game state visualization
- **Animation System**: Controls diamond movement and game timing
- **Input Handlers**: Processes keyboard and mouse interactions
- **Collision Detection**: Manages diamond-catcher collision events
- **Game State Management**: Handles play, pause, restart, and exit functionality

### Key Functions

- `drawLine()`: Implements Bresenham's line algorithm
- `display()`: Main rendering function
- `diamond_animation()`: Handles game physics and updates
- `check_collision()`: Detects catcher-diamond intersections
- `mouseListener()`: Processes mouse click events
- `specialKeyListener()`: Handles keyboard input

## Game Configuration

- **Window Size**: 500x500 pixels
- **Initial Diamond Speed**: 0.4 units per frame
- **Speed Increment**: 0.1 units per score point
- **Catcher Speed**: 20 units per key press
- **Diamond Size**: 40x60 pixel collision box
- **Catcher Size**: 80x30 pixel collision box

## Development

This project was developed as part of CSE423 Computer Graphics Lab coursework, focusing on:
- Computer graphics fundamentals
- Line drawing algorithms implementation
- Real-time rendering techniques
- Game development with OpenGL
- Event-driven programming

## System Requirements

- **Operating System**: Windows, macOS, or Linux
- **Python Version**: 3.7+
- **Graphics**: OpenGL-compatible graphics card
- **Memory**: Minimum 256MB RAM
- **Display**: Minimum 800x600 resolution

## Author

Developed by Nihal Kabir for CSE423 Computer Graphics Lab.

## Course Information

- **Course**: CSE423 - Computer Graphics Lab
- **Project Type**: Solo Project 2
- **Focus**: Interactive Graphics and Game Development

## License

This project is developed for educational purposes as part of university coursework.
=======
# Twin Invaders

A classic space shooter game implemented in Python using OpenGL. Defend Earth from alien invaders by controlling a spacecraft and shooting down enemies while avoiding their attacks.

<div align="center">
  <img src="423-p.png" alt="Twin Invaders Game Screenshot" width="600"/>
</div>

<div align="center">
  <h3><a href="https://surli.cc/euliul">🎮 YouTube</a></h3>
</div>

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [How to Play](#how-to-play)
- [Game Controls](#game-controls)
- [Game Mechanics](#game-mechanics)
- [Technical Implementation](#technical-implementation)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

Twin Invaders is a 2D space shooter game developed as part of the CSE423 Computer Graphics Lab course. The game features classic arcade-style gameplay where players control a spacecraft to eliminate alien invaders while managing limited lives and achieving high scores.

## Features

- **Classic Arcade Gameplay**: Navigate and shoot in a retro-style space shooter environment
- **Dynamic Enemy AI**: Aliens move horizontally and fire projectiles at the player
- **Progressive Difficulty**: Multiple bullet patterns and increasing challenge levels
- **Life System**: Three lives with visual heart indicators
- **Score Tracking**: Real-time score display based on alien eliminations
- **Game State Management**: Play, pause, restart, and exit functionality
- **Smooth Graphics**: OpenGL-rendered graphics with fluid animations
- **Responsive Controls**: Keyboard and mouse input support

## Requirements

- Python 3.7 or higher
- OpenGL support
- Windows/Linux/macOS compatible

### Required Python Packages

- PyOpenGL
- PyOpenGL_accelerate

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/nihal-kabir/CSE423-Computer-Graphics-Lab.git
   cd CSE423-Computer-Graphics-Lab
   ```

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required packages**:
   ```bash
   pip install PyOpenGL PyOpenGL_accelerate
   ```

4. **Run the game**:
   ```bash
   python 423_project.py
   ```

## How to Play

The objective is to eliminate all alien invaders while avoiding their projectiles. You control a spacecraft at the bottom of the screen and must survive waves of alien attacks.

### Game Controls

| Control | Action |
|---------|--------|
| Left Arrow | Move spacecraft left |
| Right Arrow | Move spacecraft right |
| Spacebar | Fire bullets |
| P Key | Pause/Resume game |
| Mouse Click | Interact with UI elements |

### Game Mechanics

- **Lives**: Start with 3 lives (displayed as hearts)
- **Scoring**: Gain points by destroying alien invaders
- **Weapons**: Multiple bullet patterns unlock as you progress
- **Enemy Behavior**: Aliens move horizontally and shoot downward
- **Collision Detection**: Bullets and spacecraft interact with enemies and obstacles

## Technical Implementation

### Graphics Engine
- **OpenGL**: Hardware-accelerated 2D graphics rendering
- **GLUT**: Window management and input handling
- **Custom Rendering**: Hand-coded geometric shapes and animations

### Key Components

- **Renderer**: OpenGL-based drawing functions for all game objects
- **Physics Engine**: Collision detection and movement calculations
- **Game State Manager**: Handles play/pause/restart/exit states
- **Input Handler**: Keyboard and mouse event processing
- **Animation System**: Smooth object movement and visual effects

### Code Architecture

- **Modular Design**: Separate functions for different game components
- **Global State Management**: Efficient variable handling for game state
- **Event-Driven Programming**: Responsive input and animation loops
- **Real-time Rendering**: Continuous screen updates for smooth gameplay

## Project Structure

```
Twin Invaders/
│
├── 423_project.py          # Main game file
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies (if created)
```

### Key Functions

- `show_screen()`: Main rendering loop
- `animate()`: Game logic and object updates
- `keyboardListener()`: Keyboard input handling
- `mouseListener()`: Mouse input processing
- `specialKeyListener1()`: Special key combinations
- Rendering functions for game objects (shooter, bullets, aliens, UI)

## Game Features Detail

### Visual Elements
- Spacecraft with customizable colors
- Animated bullet projectiles
- Moving alien enemies with directional AI
- UI elements (hearts, score, control buttons)
- Background and border graphics

### Audio-Visual Feedback
- Real-time score updates
- Visual life indicators
- Game state notifications
- Smooth animations and transitions

## Development Notes

This project demonstrates fundamental computer graphics concepts including:
- 2D coordinate systems and transformations
- Real-time rendering and animation
- Event-driven programming
- Collision detection algorithms
- Game state management
- OpenGL programming in Python

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Bug fixes
- Feature enhancements
- Code optimizations
- Documentation improvements

## License

This project is developed for educational purposes as part of the CSE423 Computer Graphics Lab course. Feel free to use and modify for learning purposes.

---

**Course**: CSE423 - Computer Graphics Lab  
**Institution**: BRAC University  
**Developer**: [Lawrence Amlan Gomes](https://github.com/Lawrence-Amlan-Gomes), A K M Nihalul Kabir, [Hasan Sarwar Zami](https://github.com/noobcoder-hasan)  
**Academic Year**: 2024
>>>>>>> 33b50638e0f0421e9f387f86f021287b1700b1da
