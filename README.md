# Reinforcement Q-Learning Alg Maze Solving

**Objective** : You’re going to implement an agent that can solve a given maze. Maze information is stored
in a dictionary structure. Maze consists of cells and cells will be stored as tuples.

**Question:** In this homework, you’re going to implement a scenario where an agent searches for the exit
in a given maze. Maze consists of cells and cells can have 4 states: empty, wall, start and end.

Empty Cell: Empty cell means the agent can move freely across those cells. Agent can move in 4
directions: west, east, south and north.

Cells with walls: These are the cells that contain walls and the agent can’t move to those cells. Please
examine the given figure below.

Start Cell: The agent will start from this cell and search for the exit cell.

End Cell: The agent will search for this cell and when it finds the exit cell it’ll output the path that leads
to that cell (starting from the start cell).

The information regarding the maze will be provided in a dictionary structure. You’ll utilize this
dictionary to get the information about cell states and the maze length. Dictionary will have the following
structure:

{ cell_tuple: “Wall”, cell_tuple:”Wall”, .. “information”: {“rows”:x, “columns”: y, “start”:cell_tuple,
“end”: cell_tuple} }

As you can see the dictionary has an internal dictionary that contains the additional information about the
maze. Internal dictionary holds the maze length, width and also agent’s start location and maze’s finish
location. Locations are held in cell_tuple structure which are simple tuple structures that show the
coordinates of a cell.

Cell_tuple = (x_coordinate, y_coordinate)


Two examples of the mentioned dictionary are given below in order to create a more solid understanding
of the desired structure. Be careful that the cell coordinates are starting from the 0 just like array indices.

Maze 1:

map_information =

```
{
```
```
(0,1) : "W", (3,1) : "W", (3,3) : "W", (3,4) : "W",
```
```
"information" : {"rows":5,"columns":5, "start":(0,4), "end":(4,2)}
```
}

Maze 2:

map_information =

```
{
```
```
(1,1) : "W", (2,3) : "W", (0,5) : "W", (4,3) : "W",(2,7) : "W", (5,7) : "W", (5,6) : "W",
```
"information" : {"rows":6,"columns":8, "start":(2,1), "end":(0,7) }

}

As you can see from the dictionaries, only cells with walls are provided. All other cells are free cells. Be
careful about the indentations, additional spaces are applied in order to make it more visually appealing,
delete these spaces before you paste it into your code. The nested dictionary (The internal one with the
“information” tag) stores additional information about maze’s length and width. Also, it holds the
agent’s start location and maze’s end location. Maze 2 example is visualized below, where W means
walls, S means start location, E means end location.


Start with the provided maze examples and try to create a searching algorithm that takes the agent from S
to E. There are literally hundreds of search algorithms you can find online that can work in this
homework. Choose one and implement it as your searching algorithm. You’ll choose your own algorithm
so I expect to see different search algorithms in different homeworks. If everyone implements the same
algorithm that means something inappropriate is going on. You can implement the breadth first search
[1], Q learning [2], A* algorithm [3], Dijsktra’s algorithm [4] or you can use a simple brute force
algorithm. Searching algorithm choice is up to you, just don’t use a 3rd party library. After searching, your
algorithm should output the path it found (It doesn’t need to find the shortest path). For the second maze
example, your output should look like this:


That path can be visualized as below:

**References:**

[1]: https://www.geeksforgeeks.org/shortest-distance-two-cells-matrix-grid/

[2]: [http://mnemstudio.org/path-finding-q-learning-tutorial.htm](http://mnemstudio.org/path-finding-q-learning-tutorial.htm)

[3]: https://www.geeksforgeeks.org/a-search-algorithm/

[4]: https://www.geeksforgeeks.org/dijkstras-shortest-path-algorithm-greedy-algo-7/





