# Architecture
![UML](https://github.com/nuPURohit/LTTS_MiniProject_StepIn/blob/main/2_Architecture/chess_engine_uml.png)

*  Referring to the following gameboard setup:
![Gameboard_Setup](https://github.com/nuPURohit/LTTS_MiniProject_StepIn/blob/main/6_ImagesAndVideos/Screenshot%202021-04-12%20163251.png)
*  Rank => Rows(1 to 8)  Files => Columns(a to h)
*  UpperCase => White Piece Lowercase => Blackpiece
## King "K" "k" 
One Step in any direction
## Rook "R" "r"
Straight: North,South,East,West
## Bishop "B" "b"
Diagonal: North-East, South-East, Nort-West, South-West
## Queen "Q" "q"
All moves of King, Rook and Bishop are valid
## Knight "N" "n"
"L"-shape: two squares vertically and one square horizontally, or two squares horizontally and one square vertically
## Pawn "P" "p"
Initially two steps front. Then 1 step front. To kill => Diagonal (North-East or North-West)
### Castling
Moving the king 2 squares along the 1st rank towards a rook on the player's 1st rank and then placing the rook on the last square that the king crossed.
Only if: (i) Niether K or R has previously moved 
         (ii) No pieces b/w K and R
         (iii) K is not in check
         (iv) Only if the rook is under attack
### EnPassant
When a P makes a 2 step advance from its starting position and there is an opponent pawn a square next to the destination square on an adjacent file then the opponent's pawn can capture it (in passing), moving to the square that the pawn crossed over (Must be done in the very next move)
### Promotion
When a P advances to the 8th rank, it is promoted and must exchange for the player's choice of Q,R,B,N of the same colour
### Check and checkmate
When a king is under immediate attack by one or two of the opponents pieces, it is said to be in check. A move in response to a check is legal only if it results in a position where the king is no longer in check. The object of the game is to checkmate the opponent this occurs when the opponent's king is in check and there is no legal way to remove it from attack.
### Stalemate and Dead
If the player to move has no leagal moves, but it is not in check, the position is a stalemate and the game is drawn --> dead position ex. if only 2 kings are left on the board
