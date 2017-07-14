Snake *
==========
My simple attempt at creating an AI within a game.

Background
-------------
After lunch right before the long weekend, like most people, I was too lazy to do any real work. I have been interested in understanding gaming AI for quite some time, mainly after feeling the frustration of the Dark Souls AI, so I decided I'd attempt to get my feet wet in the field by attempting to create a simple pathing AI for the classic game Snake.

How it looks
-------------
<img style="float: right;" src="snake.gif" width="458" height="400">

Implementation
-------------
Going back to what I was taught in university, I thought of using Dijkstra's algorithm to find the shortest path from the head of the snake to the item but have read that A* is very similar to Dijkstra's algorithm but includes a heuristic for better estimating. 
> __Solution: Using A* algorithm__

While this did provide me with a snake that did get to the item (apple) the fastest, it would also make a lot of errors such as not working at all if the snake's body was long enough to prevent the head from reaching the item. 
> __Soltuion: Move to a direction furthest from the item to attempt to 'stall' it__

This would move the snake's body enough such that there would be a path from head to item although this lead to another difficulty as the snake's head would sometimes move in a direction that would tunnel it to immediate death. 
> __Solution: *Take into factor the number of available spaces within my calculation of determining the next node and choose one that would net the snake the most amount of available movements for stalling__

While the AI at this point does work moderately well, it still with make errors such as going for items that will instantly cause it to die or when performing 'stalling', not use all available spaces.

Remarks
-------------
While I did think this would be an easy experiment that could be completed within a time frame of roughly 4 hours, something even as simple as creating an AI in snake can be challenging as there are multiple measures to account for. I may spend time when there isn't much work to strengthen the AI but for now, it was a fun little experiment to get a grasp at AI implementation.
