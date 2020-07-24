# Asimov_MarsRover
The project with all the files, that we as a team have developed for the Engage2020 mentorship program as a part of the Microsoft Codess India initiative.
--------
# Introduction
The aim of this project is to provide a path-finding library to approximate the shortest path in real-life situations, like- in maps, games where there can be many hindrances.
We consider a 2D Grid having several obstacles genearted randomly and we start from a source cell (top left corner of the grid) to reach towards a goal cell (bottom right corner)
----------
# Why A* algorithm? An explanation
A* Search algorithm is one of the best and popular technique used in path-finding and graph traversals. Consider a square grid having many obstacles and we are given a starting cell and a target cell. We want to reach the target cell (if possible) from the starting cell as quickly as possible. 

What A* Search Algorithm does is that at each step it picks the node according to a value-‘f’ which is a parameter equal to the sum of two other parameters – ‘g’ and ‘h’. At each step it picks the node/cell having the lowest ‘f’, and process that node/cell.

We define ‘g’ and ‘h’ as follows:

g = the movement cost to move from the starting point to a given square on the grid, following the path generated to get there.
h = the estimated movement cost to move from that given square on the grid to the final destination. This is often referred to as the heuristic, which is nothing but a kind of smart guess. We really don’t know the actual distance until we find the path. There can be many ways to calculate this ‘h’ which are discussed in the later sections.


