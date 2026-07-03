# Maze Solver

A simple Java program that solves a 2D maze grid automatically. You give it the grid dimensions and layout, and it will use a DFS algorithm to find a working path from the start point (`S`) to the exit point (`E`). It then prints the solved path using `*` characters and tells you the total number of steps.

---

## Features

* Takes custom maze dimensions and layouts dynamically from the console.
* Solves the maze automatically without requiring manual user movements.
* Prints the layout twice: first showing the original maze, and then the solved version.
* Counts and displays the exact number of steps taken to reach the exit.

---

## System Rules & Constraints

* Movement is allowed in 4 directions only: Up, Down, Left, and Right. Diagonal movement is blocked.
* The solver cannot walk through walls (`1`) or move out of the grid boundaries.
* Shows an error message if the maze doesn't have exactly one `S` and one `E`.
* Shows an error message if the maze is blocked and there is no possible path to the exit.

---

## File Structure

The project is split into 3 clear files to keep the code organized:
1. `Cell.java`: A small helper class to store the coordinates (row and column) of a position in the grid.
2. `MazeSolver.java`: The main logic class that handles the DFS pathfinding algorithm, grid validations, and text rendering.
3. `Main.java`: The entry point that opens a `Scanner` to read all the rows and layout inputs from the console.

---

## How to Run & Test

Run the `Main.java` file and enter your data just like this example:

```text
Enter number of rows: 5
Enter number of columns: 5
Enter the maze row by row (space-separated values):
S 0 1 0 0
0 0 1 0 1
1 0 0 0 1
1 1 1 0 0
0 0 0 0 E

--- Original Maze ---
S 0 1 0 0 
0 0 1 0 1 
1 0 0 0 1 
1 1 1 0 0 
0 0 0 0 E 

--- Solved Maze ---
S * 1 0 0 
0 * 1 0 1 
1 * * * 1 
1 1 1 * 0 
0 0 0 * E 
Path found in 9 steps
