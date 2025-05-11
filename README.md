# MiddleEdgeFinder

# Description
MiddleEdgeFinder is a Python script that computes the alignment score and the middle edge of the alignment graph between two sequences using dynamic programming. This is useful in memory-efficient implementations of sequence alignment algorithms like Hirschberg's Algorithm, which splits the problem around the middle column of the dynamic programming matrix.


# Functionality
find_middle_edge(match_reward, mismatch_penalty, indel_penalty, v, w)
Purpose:
Finds the alignment score and the middle edge (a path across the matrix center) in the global alignment graph between two sequences.

# Approach:

* Builds a scoring matrix using dynamic programming.
* Tracks directions with a pointer matrix (diagonal, up, left).
* Traces the optimal path backward to identify the middle edge.
* Returns the total alignment score and the coordinates of the middle edge.

# Parameters
* match_reward (int): Score for a character match (e.g., +1).
* mismatch_penalty (int): Penalty for a mismatch (e.g., -1).
* indel_penalty (int): Penalty for insertion/deletion (gap) (e.g., -2).
* v (str): First sequence (e.g., "GAGA").
* w (str): Second sequence (e.g., "GAT").

# Returns

* tuple: A tuple containing:

* int: The final alignment score.

* list of tuple: A list of coordinate pairs representing the middle edge of the optimal alignment path.

#  Example Usage

```

  score, middle_edge = find_middle_edge(1, -1, 2, "GAGA", "GAT")
print("Score:", score)
print("Middle edge path:", middle_edge)
```

# Output Example

(1, [(0, 0), (1, 1), (2, 2), (3, 3)])

# Applications

* This function is relevant in several bioinformatics and computational biology tasks:
* Hirschberg’s Algorithm: Identifying the middle edge to optimize space in pairwise alignment.
* Global Alignment: In memory-limited scenarios where only part of the matrix is computed.
* Dynamic Programming Education: Demonstrates step-by-step scoring and traceback logic.

# Requirements
* Python 3.x
* No external libraries required.

# License
This project is licensed under the MIT License – see the LICENSE file for more details.








