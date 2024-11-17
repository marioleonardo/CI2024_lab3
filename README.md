n²-1 Puzzle Solver
This project implements an A* search algorithm to solve the n²-1 puzzle (also known as the sliding puzzle). The puzzle is represented as a 2D numpy array, and the algorithm uses either the Hamming distance or Manhattan distance as the heuristic function.

Requirements
Python 3.x
numpy
tqdm

Installation
To install the required packages, run:

Usage
The main script randomizes the initial state of the puzzle and then attempts to solve it using the A* search algorithm with the Manhattan distance heuristic.

Code Overview
Constants
PUZZLE_DIM: The dimension of the puzzle (e.g., 4 for a 4x4 puzzle).
Functions
available_actions(state: np.ndarray) -> list: Returns a list of possible actions (moves) from the current state.
do_action(state: np.ndarray, action: 'Action') -> np.ndarray: Applies an action to the current state and returns the new state.
hamming_distance(state: np.ndarray, goal_state: np.ndarray) -> int: Calculates the number of misplaced tiles, excluding the empty tile.
manhattan_distance(state: np.ndarray, goal_state: np.ndarray) -> int: Calculates the sum of Manhattan distances of tiles from their goal positions.
solve_n2_1_puzzle(initial_state: np.ndarray, goal_state: np.ndarray, heuristic_func, length_criteria=0) -> list: Solves the n²-1 puzzle using A* search with the given heuristic function.
Example Usage