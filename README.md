# Reinforcement Q-Learning Alg Maze Solving
#(Project requires update. Take a look and help me to improve the algorithm :) )

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
![p1](https://user-images.githubusercontent.com/32989239/74086005-ec180f80-4a8f-11ea-808a-7604d3ff86a4.png)

![p2](https://user-images.githubusercontent.com/32989239/74086024-0ce06500-4a90-11ea-94a4-129d8ebe02cf.png)



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

![p3](https://user-images.githubusercontent.com/32989239/74086027-1669cd00-4a90-11ea-88bf-aef4e38666c5.png)







