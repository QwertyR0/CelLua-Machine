# CelLua-Machine
A fanmade version of Sam Hogan's Cell Machine, based heavily off the Mystic Mod, that adds a bunch of new cells.
## Running
1. Download a release, preferably the latest one (should be a .love file)
2. Download and install LOVE at https://love2d.org
3. Double-click the .love file (might not work on all OS, for more info see https://love2d.org/wiki/Getting_Started#Running_Games)
## Sharing Levels
If you use an app or website to share levels that has markdown, like Discord, use some method of supressing it, otherwise it's possible that the code will not be posted properly. The easiest way with Discord is to surround your code in two \` marks.
## Compiling mods
1. Create a zip file of the whole game directory (make sure the zip contains the files and *not* the folder OF the files)
2. Rename the .zip to .love <br>
For more info see https://love2d.org/wiki/Game_Distribution#Create_a_.love-file
## New Cells
Trash Cell - Deletes any cells that get pushed into it. Taken from the Mystic Mod. <br>
![image](https://user-images.githubusercontent.com/71151507/126050831-631a3a5e-856f-418b-a6a5-0d82c4834672.png)

One/Two/Three Directional - Can only be pushed towards the marked directions. <br>
![image](https://user-images.githubusercontent.com/71151507/126050754-adf65e40-b0f1-46d7-838a-be619b70080b.png) ![image](https://user-images.githubusercontent.com/71151507/126050761-58bd68c4-b6e1-45ed-a641-2215cd5e7efc.png) ![image](https://user-images.githubusercontent.com/71151507/126050767-433d2200-dd3a-496a-bf16-98f90d3abcb0.png)

180° Rotator Cell - Rotates cells 180 degrees. <br>
![image](https://user-images.githubusercontent.com/71151507/126050775-03e39b96-f705-44a9-bc3f-14cfa01945c1.png)

Mirror Cell - Swaps the cells that it's arrows point to. <br>
![image](https://user-images.githubusercontent.com/71151507/126050777-9a8072e9-88d6-453c-84f5-43e31b175d9a.png)

Puller Cell - Pulls cells. Does not push cells. <br>
![image](https://user-images.githubusercontent.com/71151507/126050778-88e20293-cea0-4c5c-a925-e1a74ae26202.png)

Diverger Cell - Any forces that come into the sides which the arrows point to get rotated 90° and teleported to the end of the diverger. This is a dangerous cell to play with, as it's very concept provides the possibility of infinite loops; I have done my best to prevent these, but if an infinite loop slips by, it will stop the loop and create a trash cell, for debugging purposes. <br>
![image](https://user-images.githubusercontent.com/71151507/126050780-6e618371-dfce-4482-b580-87d5b6cac04b.png)
![image](https://user-images.githubusercontent.com/71151507/126437594-23d8c6c9-2389-4a0f-b4cb-ffd15b14dc73.png)

Redirector Cell - Sets the rotation of the 4 cells it touches to it's own rotation. Wont affect other redirectors. <br>
![image](https://user-images.githubusercontent.com/71151507/126050783-5fd81eeb-c7f5-433a-b894-36390eb88dfe.png)

Gear Cell - Grabs the 8 cells nearby and rotates them 45 degrees around itself. Cells going from diagonally adjacent to orthogonally adjacent will have their rotation adjusted. <br>
![image](https://user-images.githubusercontent.com/71151507/126050785-8d82bd19-1859-4a33-a3c8-a15a94a1a761.png)
![image](https://user-images.githubusercontent.com/71151507/126050787-560bc47e-8b21-4807-aea1-ecbb3170ace8.png)

Mold Cell - Upon being generated by a generator, the generated cell will disappear (but the forces from being cloned will still apply.) <br>
![image](https://user-images.githubusercontent.com/71151507/126050788-3ec06ebc-e78f-4282-af07-ea3c509ea1c9.png)

Repulse Cell - Applies a pushing force in all 4 directions. <br>
![image](https://user-images.githubusercontent.com/71151507/126256027-cf7ef041-e25f-4b42-a5d8-ca7f0a8001a0.png)

Weight Cell - This cell will effectively remove the force from one mover that is trying to push it. They will stack with each other. <br>
![image](https://user-images.githubusercontent.com/71151507/126050791-9d8e1397-cad7-4137-97a1-e8d5bb40f2cf.png)

Cross Generator Cell - Clones in two directions. <br>
![image](https://user-images.githubusercontent.com/71151507/126051500-9b347b2a-0b6a-44c6-adfa-714374a4958f.png)

Strong Enemy Cell - An enemy cell that takes two hits to kill. <br>
![image](https://user-images.githubusercontent.com/71151507/126051507-b1d115c5-bcc6-41af-8f70-b32fbb13d633.png)

Freezer Cell - Stops adjacent cells from preforming their actions. Other cells will still treat them as normal. If a cell is moved next to it after it's subtick finishes, the cell will act normally.<br>
![image](https://user-images.githubusercontent.com/71151507/126086251-545d9fc6-6bb9-463d-9c85-de33d05621db.png)

Angled Generators - Generate at an angle. Rotation of the generated cell will be affected. <br>
![image](https://user-images.githubusercontent.com/71151507/126085128-11d6900b-ba94-4275-9d5b-9bd95307cbd1.png)
![image](https://user-images.githubusercontent.com/71151507/126085129-7a778814-2352-4d35-89d4-4ec5b4119da9.png)

Impulse Cell - Pulls cells 2 spaces away towards it. Can pull through trash cells and enemies.<br>
![image](https://user-images.githubusercontent.com/71151507/126256021-7ad374ce-d851-4522-a8b8-438a2306bc69.png)

Advancer Cell - Acts like a mover and puller combined. They are also, in a way, "smarter" than pullers, as if there is too much force going against them when they try to pull, they will just let go and only do the pushing.<br>
![image](https://user-images.githubusercontent.com/71151507/126256042-04006b8b-500b-428b-82d2-e10dbd3d3c98.png)

Flipper Cell - Will effectively "flip" the 4 neighboring cells horizontally or vertically, depending on it's own rotation. "Flipping" includes turning clockwise cells into counter-clockwise cells, and vice versa.<br>
![image](https://user-images.githubusercontent.com/71151507/126307519-0dea882f-cb75-4082-8b86-8ac5a3cef3ea.png)

Twist Generator Cell - Acts like a flipper and a generator combined.<br>
![image](https://user-images.githubusercontent.com/71151507/127073322-801b8fe9-34c9-4232-b8f0-7d5aaebf1436.png)

Gate Cell - Act like conditional (and semi-immobile) generator cells. They take in cells on their left and right, sort of acting like a trash cell, and clone the cell behind them if the condition is satisfied. <br>
From left to right: OR, AND, XOR, NOR, NAND, XNOR
![image](https://user-images.githubusercontent.com/71151507/127064896-f5d1c6d5-3062-439b-88d4-2ddf1f705a9f.png)
![image](https://user-images.githubusercontent.com/71151507/127064903-5fd4e6ec-3354-4fff-b69d-bfffb33a5e89.png)
![image](https://user-images.githubusercontent.com/71151507/127064924-07acf6ee-6a06-4d40-bd8c-98ec8695b5a3.png)
![image](https://user-images.githubusercontent.com/71151507/127064933-1cbd9f5a-a70c-48ae-af46-7b6a9dcd773c.png)
![image](https://user-images.githubusercontent.com/71151507/127064945-b49cc596-046d-46b9-b18e-b62112483798.png)
![image](https://user-images.githubusercontent.com/71151507/127064950-c689dded-9b02-44fe-8806-769a9c8b4bfd.png)

Current priority system (updating from left to right) <br>
![image](https://user-images.githubusercontent.com/71151507/127073266-165dfc09-01c7-469d-8e1a-d3a55e01f598.png) <br>
(Cross generators are like normal generators but are activated in two different subticks, and angled generators are both updated after normal/cross generators)<br>
(Twist generators update at the same time as normal generators)<br>
(All types of gate cells update at the same time)
