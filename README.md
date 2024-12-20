# Sudoku Game GUI Documentation

## Overview
This project implements a **Sudoku game GUI** using Python's `tkinter` library. The application provides a playable Sudoku board with interactive features such as number dragging, AI moves, puzzle solving, and victory detection. Players can solve the provided Sudoku puzzle or interact with the grid by filling cells manually or using automated tools.

---

## Features
1. **Sudoku Grid**: A 9x9 Sudoku grid with highlighted subgrids for visual clarity.
2. **Number Dragging**: Drag numbers from the number pad to cells in the grid.
3. **Keyboard and Mouse Controls**:
   - Select cells using the mouse.
   - Press `Space` to start a new game.
4. **Control Buttons**:
   - Solve: Automatically solve the puzzle.
   - AI Move: Let the program make a smart move.
   - Clear: Clear non-initial cells.
   - Reset: Undo the last entered value.
5. **Victory Detection**: Display a congratulatory message upon completing the puzzle.

---

## File Structure
The code is contained in a single Python file. It uses the `tkinter` library for GUI functionality and basic Python data structures to handle the board logic.

---

## Components

### Classes and Methods
#### `SudokuGUI`
The main class that initializes and manages the GUI and game logic.

##### Constructor (`__init__`)
- **Arguments**: `root` (the `tk.Tk()` instance).
- **Responsibilities**:
  - Initialize the game window.
  - Create the Sudoku grid, number pad, and control buttons.
  - Bind events for interaction.

##### Methods
- **`create_grid`**: Constructs the 9x9 Sudoku grid and initializes cell styles.
- **`create_cell_frame`**: Creates a frame for each grid cell.
- **`create_cell_label`**: Creates a label for a cell to display numbers.
- **`create_control_buttons`**: Adds control buttons (Solve, AI Move, Clear, Reset).
- **`create_button`**: Helper method to simplify button creation.
- **`create_numpad`**: Creates the number pad for selecting and dragging numbers.
- **`reset_game`**: Resets the grid to the initial state.
- **`clear_victory_message`**: Removes any victory message displayed.
- **`solve_puzzle`**: Solves the Sudoku puzzle using a backtracking algorithm.
- **`solve_sudoku`**: Recursive function for solving the puzzle.
- **`make_ai_move`**: Allows the AI to make a single smart move.
- **`clear_board`**: Clears all non-initial cells.
- **`start_drag`**: Starts dragging a number from the number pad.
- **`drag`**: Updates the position of the dragged number.
- **`handle_drop`**: Places a number in a selected cell if valid.
- **`cell_clicked`**: Handles cell selection.
- **`is_valid_move`**: Checks if a number placement is valid.
- **`update_display`**: Updates the grid display based on the current board state.
- **`check_victory`**: Checks if the board is completely and correctly filled.
- **`show_victory`**: Displays a victory message.
- **`new_game`**: Starts a new game.

---

## Sudoku Logic
The Sudoku board is represented as a 2D list (`self.board`) with:
- `0` indicating empty cells.
- Predefined numbers as the initial board.

The following logic is implemented:
1. **Validation**: Ensures that a number placement satisfies Sudoku rules.
2. **Backtracking Solver**: Recursively solves the Sudoku using trial and error.
3. **Victory Detection**: Checks if all cells are filled correctly.

---

## Controls
- **Mouse**:
  - Click on a cell to select it.
  - Drag numbers from the number pad to the grid.
- **Keyboard**:
  - Press `Space` to reset the game.

---

## Dependencies
- Python 3.x
- `tkinter` library (included in standard Python distributions).

---

## How to Run
1. Ensure Python 3 is installed.
2. Save the code to a file, e.g., `sudoku_gui.py`.
3. Run the file using the command:
   ```bash
   python sudoku_gui.py
   ```
4. Interact with the GUI to play the game.

---

## Future Improvements
- Add difficulty levels with varying board setups.
- Implement timer and scoring system.
- Allow saving and loading puzzles.
- Enhance AI for multiple moves.

---

## License
This project is open-source and available for personal or educational use. Contributions are welcome!

