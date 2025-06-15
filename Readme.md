# Tic-Tac-Toe with AI

A C++ implementation of the classic Tic-Tac-Toe game featuring an unbeatable AI opponent using the Minimax algorithm.

## Project Overview

This project was created as a learning exercise to understand:
- Implementation of the Minimax algorithm
- Game state management
- Basic AI decision making
- C++ programming concepts

## Features

- Player vs AI gameplay
- Unbeatable AI opponent
- Clean console interface
- Move validation
- Available moves display
- Option to play multiple games

## How to Run

1. Ensure you have a C++ compiler installed (g++ recommended)
2. Compile the code:
```bash
g++ game.cpp -o main
```
3. Run the executable:
```bash
./main.exe
```

## Understanding the Minimax Algorithm

The Minimax algorithm used in this project is a decision-making algorithm that plays a crucial role in the game's AI. Here's how it works:

### Basic Concept
Minimax is a recursive algorithm that helps the AI determine the best possible move by:
- Maximizing the AI's chances of winning
- Minimizing the player's chances of winning

### How it Works in This Project

1. **Scoring System:**
   - Win: +10 for AI, -10 for Human
   - Draw: 0
   - Loss: -10 for AI, +10 for Human

2. **Algorithm Flow:**
   - The algorithm simulates all possible moves
   - For each move, it recursively evaluates future game states
   - The AI (maximizer) tries to get the highest score
   - The Human (minimizer) is assumed to play optimally to get the lowest score

3. **Implementation Details:**
```cpp
int minimax(vector<vector<char>>& board, int depth, bool is_ai) {
    // Base cases: game over or board full
    if (game_over(board)) return is_ai ? -10 : 10;
    if (depth == 9) return 0;

    // Recursive case
    int best_score = is_ai ? -9999 : 9999;
    for (each empty cell) {
        make move
        evaluate score
        undo move
        update best_score
    }
    return best_score;
}
```

## Resources Used

- C++ Standard Library
- Minimax Algorithm Documentation
- Game Theory Concepts

