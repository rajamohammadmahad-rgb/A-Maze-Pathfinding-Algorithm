# A* Maze Pathfinding Algorithm

This project implements the A* (A-Star) search algorithm in Python to find the shortest available path between a starting position and a goal within a randomly generated maze. Developed as part of an AI internship, the project explores fundamental artificial intelligence concepts, particularly informed search algorithms, heuristic functions and data structures used in pathfinding.

The maze environment is generated and visualised using the `pyamaze` Python library. However, the A* search algorithm itself is implemented separately, allowing the underlying search process and its logic to be explored.

The implementation uses Manhattan distance as its heuristic function to estimate the distance between the current cell and the goal. This is combined with the G-score, representing the actual cost of reaching a cell from the starting position, to calculate the F-score:

**f(n) = g(n) + h(n)**

These evaluation scores allow the algorithm to prioritise promising routes rather than exploring every possible path indiscriminately.

A `PriorityQueue`, imported from Python's built-in `queue` module, is used to organise cells awaiting exploration. Each entry contains the F-score, heuristic score and cell coordinates. The queue prioritises cells with the lowest F-score, helping the algorithm determine which position to explore next.

As the algorithm explores the maze, it updates the path costs and records parent-cell relationships in a dictionary. Once the goal is reached, these relationships are used to reconstruct the resulting path from the starting position to the destination.

### Key Concepts Explored

- A* informed search and pathfinding algorithms.
- Manhattan distance and heuristic estimation.
- Priority queues and element prioritisation.
- G-scores and F-scores for path evaluation.
- Python dictionaries and coordinate-based grid navigation.
- Path reconstruction using parent-node relationships.

### Technologies Used

- Python
- pyamaze
- queue.PriorityQueue

### Future Development

Potential improvements include experimenting with alternative priority queue implementations using `heapq`, comparing A* with Dijkstra's algorithm, and analysing performance across different maze sizes.

This project provided practical experience implementing a foundational AI search algorithm while developing my understanding of the data structures and mathematical concepts behind intelligent pathfinding.

Acknowledgements

Developed as part of an AI internship, following the associated instructional material. The implementation and learning resources will be credited here.
https://youtu.be/W9zSr9jnoqY?si=WVDhp2X25So7mcrR
