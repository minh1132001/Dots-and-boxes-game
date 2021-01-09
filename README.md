# Dots-and-boxes-game
## 1.Project description:
 * The game starts with an empty grid of 4x4 dots.
 * Two players take turns adding a single horizontal or vertical line
between two unjoined adjacent dots.
 * A player who completes the fourth side of a 1×1 box earns the
point that is equal to the number of the lines that player drawn out
of 4 line of that box.
 * The game ends when no more lines can be placed.
 * The winner is the player with the most points.
## 2.Problem description:
**Input**: 
 a 4x3 zeros matrix A, a 3x4 zeros matrix B, a 3x3 matrix S\
**Where:** 
- Matrix A show the state of horizontal edges
- Matrix B show the state of vertical edges
- Matrix S show the state of 1x1 squares\
**Algorithm:**
- The main algorithm is minimax and alpha-beta pruning
algorithm
- When each player choose a edge to draw, the value of the
position in matrix A (if that edge is a horizontal edges) or
B (if that edge is a vertical edges) that correspond to the
edge of table will be change:
  > 1 if it is turn of player 1\
  > 2 if it is turn of player 2
- If there is a 1x1 square formed the value of the position in
matrix S that correspond to the edge of table will be change:\
  > 1 if it is turn of player 1\
  > 2 if it is turn of player 2
 - This process will be continuous until all element in the
matrix S are different 0.
- After all the score of player1 and player 2 will be calculate
base on the matrix A, B and S.
- We will use the minimax algorithm to find the best way that
each player can choose and perform it.
## 3. Algorithm for the problem:
### Minimax stragety:
This algorithm assigns a good score to a move that will give points to the
player. On the otherhand, it will give a bad score to a move which allows the
opponent to finish the square in the future:
- We assume that our AI is the maximizing and the opponent is the
minimizing.
- The algorithm takes as input the state of the game, the current
depth of investigation of the tree and whether the move has to be
played by the maximizing or minimizing player.
- It is going to calculate the evaluation function at each level and
thus determine if the move leading to the given state is a good
move.
- Whenever the AI moves, it will consider all possible cases and
calculate the its point and opponient’s point then select the case
with maximum point between it and player.
- Use the following scoring function to evaluate the leaves of the
tree: score = score(AI) – score(Player)
```
If we only use minimax algorithm for the game, the AI has to try many
positions. For example, a 3x3 board already has 18! (6.4e15) states to
investigate. Consequently, it is not feasible to traverse the entire tree, which is
why we have to set a time limit for each move. Accordingly, this means that
weare not traversing the entire tree; this algorithm might fail to find the best
move. To solve this problem, we have to use alpha-beta pruning to optimize it.
```
