# hotel-dungeon

This game allows the player to navigate and explore a hotel that is described with a level file. A level file will specify the rooms on the first line delimited by a space, following that, each line will describe a room's pathway to another room.

The first room listed on the first line is the starting point of the level. The level file structure :

START FOYER ELEVATOR
START > NORTH > FOYER
FOYER > SOUTH > START
START > WEST > ELEVATOR

Each pathway is broken up by spaces and the > symbols. > WEST > this translates to: roomA's west's pathway connects to roomB:

Annotation for the test level file:

START FOYER ELEVATOR //START is the first room of the hotel.
START > NORTH > FOYER //START's north pathway connects to the FOYER
FOYER > SOUTH > START //FOYER's south pathway connects to the START
START > WEST > ELEVATOR //START's west pathway connects to the ELEVATOR

The commands that a player can input:

NORTH
SOUTH
EAST
WEST
QUIT

QUIT command allows the user to quit the program, please ensure that you clean up any memory you have allocated.

The NORTH, SOUTH, EAST and WEST commands will allow the player to move between the rooms via the room's pathways. Each room has a maximum of 4 pathways.

A room will outline if the paths that are available to it by specifying the direction at the side of the room. For example if the room has a path to another room by going north it will show N on the north side of the room.

If a user specifies a direction that does not have a pathway the program should output: No Path This Way

If the user inputs an invalid command the program should respond with: What?