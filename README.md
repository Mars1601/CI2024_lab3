# LAB03 COMPUTATIONAL INTELLIGENCE: PUZZLE

The code solves the sliding puzzle problem (e.g. puzzle 8 or 15) using the A* algorithm. Here's how it works:

### 1. Initial state generation: 
A randomized puzzle is created, but only if it is solvable (i.e. if the number of reversals in the puzzle is even).

### 2. Finding available actions: 
The available_actions() function finds possible moves (up, down, left, right) from the position of the empty element (denoted by 0).

### 3. Execution of actions: 
The do_action() function executes a move (exchanges two positions in the puzzle) generating a new state.

### 4. Manhattan Distance Calculation: 
The manhattan_distance() function calculates the heuristic, which measures the total distance between the current positions of the numbers and their target positions in the puzzle. Heuristics are used to estimate the "residual cost" of reaching the solution.

### 5. Algorithm A*: 
The a_star_search() function explores the states of the puzzle starting from the initial state and using a priority queue (PriorityQueue) to expand the states with the lowest total cost (sum of the current distance and the heuristic). If the final state (solution) is found, it returns the sequence of moves to get there.

### 6. Solvability check: 
The is_solvable() function checks whether the puzzle is solvable by calculating the number of reversals.

### 7. Solution: 
Finally, the program prints the sequence of moves to solve the puzzle and its final state.

##
In summary, the code uses A* with Manhattan distance as a heuristic to find the optimal sequence of moves from a random initial state to a solution.

