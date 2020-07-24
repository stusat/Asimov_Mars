# Asimov_MarsRover
The project with all the files, that we as a team have developed for the Engage2020 mentorship program as a part of the Microsoft Codess India initiative.
--------
## Introduction
The aim of this project is to provide a path-finding library to approximate the shortest path in real-life situations, like- in maps, games where there can be many hindrances.
We considered a 2D Grid having several obstacles genearted randomly and we start from a source cell (top left corner of the grid) to reach towards a goal cell (bottom right corner). This project is made using the _p5.js library._
## Why A* algorithm? An explanation
A* Search algorithm is indeed a well known technique used in path-finding and graph traversals. Consider a square network/grid that has obstacles and we are given a start cell and a target cell. Our job is to reach the target cell (if possible) from the start cell as efficiently possible in the shortest path. 

What the A* Search Algorithm does is that at each succession it picks up the node based on a value-‘f’ which is a parameter equal to the sum of two other parameters – ‘g’ and ‘h’. At each succession, node/cell having the lowest ‘f’ value is selected, and processed.

We define ‘g’ and ‘h’ as follows:

g = the movement cost to move from the start cell to a given square on the network, following the path generated to get there.

h = the estimated movement cost to move from that given square on the grid to the final target. This is known as the heuristic: a kind of smart guess. The actual distance isn't known until we path is found. There are several ways to calculate this ‘h’.
## Heuristics
h can be calculated in 2 methods:
* `Calculate the exact h value (very time consuming).` 

                            (or)
                            
* `Approximate the value of h using some heuristics (less time consuming).`

**1) Exact Heuristics –**

A few methods to calculate the exact value of h are as follows:

(i) Pre-compute the distance between each pair of cells prior to the running of the A* Search Algorithm.

(ii) If there are no obstacles then the exact value of h can be found without any pre-computation using the distance formula/Euclidean Distance

**2) Approximation Heuristics –**

There are generally three approximation heuristics to calculate h, namely, _Manhattan Distance, Diagonal Distance_ and thirdly _Euclidean distance._ We've implemented the heuristics using the **Euclidean Distance** method and the same is explained below.

• As it is clear from its name, it is nothing but the distance between the current cell and the goal cell using the distance formula:
   
   `h = sqrt ( (current_cell.x – goal.x)2 + 
            (current_cell.y – goal.y)2 )` 
            
• This heuristic is used when we are allowed to move in any direction, inclusive of diagonal movement.
## Time Complexity
Considering a graph, it may take us to travel all the edge to reach the destination cell from the source cell. For example, consider a graph where source and destination nodes are connected by a series of edges, like – 0(source) –>1 –> 2 –> 3 (target).
So the worse case time complexity is O(E), where E is the number of edges in the graph
## Limitations
Although being the best pathfinding algorithm around, A* Search Algorithm doesn’t produce the shortest path _always_, as it relies heavily on heuristics / approximations to calculate h.




