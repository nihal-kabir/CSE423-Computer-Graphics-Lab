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
pip install -r requirements.txt
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
