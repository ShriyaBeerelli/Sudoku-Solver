

# 🧩 Sudoku Solver in C++ Using Backtracking & Bitmasking

Solve any 9x9 Sudoku puzzle efficiently with this C++ program that combines classic backtracking and smart bitmasking optimizations to rapidly find solutions.

***

## 🚀 Project Overview

Sudoku challenges you to fill a 9x9 grid so every row, column, and 3x3 sub-box includes digits 1 through 9 exactly once. This solver uses a **recursive backtracking approach enhanced with bitmasks** to quickly check if placing a number violates Sudoku rules, making it much faster than naive methods.

***

## ✨ Key Features

- **Backtracking Search:** Systematically tries numbers in empty cells, retreats on dead ends until the puzzle is solved
- **Bitmask Optimization:** Tracks filled numbers per row, column, and box with bits for lightning-fast validity checks (O(1))
- **Dynamic Mask Updates:** Efficiently marks and unmarks placed numbers during recursion for clean backtracking
- **Compact & Readable:** Clear structure with separated safety checks and solving logic
- **Hardcoded Puzzle:** Comes with a sample Sudoku puzzle for immediate testing

***

## 🛠️ How It Works

- **Bitmasks for Rows, Columns & Boxes:**  
  Integer bitmasks represent which numbers are placed in each row, column, and 3x3 box.  
- **Safety Check (isSafe):**  
  Uses bit comparisons to confirm if a number can be placed without collisions.  
- **Recursive Solver (sudokuSolverRec):**  
  Moves cell by cell, placing a number only when safe. If all cells are filled correctly, returns success.  
- **Backtracking:**  
  On invalid moves, undoes assignments and tries alternatives until a solution emerges.

***

## 📋 Usage

1. Compile the code with a C++ compiler (e.g., `g++ sudoku.cpp -o sudoku`)  
2. Run the executable (`./sudoku`)  
3. View the solved Sudoku printed in the terminal

***

## 🧮 Sample Input Puzzle

```
3 0 6 5 0 8 4 0 0
5 2 0 0 0 0 0 0 0
0 8 7 0 0 0 0 3 1
0 0 3 0 1 0 0 8 0
9 0 0 8 6 3 0 0 5
0 5 0 0 9 0 6 0 0
1 3 0 0 0 0 2 5 0
0 0 0 0 0 0 0 7 4
0 0 5 2 0 6 3 0 0
```

***

## 🏁 Sample Output (Solved Puzzle)

```
3 1 6 5 7 8 4 9 2
5 2 9 1 3 4 7 6 8
4 8 7 6 2 9 5 3 1
2 6 3 4 1 5 9 8 7
9 7 4 8 6 3 1 2 5
8 5 1 7 9 2 6 4 3
1 3 8 9 4 7 2 5 6
6 9 2 3 5 1 8 7 4
7 4 5 2 8 6 3 1 9
```

***

## ⚙️ Why Bitmasking?

By encoding used numbers as bits in integers for rows, columns, and boxes, the program:

- **Performs instant lookups** to check if a digit is free or taken  
- Avoids costly loops over arrays/checks  
- Makes backtracking updates seamless and efficient

This drastically speeds up the solving process, especially for complex puzzles.

***

## 📜 License

 freely use, modify, and share.

***

This README makes your Sudoku project stand out by combining technical accuracy, clarity, and effective presentation to engage developers and Sudoku enthusiasts alike.
