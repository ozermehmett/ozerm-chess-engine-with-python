# Chess Engine

This is a simple chess engine implemented in Python. It provides basic functionalities for playing chess, including move generation, check detection, and castling.

## Functions

### `square_under_attack(row, col)`

Determines if an enemy can attack the square at the given row and column.

**Parameters:**
- `row` (int): The row index of the square.
- `col` (int): The column index of the square.

**Returns:**
- `True` if the square is under attack, `False` otherwise.

### `get_all_possible_moves()`

Generates all possible moves for the current position without considering checks.

**Returns:**
- A list of all possible moves.

### `check_for_pins_and_checks()`

Checks for pins and checks on the board.

**Returns:**
- A tuple `(in_check, pins, checks)` where
  - `in_check` (bool): Indicates if the current side is in check.
  - `pins` (list): List of pinned squares and their pinning direction.
  - `checks` (list): List of squares where the enemy is applying a check.

### `get_pawn_moves(row, col, moves)`

Generates all possible moves for a pawn located at the given row and column.

**Parameters:**
- `row` (int): The row index of the pawn.
- `col` (int): The column index of the pawn.
- `moves` (list): List to store the generated moves.

### `get_rook_moves(row, col, moves)`

Generates all possible moves for a rook located at the given row and column.

**Parameters:**
- `row` (int): The row index of the rook.
- `col` (int): The column index of the rook.
- `moves` (list): List to store the generated moves.

### `get_knight_moves(row, col, moves)`

Generates all possible moves for a knight located at the given row and column.

**Parameters:**
- `row` (int): The row index of the knight.
- `col` (int): The column index of the knight.
- `moves` (list): List to store the generated moves.

### `get_bishop_moves(row, col, moves)`

Generates all possible moves for a bishop located at the given row and column.

**Parameters:**
- `row` (int): The row index of the bishop.
- `col` (int): The column index of the bishop.
- `moves` (list): List to store the generated moves.

### `get_queen_moves(row, col, moves)`

Generates all possible moves for a queen located at the given row and column.

**Parameters:**
- `row` (int): The row index of the queen.
- `col` (int): The column index of the queen.
- `moves` (list): List to store the generated moves.

### `get_king_moves(row, col, moves)`

Generates all possible moves for a king located at the given row and column.

**Parameters:**
- `row` (int): The row index of the king.
- `col` (int): The column index of the king.
- `moves` (list): List to store the generated moves.

### `get_castle_moves(row, col, moves)`

Generates all valid castle moves for the king located at the given row and column.

**Parameters:**
- `row` (int): The row index of the king.
- `col` (int): The column index of the king.
- `moves` (list): List to store the generated moves.

### `get_king_side_castle_moves(row, col, moves)`

Generates valid king-side castle moves for the king located at the given row and column.

**Parameters:**
- `row` (int): The row index of the king.
- `col` (int): The column index of the king.
- `moves` (list): List to store the generated moves.

### `get_queen_side_castle_moves(row, col, moves)`

Generates valid queen-side castle moves for the king located at the given row and column.

**Parameters:**
- `row` (int): The row index of the king.
- `col` (int): The column index of the king.
- `moves` (list): List to store the generated moves.

### `CastleRights`

A class representing castling rights for both players.

**Attributes:**
- `wks` (bool): White king-side castling rights.
- `bks` (bool): Black king-side castling rights.
- `wqs` (bool): White queen-side castling rights.
- `bqs` (bool): Black queen-side castling rights.

### `Move`

A class representing a chess move, including methods for obtaining chess notation.

**Attributes:**
- `start_row` (int): The row index of the starting square.
- `start_col` (int): The column index of the starting square.
- `end_row` (int): The row index of the ending square.
- `end_col` (int): The column index of the ending square.
- `piece_moved` (str): The piece moved.
- `piece_captured` (str): The piece captured.
- `is_pawn_promotion` (bool): Indicates if the move is a pawn promotion.
- `is_enpassant_move` (bool): Indicates if the move is an en passant capture.
- `is_castle_move` (bool): Indicates if the move is a castling move.

**Methods:**
- `get_chess_notation()`: Returns the real chess notation for the move.
- `__str__()`: Returns a string representation of the move.

## Example Usage

```python
# Example Usage of the Chess Engine

# Initialize the chess engine
chess_engine = ChessEngine()

# Get all possible moves for the current position
all_moves = chess_engine.get_all_possible_moves()

# Print the moves
for move in all_moves:
    print(move.get_chess_notation())
