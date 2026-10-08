# Simon Game

A browser version of the classic **Simon Says** memory game. Watch the color sequence, then repeat it. Every level adds one more step.

## Features

- Press any key to start
- Four colored buttons, each with its own sound
- The sequence grows by one color each level
- The current level is shown at the top
- A wrong click plays an error sound, flashes the screen and resets the game

## Tech Stack

- HTML5
- CSS3
- JavaScript + jQuery

## How to Run

```bash
git clone https://github.com/PRiNCeKUsHW/Simon-game.git
cd Simon-game
```

Open `index.html` in a browser and press any key to begin.

## Project Structure

```
Simon-game/
├── index.html     # Layout with the four color buttons
├── styles.css     # Button colors, press and game-over animations
├── game.js        # Game logic: sequence, input checking, levels
└── sounds/        # red, blue, green, yellow and wrong .mp3 files
```

## How It Works

1. `nextSequence()` picks a random color, adds it to `gamePattern` and flashes it.
2. Each click is pushed to `userClickedPattern`.
3. `checkAnswer()` compares the two step by step.
4. If the full sequence matches, the next level starts. If not, `startOver()` resets the game.
