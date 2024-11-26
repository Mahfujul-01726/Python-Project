`                                                    `**Tic-Tac-Toe Game Documentation**

**Overview:**

This program implements a console-based Tic-Tac-Toe game in Python. Players can choose to play in single-player mode (against the computer) or multiplayer mode (two players). The computer uses the Minimax algorithm with Alpha-Beta pruning to make optimal decisions.

**Modules and Dependencies**

The program uses the following module:

- random: Used to generate random moves for the computer in "easy" difficulty mode.

**Functions**

1. ConstBoard(board)
   1. **Description**: Draws the current state of the Tic-Tac-Toe board.
   1. **Parameters**:
      1. board (list): A list of size 9 representing the board. Values are:
         1. 0: Empty spot.
         1. 1: O (computer's move).
         1. -1: X (player's move).
   1. **Output**: Prints the current board to the console.
1. UserTurn(board, player)
   1. **Description**: Handles the user's move, validating input and updating the board.
   1. **Parameters**:
      1. board (list): The current board state.
      1. player (int): Player identifier (-1 for X, 1 for O).
   1. **Input**: Prompts the user for a position between 1 and 9.
   1. **Output**: Updates the board with the user's move.

3. analyzeboard(board)
   1. **Description**: Analyzes the board to determine if there is a winner or a draw.
   1. **Parameters**:
      1. board (list): The current board state.
   1. **Returns**:
      1. 1: If O (computer) wins.
      1. -1: If X (user) wins.
      1. 0: If the game is a draw.
      1. None: If the game is ongoing.
3. minimax(board, depth, is\_maximizing, alpha, beta, player)

**Description**: Implements the Minimax algorithm with Alpha-Beta pruning to determine the best move.

**Parameters**:

board (list): The current board state.

depth (int): The current depth of the recursion (used for limiting search depth).

is\_maximizing (bool): True if the current player is maximizing (computer).

alpha (float): The best score for the maximizing player.

beta (float): The best score for the minimizing player.

player (int): 1 for computer (O), -1 for user (X).

**Returns**:

The score of the board state.

3. CompTurn(board, difficulty)
- **Description**: Determines and executes the computer's move based on the selected difficulty level.
- **Parameters**:
  - board (list): The current board state.
  - difficulty (str): Difficulty level ("easy", "medium", "hard").
- **Output**: Updates the board with the computer's move.

6. main()
   1. **Description**: The main function to run the game loop. Handles game initialization, mode selection, and turn-taking.
   1. **Flow**:
      1. Prompts the user to select single-player or multiplayer mode.
      1. Initializes the board as a list of 9 zeros.
      1. For single-player mode:
         1. Allows the user to choose difficulty and who plays first.
         1. Alternates turns between the user and the computer until the game ends.
      1. For multiplayer mode:
         1. Alternates turns between two players until the game ends.
      1. Analyzes the board for a winner or draw after each move.
      1. Displays the final result.
   1. **Output**: Prints the winner or indicates a draw.

**How to Run the Game**

1. Execute the script in a Python environment.
1. Follow the prompts to:
   1. Select game mode (single-player or multiplayer).
   1. If single-player, choose difficulty (easy, medium, or hard).
   1. If single-player, decide who plays first.
1. Input moves as prompted (1-9 positions corresponding to the board).

**Board Representation**

The board is represented as a list of size 9, with positions mapped as follows:

1 | 2 | 3

\---------

4 | 5 | 6

\---------

7 | 8 | 9

Values in the list:

- 0: Empty spot.
- 1: O (computer's move).
- -1: X (player's move).

**Game Modes**

1. **Single-Player**:
   1. Play against the computer.
   1. Choose difficulty:
      1. **Easy**: Random moves by the computer.
      1. **Medium**: Minimax with a depth limit.
      1. **Hard**: Full Minimax with Alpha-Beta pruning.
1. **Multiplayer**:
   1. Two players alternate moves.

**Output Examples**

1. **Board Display**:

Current State of Board:

X | O | -

\---------

\- | X | -

\---------

\- | - | O

1. **Result**:
   1. "Computer (O) wins!"
   1. "You (X) win!"
   1. "It's a draw!"

