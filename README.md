# Optimal Game Strategy Using Dynamic Programming

## Problem Description
This is a two-player game where an even number of coins are arranged in a row. Players take turns alternately. In each turn, a player can either select the first coin in the row or the last coin and keep it. The objective is to determine the maximum possible amount of money a player can definitely win if they move first.

## Problem Solution
To solve this problem optimally, we need to ensure that the player collects the maximum amount while taking into account the opponent’s possible moves. The approach involves choosing either the first or last coin in the row while considering the option that leaves the opponent with the least advantage. We use dynamic programming to compute the optimal strategy efficiently.

## Expected Input and Output
### Example:
```plaintext
Coins [] = [4, 15, 7, 3, 8, 9]
Expected Result = 27
```

### Program Output:
1. The expected result.
2. The DP table used in calculations.
3. The sequence of coins picked that leads to the optimal result.
4. A graphical or text-based user interface demonstrating the result.

## Implementation Details
- Use a 2D DP table where `dp[i][j]` stores the maximum value a player can collect from coins in the range `i` to `j`.
- The table is filled iteratively using a bottom-up approach.
- The final result is stored in `dp[0][n-1]`, where `n` is the number of coins.

## Example DP Table Representation
For `Coins = [4, 15, 7, 3, 8, 9]`, the DP table might look like this:

|   | 0  | 1  | 2  | 3  | 4  | 5  |
|---|----|----|----|----|----|----|
| 0 |  4 | 15 | 15 | 18 | 23 | 27 |
| 1 |    | 15 | 15 | 10 | 18 | 22 |
| 2 |    |    |  7 |  7 | 15 | 16 |
| 3 |    |    |    |  3 |  8 |  9 |
| 4 |    |    |    |    |  8 |  9 |
| 5 |    |    |    |    |    |  9 |

## User Interface
The program should present:
- A clear output of the expected result.
- A visual representation (table or text) of the DP table.
- A breakdown of the optimal sequence of moves.
- A simple and intuitive interface for users to input their own set of coins.

## Good Luck!
Implement the program effectively using Dynamic Programming and ensure correctness in results!
