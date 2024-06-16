## Minesweeper Game Overview

### Game Description:
Minesweeper is a puzzle video game in which mines (resembling naval mines in the classic theme) are scattered throughout a board that is divided into cells. The objective is to clear the board without detonating any mines.

### Game Rules:
1. **Board and Cells**:
    - The game board is a grid of cells, each of which can be in one of three states: unopened, opened, or flagged.
    - An unopened cell is blank and clickable.
    - An opened cell is exposed and shows either a number (indicating the number of mines adjacent to it) or a blank tile (or "0").
    - A flagged cell is marked by the player to indicate a potential mine location.

2. **Gameplay**:
    - A player selects a cell to open it. If an opened cell contains a mine, the game ends.
    - If the cell does not contain a mine, it will display a number indicating the number of mines in the surrounding cells (diagonally and adjacent).
    - If an opened cell shows "0", all adjacent non-mined cells are automatically opened.
    - Players can also flag cells to mark potential mine locations. Flagged cells are still considered unopened and can be unflagged or opened later.
    - In some versions, when the number of adjacent mines equals the number of flagged cells, all adjacent non-flagged unopened cells are automatically opened. This is known as "chording".

3. **Winning and Losing**:
    - The game is won when all non-mined cells are opened.
    - The game is lost if a mined cell is opened.

### Game Controls:
1. **Left Click**:
    - Left-click on a cell to open it. If the cell is a mine, the game ends.
    - If the cell shows a number and the number of adjacent mines equals the number of flagged cells, left-clicking on it will open all adjacent non-flagged cells (chording).

2. **Right Click**:
    - Right-click on a cell to flag or unflag it. A flagged cell is marked with an "F" to denote a potential mine location.

### Game Implementation Details:
1. **Classes**:
    - **Minesweeper**: Handles the game logic, including board initialization, mine placement, number calculation, cell revealing, flagging, and chording.
    - **MinesweeperGUI**: Manages the graphical user interface using `tkinter`, including creating the game board, handling user input, updating the display, and managing game state.

2. **Functions and Methods**:
    - **initialize_board**: Sets up the board by placing mines and calculating numbers.
    - **place_mines**: Randomly places the specified number of mines on the board.
    - **calculate_numbers**: Calculates and assigns the number of adjacent mines for each cell.
    - **reveal**: Opens a cell and triggers recursive opening for blank cells.
    - **flag**: Flags or unflags a cell.
    - **chord**: Opens all adjacent non-flagged cells if the number of flagged cells equals the number of adjacent mines.
    - **create_menu**: Sets up the menu with options to restart the game and change settings.
    - **create_widgets**: Creates the grid of buttons representing the game board.
    - **on_button_click**: Handles left-click events on cells.
    - **on_right_click**: Handles right-click events to flag or unflag cells.
    - **update_buttons**: Updates the button states based on the game state.
    - **reveal_all**: Reveals all cells when the game is over.
    - **restart**: Restarts the game with the current settings.
    - **change_size**: Prompts the user to change the board size and restarts the game.
    - **change_mines**: Prompts the user to change the number of mines and restarts the game.
    - **update_widgets**: Redraws the game board when settings change.

### How to Play:
1. **Start the Game**: Run the script to open the Minesweeper game window.
2. **Open Cells**: Left-click on cells to open them.
3. **Flag Mines**: Right-click on cells to flag or unflag potential mine locations.
4. **Win the Game**: Successfully open all non-mined cells to win.
5. **Lose the Game**: Open a cell with a mine to lose the game.
6. **Restart or Change Settings**: Use the menu to restart the game or change the board size and number of mines.
