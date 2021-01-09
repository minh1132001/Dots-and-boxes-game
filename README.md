# Dots-and-boxes-game
1. Project description:
 * The game starts with an empty grid of 4x4 dots.
 * Two players take turns adding a single horizontal or vertical line
between two unjoined adjacent dots.
 * A player who completes the fourth side of a 1×1 box earns the
point that is equal to the number of the lines that player drawn out
of 4 line of that box.
 * The game ends when no more lines can be placed.
 * The winner is the player with the most points.
2. Problem description:\
 **Input**:\ 
 a 4x3 zeros matrix A, a 3x4 zeros matrix B, a 3x3 matrix S\
**Where:** 
- Matrix A show the state of horizontal edges
- Matrix B show the state of vertical edges
- Matrix S show the state of 1x1 squares\
 **Algorithm:**
- The main algorithm is minimax and alpha-beta pruning
algorithm
- When each player choose a edge to draw, the value of the
position in matrix A(if that edge is a horizontal edges) or
B((if that edge is a vertical edges) that correspond to the
edge of table will be change:\
  --1 if it is turn of player 1\
  2 if it is turn of player 2
- If there is a 1x1 square formed the value of the position in
matrix S that correspond to the edge of table will be change:\
  --1 if it is turn of player 1\
  --2 if it is turn of player 2
