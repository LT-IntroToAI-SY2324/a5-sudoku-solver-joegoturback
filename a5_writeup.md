# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

BFS and DFS may be more preferable over one another depending on how the things being searched across the grid are distributed. For example in Sudoku, DFS would be preferable if the numbers tend to be packed closer to the top of the puzzle (it would be required if one of the ranks of the grid were completely empty), and breadth first search would be more preferable if the numbers were packed closer to the side. (would be required if one of the files were completely empty)


2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

BFS algorithms search things sideways on a grid, while DFS searches everything vertically and throroughly. 


3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?
The Sudoku solver could be a step towards making a CPU play a game of chess against a player. Depth first search could be effective in each rank of the board (1-8) while breadth search would be good for files (a-h). The computer would be able to see each piece being threatened on the board depending on how the pieces move. Lots of additional code would be needed for the computer to decide whether to take the piece or move their own piece away from a threatening piece, or detect checks of their king, but seeing all the basic possible moves on the board can be taken directly from the sudoku solver. For example, a rook that can only move vertically on the board (because it is restricted by its own pieces on both sides) can utilize depth-first search most efficiently to check the possible captures and dangeorus squares in front of it. 

