# Additional Projects
Additional projects I have completed that are not located in any of my public repos.

*Code available for all projects upon request.*
## *Baba Is You* Lite
Implements the rules for a video game based on the existing game [*Baba Is You*](https://babaiswiki.fandom.com/wiki/Baba_Is_You_Wiki). 

*Baba Is You* is a puzzle game in which the player works to achieve
a win state by manipulating the environment in certain ways specified by the rules. However, the player is also allowed to manipulate the rules themselves.

The actual *Baba Is You* has many rules that are gradually revealed throughout the course of the game. This version only implements the basic push and pull rules, the ability to transform objects in the environment, and the ability to change the rules.

## LISP Lite Interpreter
Given code written in a basic version of LISP, interprets and evaluates the given code. The main functionality of this program is the creation of a REPL that supports the following operations:
- Defining variables
- Creating and manipulating linked lists (e.g. concatenating linked lists, finding the nth element of linked lists, etc.)
- Using conditional expressions (e.g. `if`, `and`, `or`)
- Defining functions
- Evaluating function calls

When running the program from the command line, there is also the option to add command line arguments corresponding to filenames. These files will be interpreted and evaluated before dropping into the REPL (i.e. the functions/variables in the files will be pre-loaded into the REPL environment).

## Symbolic Algebra Calculator
Given an expression of symbolic algebra that can contain either variables or numbers, can perform various operations on the expression, including:
- Differentiation with respect to a specified variable
- Simplification
- Evaluation, given a mapping of variables to values

Each of these operations returns a new symbolic algebra expression.

This program allows users to manually input symbolic alegbra expressions as strings. The following operators are supported by the parser: `+`, `-`, `*`, `/`, and `**` (exponentiation).

## File Downloader
Given a URL, constructs a generator that yields raw data from the URL in chunks of predetermined size (can be user-specified). This allows the user to start receiving data without having to wait for the whole file to be downloaded. This program supports yielding data from single files, sequences of files, and manifests. No data will be cached, except in the case where the program is yielding data from a manifest file and the manifest specifically indicates that a certain piece of data should be cached.

When running the code for this program from the command line, the user can add optional command line arguments corresponding to a URL and a filename. In this case, the program will save the file indicated by the URL to the specified filename on the user's computer. If the URL indicates a sequence of files, each file in the sequence will be saved as a different file on the user's computer, with the suffix `-file[num]` indicating its order in the sequence (e.g. `filename-file1`, `filename-file2`, etc.).

## Boolean Satisfiability Solving
Given a Boolean formula in [conjunctive normal form](https://en.wikipedia.org/wiki/Conjunctive_normal_form) (CNF), returns either a satisfying assignment of the Boolean variables or `None` if no such assignment exists.

Additionally, given a room scheduling problem, converts the problem into a Boolean formula. The room scheduling problem is represented as two dictionaries: one dictionary mapping people's names to room preferences, and the other mapping rooms to their numerical capacities.

## N-Dimensional Minesweeper
Implements the rules for playing a game of N-dimensional Minesweeper, where N is any positive integer. This program uses recursion to extend the logic of 2D Minesweeper to any number of dimensions. The rules of N-dimensional Minesweeper are the same as those of 2D Minesweeper. There are some number of bombs located throughout the game board. The player's job is to dig up all the squares without bombs while avoiding all the bomb-filled squares. Each dug-up square displays a number indicating the total number of bombs in neighboring squares. If a player digs up a bomb-less square whose neighbors are all also bomb-less, the neighboring squares are automatically dug up for the player. 

## Map Path-Finding
Given a map dataset from [OpenStreetMap](https://www.openstreetmap.org/about), finds the shortest path between any two locations on the map. This program utilizes the A* search algorithm and supports the following operations:
- Given two predetermined nodes on the map, returns the shortest path between them
- Given two locations in (latitude, longitude) form, returns the shortest path in terms of distance between them
- Given two locations in (latitude, longitude) form, returns the shortest path in terms of time (i.e. takes speed limits into account) between them

## Sokoban Solver
Given a level description for the puzzle game [Sokoban](https://en.wikipedia.org/wiki/Sokoban), returns a list representing the shortest sequence of moves to solve the level or `None` if no solution exists.

The solver function utilizes BFS to find the shortest possible sequence of moves.

## Image Manipulation
Given images represented as lists of pixels, performs various manipulations on those images. These manipulations include:
- Applying an inversion filter to the image
- Blurring the image
- Sharpening the image
- Applying a Sobel operator to the image (i.e. emphasizing the image's edges)
- Applying a ripple filter to the image

These manipulations can be used on both greyscale and color images.

## Audio Manipulation
Given audio files represented as lists of audio samples sampled at a set rate, performs various manipulations on those files. These manipulations include:
- Reversing the sound
- Mixing two sounds together
- Adding echoes to a sound
- Adding a pan effect

## RISC-V Processor
Implements a RISC-V processor in Minispec, a hardware language closely related to Bluespec. So-called "magic memory" modules are used to allow all instructions to be executed in a single cycle.


