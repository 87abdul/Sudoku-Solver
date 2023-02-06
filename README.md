# Introduction
A bunch of C++ programs which deal with Sudoku Puzzles, Sudoku Puzzle Validation.



# Sudoku-Solver
This is a program which solves 9x9 Sudoku puzzles.
This program reads input either from a user or from a file containing the Sudoku values and solves the puzzle.
 It employs concepts such as backtracking and recursion.

### Getting Started
* Simply download the ```sudoku-solver.cpp``` file found in the ```Sudoku-Solver/``` directory.
 Run it using any standard C++ compiler.
 In case of any errors or compatibility issues, submit an issue in this git.
* Once downloaded, compiled and run; the program will require the user to input the Sudoku puzzle into it. There are two ways to do this.
    * The user can either input the values manually.
    * The user can write all the values into a file, seperated by whitespaces. 
     the user will be prompted to simply enter the name of the file (with extension). 

    Example: ```input.txt```
    
        ```
            0 0 0 0 0 4 0 9 0
            8 0 2 9 7 0 0 0 0
            9 0 1 2 0 0 3 0 0

            0 0 0 0 4 9 1 5 7
            0 1 3 0 5 0 9 2 0
            5 7 9 1 2 0 0 0 0

            0 0 7 0 0 2 6 0 3
            0 0 0 0 3 8 2 0 5
            0 2 0 5 0 0 0 0 0
        ```

* Once solved, the Sudoku puzzles shall be displayed like this.
    ```
            ++=====================================++
            || 7   3   5 || 6   1   4 || 8   9   2 ||
            ++-----------++-----------++-----------++
            || 8   4   2 || 9   7   3 || 5   6   1 ||
            ++-----------++-----------++-----------++
            || 9   6   1 || 2   8   5 || 3   7   4 ||
            ++=====================================++
            || 2   8   6 || 3   4   9 || 1   5   7 ||
            ++-----------++-----------++-----------++
            || 4   1   3 || 8   5   7 || 9   2   6 ||
            ++-----------++-----------++-----------++
            || 5   7   9 || 1   2   6 || 4   3   8 ||
            ++=====================================++
            || 1   5   7 || 4   9   2 || 6   8   3 ||
            ++-----------++-----------++-----------++
            || 6   9   4 || 7   3   8 || 2   1   5 ||
            ++-----------++-----------++-----------++
            || 3   2   8 || 5   6   1 || 7   4   9 ||
            ++=====================================++
    ```


# Sudoku Validator
This is a program which validates solutions for 9x9 Sudoku puzzles.
This program takes in input from the user or from a file containing the values.
 It then validates the puzzle and then displays whether it is a valid solution or not.
    
    Example: ```input.txt```
    
        ```
            0 0 0 0 0 4 0 9 0
            8 0 2 9 7 0 0 0 0
            9 0 1 2 0 0 3 0 0

            0 0 0 0 4 9 1 5 7
            0 1 3 0 5 0 9 2 0
            5 7 9 1 2 0 0 0 0

            0 0 7 0 0 2 6 0 3
            0 0 0 0 3 8 2 0 5
            0 2 0 5 0 0 0 0 0
        ```


### How It Works
The workings of the Sudoku Validator are quite simple, to be honest. Here's a simple algorithm explaining them all.

1. Start
2. The values in all the cells are checked to see if they are in the range 1-9. If not, the puzzle is invalid.
3. Every row is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
4. Every column is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
4. Every 3x3 grid is checked to see if it contains 1-9 atleast once. If not, the solution is invalid.
5. If all the criteria have been satisfied, the solution is valid.
6. Stop
