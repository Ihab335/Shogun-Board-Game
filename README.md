# Shogun Board Game

**Shogun** is a strategic 2-player board game played on an 8x8 chessboard, combining elements of chess and checkers. Each player controls a king and seven pawns, with movement determined by energy levels.

## Features

- **Piece Energy:** Pawns have energy between 1–4, and kings have energy between 1–2, determining how far pieces can move.
- **Dynamic Movement:** Pieces move in straight lines or L-shaped patterns, without diagonal moves or backward steps.
- **Capture:** Pieces capture by landing on occupied fields, removing the opponent’s piece.

## Implementation

This repository contains an implementation of Shogun’s piece movement functions. It includes data structures for positions, colors (red or white), and pieces (pawn or king). Functions for incrementing and decrementing coordinates are provided in the template file.

## Usage

To set up the game, create an initial board configuration using the `Board` class:

```scala
val b_init = Board(Set(King(2, Wht, (4, 1)), King(1, Red, (5, 8)),
                       Pawn(4, Wht, (1, 1)), Pawn(4, Red, (1, 8)),
                       Pawn(2, Wht, (8, 1)), Pawn(3, Red, (8, 8))))


```
Then, find legal moves for a piece:

```scala
val pw1 = Pawn(4, Wht, (4, 6))
legal_moves(pw1, b_init)
