![minimax](https://user-images.githubusercontent.com/83718657/118381638-d8285b00-b5ba-11eb-9179-394cdf152c6d.png)
# Tic-Tac-Toe

TicTacToe too easy? Competition too soft? This AI will give you a run for your money!
With the use of the MiniMax Algorithm, you can say goodbye to the W's. Play against an unbeatable
AI in TicTacToe and watch your ego drop to the floor!

### How To Play?
Click on the square you wish and the AI will instantly find a counter!
As always, first to three in a row wins. If neither gets three in a row,
it is a tie (noone wins).
Have fun!

## What is the MiniMax Algorithm?

Within the large variety of backtracking algorithms, the MiniMax (search) algorithm is used in decision
making and game theory in order to attain the most optimal move with the idea that the opponent
also makes the most optimal decision. In essence, this algorithm calculates all the moves with the
utility of the board for the future. 

The name MiniMax describes the two goals that this algorithm must execute. For two player games, 
two players are working towards opposite goals to make predictions about which future states will be 
reached as the game progresses, and then proceeds accordingly to optimize its chance of victory.
In the algorithm, one player is called the maximizer, and the other player is a minimizer. 
Suppose we state a scoreboard for the game, the maximzer would try to choose a game state with 
the maximum score, while the minimizer tries to choose a state with the minimum score. Each player would 
try to counter each other, given that each makes the best possible move as aformentioned.

### Visualization
<p align="center">
<img width=1000 src="/wp-content/uploads/2017/07/minimax.png">

</p>

We visualize this method of finding states and different versions of the game (which depends on different
turns) by looking at a tree diagram as each branch is formed with the selection of each move.

Time Complexity: O(b^m) 
                  Where b is branching factor of the game-tree, and m is the maximum depth of the tree
                  
## Future Improvements/Implementations

### Limitations
Despite this algorithm being extremely useful in finding the best moves, an exhaustive use of the minimax algorithm
tends to be hopelessly impractical and, for many win-or-lose games, uninteresting. TicTacToe may not be the most optimal
example to show this, but for more complex games such as Chess or Mancala, there are extremely large amounts of states that
the games are able to take on in the future. Therefore efficiency is a large limitation for the MiniMax method when considering
the worst possible scenarios.



### Improvements
These limitations may seem jarring and helplessy difficult to fix as we might initially think that we must evaluate every node due to 
the unpredictability of the player, however, major improvements can be made thanks to Alpha-Beta Pruning.

Alpha-Beta Pruning allows us to set a limit on how far we want to "look into the future". This means that we can limit the number of
turns we can search into, allowing us to find the most optimal move from looking at a limited number of turns into the future. In terms
of the points system, we would only look at the move that would give us a limited number of points and losing a limited number of points.
This is done with adding parameters _alpha_ and _beta___. Alpha is the best value that the maximizer currently can guarantee at that level or above.
Beta is the best value that the minimizer currently can guarantee at that level or above. To simplify, we understand that making the absolute best 
decision in game does not always require us to look at every turn and state.

These improvements of implementing Alpha-Beta Pruning within our MiniMax algorithm will allow us to improve the efficiency of my code substanstially.
We are able to notice these changes in the beginning of the game as there are more possible future states when there is a clean board. We can see these 
improvements mathematically as well.

Time Complexity:  O(b^(d/2)) 
                  where b = branching factor and d = depth of the tree, and the base case is when all the preferred nodes are expanded first
                  
## Summary and Experience

### What I learned

I learned a lot during this process, I had some struggle on how I could code this algorithm at first but with some drawings and test cases, I was 
able to understand it well. I realized the inefficiency and learned how I could implement some improvements as well. This was a new experience
for me as this is the trickiest recursive function I wrote. 

### Summary
I implemented an unbeatable AI in TicTacToe using the MiniMax Search Algorithm. I was able to improve the efficiency using Alpha-Beta Pruning.


