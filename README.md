# Yay Sweeper
*A simple game written in JavaScript*

## Description
"Yay Sweeper" is a simple game based loosely on Minesweeper and is one of my first JavaScript projects.

## Goal of the game
The goal of the game is to contain all "boom" squares on the grid by clicking the orange "yay" squares on each side to trap them. You win when you have surrounded all blue "booms" with orange "yays." If you click a blue "boom" square, you lose.

## How to play
1. On startup, five blue "boom" squares will be placed randomly on the board. The text on the left ("YAYS FOUND") will tell you how many orange "yay" squares are on the board. There may be fewer than twenty (one for each side of the five "booms") if a blue boom square is located next to the edge of the board. The timer will be frozen at 00:00:00.
2. Click "Start Game" to begin. The stopwatch ("TIME") will begin counting up to keep track of how long you have been playing.
3. When you click a square on the board, it will turn dark gray (indicating this square is NOT a "boom" or "yay" square and will not affect your score), orange (indicating this is a "yay" square, which will increase your "YAYS FOUND" counter by 1), or blue (indicating a "boom" square, which will end the game immediately).
4. Once you find all orange "yay" squares, you win! If you click a blue "boom" square, you lose!
