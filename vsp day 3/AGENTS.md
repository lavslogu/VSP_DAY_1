# Sudoku Puzzle Solving Instructions

Use these instructions when asked to solve, check, or explain a Sudoku puzzle in this workspace.

## Input format

- Standard Sudoku is a 9×9 grid with digits 1–9 and empty cells represented by `0`, `.`, or a blank.
- Read rows in order from top to bottom and cells from left to right.
- If the puzzle is incomplete or its row boundaries are unclear, ask for a corrected grid before solving.
- If the user specifies a variant (for example, diagonal Sudoku), apply its extra rules as well as the standard rules.

## Rules

In a standard Sudoku, every digit 1–9 must appear exactly once in each row, each column, and each 3×3 box. Never alter a given clue.

## Solving workflow

1. Transcribe the givens into a 9×9 grid and check that every row has nine entries.
2. Check for immediate contradictions: duplicate nonzero digits in any row, column, or box.
3. Solve by tracking candidates for empty cells. Prefer direct deductions such as naked singles and hidden singles; then use pairs, locked candidates, and other valid elimination techniques as needed.
4. If logical deductions stall, use systematic backtracking: choose an empty cell with the fewest candidates, try a candidate, and backtrack when it creates a contradiction. Do not guess without checking consistency.
5. Preserve the original givens and continue until all cells are filled.
6. Validate the completed grid independently: each row, column, and 3×3 box contains every digit 1–9 exactly once, all original clues are unchanged, and any variant constraints hold.
7. If the puzzle has no solution or multiple solutions, report that clearly instead of presenting an unverified grid as unique. Mention whether uniqueness was checked.

## Response

- Present the answer as nine rows of nine digits, using a readable monospace block.
- When useful or requested, explain the key deductions without claiming a technique that was not used.
- If the input is invalid, point out the conflicting clue locations or the specific formatting problem.
