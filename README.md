# chess

We have uploaded several version of the game. Each new file has new criteria added. 
The final codes can be found from the folder "Final Codes"

There will be files where one file generates histogram data of 100 games of 5 different board arrangements. Other two files contain the  separate contribution of 
two collaborators. If any more files are found, then the details are also given in the commit. 
We have implemented AI vs AI, AI vs NN, Human vs AI , Tree vs AI and Tree vs Tree chess game. Users will choose which one they want to play in which instance. 
They will also get option to customize the board. 
We didn't implement human vs human because it was not required, but it should be really easy now.


Proper attribution and link to any existing code used in project:

We are planning to implement this chess960 version in our code: https://github.com/aStieber/Chess960/blob/master/README.md instead of using the library

For monte carlo implementation, we took help from https://www.geeksforgeeks.org/ml-monte-carlo-tree-search-mcts/

For stockfish and evaluation implementation: https://python-chess.readthedocs.io/en/latest/engine.html

To use the pychess library : https://python-chess.readthedocs.io/en/latest/

For neural nework we took idea from: https://www.chess.com/blog/the_real_greco/understanding-alphazero-a-basic-chess-neural-network

We used kggle data to train our neural network model. here is the link of the dataset: 
https://www.kaggle.com/code/gabrielhaselhurst/chess-dataset/data

Installation :
We used python 3.6 code. To run the code, we need to install the dependencies: 
Write "pip install chess" in command prompt to install the chess library
then "brew install stockfish" for evaluation result. (in mac)
If you are using any other operating system, download stockfish for your os from https://stockfishchess.org/download/
install tensorflow, numpy , pandas , keras for neuralnetwork
pip install numpy
pip install pandas
pip install keras
pip install https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.8.0-py3-none-any.whl
For tensor flow it is recommended to use python 3.6 , otherwise it may create issue while importing.


Explanation of how to run the computer experiments:

The board is randomized and user can choose one piece to have in the board. 
Initially we created 5 different problem instances where each board had different piece arrangements and mostly less than the total pieces to handle the time issue.
The game is Ai , baseline tree , Neural network and human based. You will be asked with options what you want. User will get proper prompts for each question with guideline.

At best , there can be 16 pieces for each players. There will be 8 pawns, 2 bishops, 2 knights, 2 rooks, 1 queen, and 1 king.
White side will have first letters of all the pieces with small letter (p,b,k,r,q,k) and human will have all the pieces with capital letter (P,B,K,R,Q,K).


If you choose AI vs human, After you run the code, AI will give the first move and you will be the second player. 
human needs to give two input each time. First one is where they want their piece to go and second one is the row and colum of which piece they want to move. here row is from a to h and colum is from 1 to 8.
If you choose invalid move, game will be over that time.

You will get the row and colum idea from the following image:
https://github.com/mhatresahil/chess/blob/45c28b5a1222ea45713b43a812814619f12fb4a9/Screenshot%202022-12-02%20at%207.23.30%20PM.png

Sometimes the program shows engine time ended error when we try to run neural network and stockfish engine together. Sometimes it shows the same error for AI vs 
tree game as well because the NN was executed recently which takes comparatively more time. The error can be solved using less epochs and smaller board after restarting the kernal

For histogram generation, there is no input required. It generated histograms for 100 games for each problem instances  based on evaluation method that we have implemented. Thw 100 games were not identical at all. We used randomization of AI vs Ai, tree vs ai , tree vs tree and also random starting position. 
