# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

### Overview
In this project, we will be writing code to implement an AI Sudoku solver.

Our strategy will consist of:
1. Elimination
2. Only Choice
3. Naked Twins
4. Search

Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint Propagation is all about using local constraints in a space (in the case of Sudoku, the constraints of each square) to dramatically reduce the search space. As we enforce each constraint, we see how it introduces new constraints for other parts of the board that can help us further reduce the number of possibilities. In other words, we apply the same constraint as many times as we can until a solution is obtained, or the constraint can no longer be applied.

The naked twins strategy is one such constraint in Sudoku. If we identify a pair of boxes belonging to the same set of peers that have the same 2 numbers as possibilities, we can eliminate those two numbers from all the boxes that have these two boxes as peers because:
* No other digit can appear in those 2 boxes.
* The 2 digits cannot appear in the other boxes of the unit.

Q: How do we use constraint propagation to solve the diagonal Sudoku problem?  
A: Diagonal sudoku has the extra constraint that among the two main diagonals, the numbers 1 to 9 should all appear exactly once. For diagonal Sudoku, we can use the same constraint propagation we used for regular Sudoku, but we need to apply them to the 2 extra units (the two diagonals). This can be accomplished easily by adding the 2 diagonal units to the unitlist.

### Install

This project requires **Python 3**.
Dependencies found in `requirements.txt`.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `AI_Sudoku.ipynb` - A walkthrough of the problem and solution.
* `solution.py` - The solution to the problem.
* `solution_test.py` - You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - This is code for visualizing the solution.
* `visualize.py` - This is code for visualizing ther solution.

### Visualizing

To visualize the solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py
