# Conway's Game of Life — Visualizer

A small, interactive visualizer and simulator for Conway's Game of Life implemented in Python with Pygame. Click to toggle cells, then use the on-screen controls to start, stop, clear, or reset the simulation.



**Features**
- Interactive grid: click cells to toggle alive/dead.
- On-screen controls: `Start`, `Stop`, `Clear`, `Reset`.
- Generation counter displayed in the window.
- Simple, easy-to-read implementation intended for learning and experimentation.

**Prerequisites**
- Python 3.8+ (tested on Windows)
- `pygame` library

If you don't already have `pygame`, install it with pip:

```powershell
python -m pip install pygame
```

**Run the visualizer**
1. Open a PowerShell terminal in the project root (where `main.py` is located).
2. Start the program:

```powershell
python main.py
```

Controls and interactions
- Click anywhere on the grid while the simulation is stopped to toggle a cell alive/dead.
- `Start`: Begins the simulation from the current board state.
- `Stop`: Pauses the running simulation.
- `Clear`: Clears the board to an all-dead state.
- `Reset`: Restores the board to the state it had when the current run was started.
- The generation counter is shown at the bottom-right of the window.

How the simulation behaves
- Each generation update applies Conway's rules: a cell becomes alive if it has exactly 3 neighbors; a living cell dies if it has fewer than 2 or more than 3 neighbors; otherwise it remains in its state.
- The simulation advances in timed steps while `Start` is active.

Project layout
- `main.py` — application entry point and main loop.
- `board.py` — grid creation, drawing logic, and button instances.
- `game.py` — game logic for computing the next generation (`updateTiles`).
- `button.py` — small helper class for on-screen buttons.
- `assets.py` — visual constants (colors, sizes, screen dimensions).

Customization
- Modify visual constants in `assets.py`:
	- `SCREENWIDTH`, `SCREENHEIGHT` — window size
	- `BLOCKSIZE` — size of each cell
	- `FILLCOLOR`, `BGCOLOR`, `WALLCOLOR` — colors used by the UI