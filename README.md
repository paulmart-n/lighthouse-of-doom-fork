# The Lighthouse of Doom

This repository contain a simple text-based adventure game,
implemented in portable C.

Quick links within this README file:

* [Plot of the game](#game-plot)
* [Implementation](#implementation)
* [Compiling & running it](#compiling--running-it)
* [Downloading It](#downloading-it)
* [Bugs?](#bugs)


## Game Plot

* You're inside a lighthouse (trapped? doesn't really matter I guess).
* You see a boat on the horizon, heading your way.
* But "oh no!", the lighthouse is dark.
  * The boat will surely crash if you don't turn on the main light.

The game is over, when you either fix the light, or find another solution.

If you do not achieve victory within a turn-limit the boat runs
aground, and death will consume you all.  (It is a _very_ big boat!)


## Implementation

The implementation is mostly concerned with creating the correct
series of data-structures, which are essentially arrays of objects.
Because if we can make the game table-based we simplify the coding
that needs to be done -- we don't need to write per-object handlers
anywhere, we can just add pointers to tables/structures.

The implementation defines most of the important things in the file
[include/globals.h](globals.h) such as:

* The structure to define a location.
* The structure to define an object.

The game-state itself is stored in a couple of global variables, there
isn't too much state to care about:

* The current location (i.e. index into location-table).
* A list of any items you're carrying.
* The number of turns you've taken.
  * Incremented by one each time you enter a command, be it recognized or not.
* Whether you won/lost.


## Compiling & Running It

Excercice: create a cmake file for compiling and running this game on
both Linux and Windows.
