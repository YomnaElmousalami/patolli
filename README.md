# patolli

# Patolli

## Simple two player Patolli Game
#### TO USE
1. `git clone https://github.com/yomnaE1/Patolli.git` repository and `cd patolli_game`

    If you are using an SSH Key: `git clone git@github.com:yomnaE1/Patolli.git` repository and `cd patolli_game`
3. To compile the code use the following commands:  
   - g++ -c main.cpp Board.cpp Player.cpp Referee.cpp
   - g++ -o patolli main.o Board.o Player.o Referee.o     
4. To run the code use the following command:
   - ./patolli
5. To stop the code type "CTRL + C"
  
# Project Design

The goal of this project was to create a two-player game where players compete to be the first to successfully maneuver all of their game pieces around the board. The pieces move based on a die-roll and in a clock-wise movement pattern. The squares at the ends of the cross shaped Board grant an additional turn to the player whose piece ended its move there. The four squares in the middle are the only squares on which capturing an opponent’s
piece is possible. Initially, the board is empty. On the first turn, the player can place their piece on the starting square and end their turn there. Then second player will then do the same. In this stage, the die roll doesn’t matter, regardless of the roll, the piece will start in its initial position and stay there until the next turn. Each player tosses a die in the beginning of the turn, the values on the dice are 0,1,2,3,4,5, and will be able to move a single piece by that many squares in the appropriate direction. A piece can only move forward in the clockwise direction and not back. Alternatively, the player may place one of their pieces on the board (usually done on low dice rolls), or pass their turn. A piece cannot occupy a square if another piece (enemy or not) is already there, except for the four middle squares. If an opponent’s piece occupies any of the middle squares, then, upon the appropriate die-roll, the player can remove that piece and replace it with their own. The removed piece goes back to the pool of available pieces for the opponent. Pieces can jump over both enemy and friendly pieces, as long as they don’t land in the same square. If a piece lands on any of the end squares, the player may roll the die again and move again any of their pieces. The player can also choose to forfeit their turn, either for strategic purposes or in the case where none of their pieces can legally move. Rolling a 0 is equivalent to losing your turn. When a piece reaches the end point, it is removed from the board and the player’s score is incremented by one (the scoring piece may not be played again). The piece has to land exactly on that end square. If based on the die roll, the piece overshoots and passes the end square, it must complete another turn in order to increment the score and the turn it has just completed will not count. The first player who has moved all six of their pieces to the end-point, wins. In case of incorrect input, the program should continue to prompt the user until a correct command is issued. When a player wins, the game should stop and a message indicating which player is victorious must be printed on the screen. Since all six pieces are identical but must be distinguished during the piece selection phase of the turn, they are represented as A, B, C, D , E ,F for player 1, and 1, 2, 3, 4, 5, 6 for player 2. Based on this piece scheme, player 1 will be called player L (Letter) and player 2 will be called player N (Number). Essentially, the project consists of two players, a referee, and a board. The referee acts as an interface between player and board, and not allow the player to cheat (player setting their own score, making illegal moves, etc.). 
