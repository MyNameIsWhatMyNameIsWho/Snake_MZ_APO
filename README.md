# Snake Game

## Introduction
Snake Game is a classic arcade game designed for a Linux-based operating system, tested on Debian. Developed in C programming language, it provides a nostalgic gaming experience where players control a snake to consume apples and achieve high scores. The game supports both single and two-player modes, allowing players to compete for the highest score.

## System Requirements
- Linux-based operating system (tested on Debian)
- C programming environment
- MZ_APO libraries for controlling peripherals (LEDs, knobs, LCD display, etc.)
- MZ_APO microcontroller

## Installation and Execution
1. Install required MZ_APO libraries and dependencies.
2. Compile and run the Snake Game code using a C compiler in a Linux environment (refer to Makefile).
3. Ensure MZ_APO board is connected and functional, updating the board's IP address in the Makefile.
4. Execute the game by running `make run` in the terminal (within the project folder).
5. Use MZ_APO knobs to control the snake(s) and navigate the menu during gameplay.

## Game Components
1. **Game Field**: Rectangular area (480x320 pixels) displaying the snake and apples.
2. **Snake**: Player-controlled entity that grows longer by consuming apples.
3. **Apples**: Food items randomly appearing for the snake to consume.
4. **Score**: Displayed in the left upper corner, representing the player's current score.
5. **Menu**: Initial screen allowing players to select the number of players and difficulty level.
6. **LCD Display**: Graphical interface showing the game field, snake, apples, and score.
7. **LEDs**: Row of LEDs indicating time remaining before a new apple appears.

## Code Structure
The code is organized into several functions, each handling specific aspects of the game, including menu display, game logic, drawing elements, and player input.

- `draw_home_page`: Displays the menu screen for player and difficulty selection.
- `draw_game_page`: Manages the game field, snake movement, apple spawning, collision detection, and scoring.
- ... (Other functions responsible for drawing, computation, initialization, and game flow. Can be found in the Documentation.docx)

## Game Controls
The game utilizes the MZ_APO board's knobs for player interaction:
- **Knob 2 (Green)**: Controls the snake's movement direction for player 1 and menu navigation.
- **Knob 3 (Blue)**: Controls the snake's movement direction for player 2 (in two-player mode).
- **Knob 1 (Red)**: Ends the game when clicked.

## Gameplay
1. Select the number of players and difficulty level on the home page using the Green knob.
2. Control the snake(s) using the knobs, guiding them to eat apples and increase length and score.
3. Avoid collisions with walls, other snakes, or themselves.
4. The game continues until at least one player collides, displaying a "Game Over" screen.
5. Press any button to return to the menu.

## Scoring
- Snake's length increases and score increments upon consuming apples.

## Additional Features
- **Two-player mode**: Enables simultaneous competition on the same field.
- **Difficulty levels**: Offers varying gameplay challenges affecting snake speed.
- **LED countdown**: Indicates time remaining before a new apple appears.

## Documentation
For more detailed information, refer to the [Documentation.docx](Documentation.docx) file.

## Conclusion
Snake Game offers an entertaining and challenging gaming experience with single or two-player modes, multiple difficulty levels, and user-friendly controls using the MZ_APO board. Enjoy the classic Snake Game and aim for the highest scores!
