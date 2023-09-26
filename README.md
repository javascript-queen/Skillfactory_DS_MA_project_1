# MIPT - Skillfactory - Data Science (MA)

# Project 1. Guess the number Game
## Table of Contents

1. Project Description

2. Which case is being solved?

3. Steps

4. Results
   
5. Conclusions

### 1. Project description
Guess the number guessed by the computer using the minimum number of attempts (less than 20 in our case).

### 2. Which problem is being solved? 
The initial program should guess the number guessed by the computer in the minimum number of attempts.

**The conditions of the game:**

- The computer guesses a number from 0 to 100, which is an argument of our program.
- The algorithm takes into account information about whether the random number is greater or less than what we need.

*Quality metric*

Results are assessed by the average number of attempts per 1000 repetitions

*What we practice*

The use of the Binary Search algorithm with Python and a simple guessing game.

### 3. Steps

**1. Choosing algorithm:**

Binary search is an efficient algorithm for finding an item from a sorted list of items. It works by repeatedly dividing in half the portion of the list that could contain the item, until you've narrowed down the possible locations to just one. 

**2. Using algorithm in our program:**

In order for the binary search to work, WE must keep track of OUR previous MAX & MIN guesses and work between them to constantly narrow the search regime.

- We set min = 0 and max = n + 1

- Compute the guess as the average round down to an integer if necessary.

- We return the number as a predicted value if they are the same.

- If the guess was low, then increase the min by one. We do not go below that minimum value.

- Otherwise, if the guess was too high, we should set the max = predicted value. We do not go above that maximum value.

### 4. Results

Eventually, the algorithm finds the best guess in less than 20 attempts. The average is 1 attempt according to the computation.

### 5. Conclusions

The Big O notation for Binary Search is O(log N). This algorithm works efficiently with sorted lists. We used the algorithm to be able to find the guessed number in less than 20 attempts.
