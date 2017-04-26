# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: We use naked twins strategy to eliminate possibilities rather than allocating value directly. After finding naked 
twins we know that possible values will be in either of the box so we can safely discard those possible values for their 
peers which might allocate a value to peer which will help us decide which values goes where in the pair. However, 
if no value is allocated to any peer and just reduces number of possibilities which is also useful as it reduces our 
search space and further application of elimination and only choice strategy might give us a solution.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Diagonal sudoku is same as normal sudoku except that is has the numbers 1 to 9 should all appear exactly once 
along the two main diagonals. Now, to solve diagonal sudoku we add a constraint to our previous solution to check the number 
occurs exactly one along the two diagonals and apply elimination, only choice, naked twins and search with this additional constraint.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.