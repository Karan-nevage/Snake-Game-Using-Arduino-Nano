# Arduino Snake Game

## Description
This project is a recreation of the classic Snake game using an Arduino Nano and an OLED display. The game is controlled using a joystick. The snake moves in four directions: up, down, left, and right. The objective of the game is to eat the food that appears randomly on the screen. Each time the snake eats the food, it grows longer and the game becomes more challenging.

## Components
- Arduino Nano
- OLED Display (128x64)
- Joystick Module

## Libraries
- Adafruit_GFX
- Adafruit_SSD1306
- Wire

## Setup
1. Connect the OLED display and the joystick module to your Arduino Nano.
2. Install the necessary libraries in your Arduino IDE.
3. Upload the snake game code to your Arduino Nano.

## How to Play
- Use the joystick to control the direction of the snake.
- Try to eat the food that appears on the screen.
- Avoid running into the wall or the snake's own body.

## Code Explanation
The code starts by including the necessary libraries and defining global variables for the game. The joystick's analog values are read in the `keyScan` function, which sets the snake's direction. The `draw_snake` function draws a block of the snake on the OLED display at the given coordinates. The `show_score` function displays the score at the given coordinates on the OLED display. The `screen` function clears the display, draws the game area, displays the level and score, and draws the snake and food on the OLED display. The `draw_food` function generates a new food location if the previous food has been eaten, ensuring that the new food location is not inside the snake's body. The `snake_move` function updates the snake's head position based on its direction, checks if the snake has eaten the food, and updates the snake's body position. It also calls the function to check if the snake has died. The `draw_game_over` function displays the "GAME OVER" message along with the final level and score on the OLED display. The `check_snake_die` function checks if the snake has hit the wall or eaten itself, and sets the `game_over` variable to true if either condition is met. The `setup` function initializes the OLED display and sets the random seed for the food location. Finally, the `loop` function is the main game loop. It calls the key scan, snake move, draw food, and screen functions in each iteration. If the game is over, it calls the draw game over function instead.

## Enjoy the game!
