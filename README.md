# julia-sudoku-solvers

Examples of Sudoku solvers written in Julia. These were written to learn the Julia language, so they may not be the best solvers, but still useful and educational.

## Installation

Download the [latest stable version](https://github.com/selliott512/julia-sudoku-solvers/archive/v0.9.0.zip) of julia-sudoku-solvers and unzip it wherever you want.

```shell
unzip julia-sudoku-solvers-0.9.0.zip
```

## Scripts

Each of the three Julia scripts described below may be run by passing a "sud" file to it. For example, to solve the hardest sudoku ever:

```shell
julia bin/constraint-backtracking.jl sudokus/hardest.sud
```

### backtracking.jl

Applies backtracking to solve sudokus using a type of brute force exhaustive search.

### constraint-backtracking.jl

First constraints each of the 81 cells to the set of allowed values that cell. The constraining is done iteratively until no more constraints are found. Once the constraining is done, which by itself is sufficient for simple and medium difficulty sudokus, backtracking constrained to the allowed values for each cell is used. Additionally the backtracking is done so that the most constrained cells are considered first similar to how a human might solve a sudoku. This should be faster than "backtracking.jl", but in practice the additional complexity makes it slower in come cases.

### incomplete-algorithm-x.jl

A half written implementation of Algorithm X. Algorithm X uses exact cover to solve sudokus.
