# flappy_Bird

![stable-release](https://img.shields.io/badge/flappy_bird-Developing-da282a)
![starts](https://shields.io/github/stars/JYe9/flappy_bird)

## Overview

This is a simplified implementation of the classic game Flappy Bird using Rust programming language and the `bracket-lib` crate for terminal-like window rendering and input handling. The game involves controlling a bird to navigate through obstacles by tapping the spacebar to avoid collisions.

## Getting Started

### Prerequisites

- Rust programming language installed on your system.
- Basic knowledge of Rust syntax and concepts.

### Installation

1. Clone the repository containing the game code.

2. Ensure you have the `bracket-lib` crate added as a dependency in your Cargo.toml file:

   ```
   tomlCopy code[dependencies]
   bracket-lib = "~0.8.7"
   ```

3. Run the game using `cargo run`.

## Game Mechanics

- **Objective**: Control the bird's flight to pass through openings between obstacles without hitting them.
- **Controls**: Press the spacebar to make the bird flap and gain altitude.

## Code Structure

The game code consists of several components:

1. **Enums and Constants**:
   - `GameMode`: Represents the different states of the game (Menu, Playing, End).
   - `SCREEN_WIDTH` and `SCREEN_HEIGHT`: Define the dimensions of the game window.
   - `FRAME_DURATION`: Specifies the duration for each frame.
2. **Structs**:
   - `Player`: Contains information about the player's position and movement.
   - `State`: Manages the game state, player, frame time, game mode, obstacles, and score.
   - `Obstacle`: Represents the obstacles in the game that the player needs to avoid.
3. **Implementations**:
   - `impl Player`: Defines methods for player creation, rendering, gravity/movement, and flapping.
   - `impl State`: Implements game functionalities like game initialization, gameplay, restarting, and menus.
   - `impl GameState for State`: Implements the trait for the game state, defining how the game progresses over time.
4. **Main Function**:
   - `main()`: Sets up the game context using `BTermBuilder`, initializes the main loop, and starts the game with a new state.

## Game Flow

1. **Initialization**:
   - Creates a new game state and sets up the initial values.
2. **Game Loop (`tick()`)**:
   - Depending on the game mode, calls the appropriate functions (`main_menu()`, `play()`, or `dead()`).
3. **Input Handling**:
   - Listens for specific keyboard inputs (`P` to play, `Q` to quit) in menu and end screens.
4. **Rendering**:
   - Renders the game elements like the player, obstacles, score, and menu texts.

## TODO List

### Graphics Enhancement

- [ ]  **Add New Bird Images**: Replace the current bird icon with new images for different bird skins.
- [ ] **Change Obstacle to an Image**: Replace the brick-like obstacles with images representing different obstacles.
- [ ] **Add Background**: Implement a background image or color scheme to enhance the visual appeal of the game.

### Game Features

- [ ] **Implement Multiple Levels**: Allow players to choose different levels with varying difficulty.
- [ ] **Add Coins as Rewards**: Introduce coins as rewards collected during gameplay.
- [ ] **Implement Bird Skins**: Enable players to use earned coins to purchase different skins for the bird.
- [ ] **Add Music**: Add music to the game during gameplay.

## Conclusion

This implementation provides a basic Flappy Bird game structure using Rust and `bracket-lib`. You can explore and expand upon this code to add more features, improve graphics, or introduce additional challenges to the gameplay.
