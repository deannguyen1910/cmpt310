# Search Heuristic function
## Greedy Search
* Strategy: expand a node that you think is closest to a goal state.
    * Heuristic: estimate of distance to nearest goal for each state.
* A common case:
    * Best-first takes you straight to the (wrong) goal
* Worst-case: like a badly-guided DFS

# A* Search (A-star)
* Uniform-cost orders by path cost, or backward cost g(n)
* Greedy orders by goal proximity, or forward cost h(n)
    * f(n) = g(n) + h(n)

# Admissible Heuristics
* A heuristic h is admissible (optimistic) if:
 ```$
    0 <= h(n) <= h*(n)
 ```       


