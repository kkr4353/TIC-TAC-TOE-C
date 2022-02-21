# TIC-TAC-TOE-C
 
# TITLE : Multiclient TIC-TAC-TOE

					SKolla_KKanjula
				
					|  
					|_ pipe-hw3.c
					|  
					|_ local.h  
					|_ intserver.c 
					|_ intclient.c  
                                    |
					|_ tttlocal.h
					|_ ttclient.c
					|_ tttserver.h
					|_ README.md    
					
	
  
In this project, we have implemented a multiclient tic tac toe with the help of socket programming in C. Multiple clients in the LAN can connect to server using hostname of the server through an assigned port and can play the game simulataneously. 

# RULES :        

* Three rows are represented as 1,2,3.
* Three columns are represented as 1,2,3.
* If you need to select a cell in the first row - second column you will have to input (1,2).
* The cell marked by the client is represented by 'X' and the cell marked by the server is represented by 'O'.
* A player wins if all the three cells in any row or column or diagonally have same symbol 'X' or 'O'.
* If there is no chance of winning, the game will be tied.

# FLOW : 

The client will be displayed a tic tac toe board initially and is prompted to enter row, column values separated by a comma for the box they want to mark. It will then send the row, column values along with the current board to the server. 

The server after receiving the current board along with the row, column values from the client checks if the input from the user is valid.

If the values are invalid, the user is prompted to enter a valid input.

If the values are valid server will check if the game has ended that is either server wins, the client wins or the game is tied.

If yes, it will go ahead and send the client that the game has ended and the client prints the status and terminates the game.

If not it will go ahead and check if there is any possibility for the server to win, if yes it will mark the box and the server wins.

If there is no possibility it will check for the possibility for the client to win and block the possibility.

The server then sends the row-column values along with the board to the client. 

The client after receiving the row-column values along with the current board updates the board and checks if the game has ended.

If not it will prompt the user to enter a row and column value where the client wants to mark.

It will then send the row-column values along with the current board to the server and the loop continues.
  
