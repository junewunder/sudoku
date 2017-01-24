# sudoku solver

A sudoku solver using the [Backtracking algorithm](https://en.wikipedia.org/wiki/Sudoku_solving_algorithms#Backtracking).

```
Initialize 2D array with 81 empty grids (nx = 9, ny = 9)
Fill in some empty grid with the known values
Make an original copy of the array
Start from top left grid (nx = 0, ny = 0), check if grid is empty
if (grid is empty) {
    assign the empty grid with values (i)
    if (no numbers exists in same rows & same columns same as (i) & 3x3 square (i) is currently in)
        fill in the number
    if (numbers exists in same rows | same columns same as (i) | 3x3 square (i) is currently in)
        discard (i) and repick other values (i++)
}
else {
    while (nx < 9) {
        Proceed to next row grid(nx++, ny)
        if (nx equals 9) {
            reset nx = 1
            proceed to next column grid(nx,ny++)
            if (ny equals 9) {
                print solution
            }
        }
    }
}
```
