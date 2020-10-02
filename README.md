# Dice

This project demonstrates a game of dice called 10,000. 
It's a game my family and I play frequently and also has rules that become
more complex depending on a person's roll of the dice. I'll use this to
demonstrate pythonic knowledge.

## Definitions
*Player* - An object which tracks each person's name and updated score
throughout the game

*Score* - The total number of points earned in the player's roll

*Score Board* - Display of points and ranking per person based on their total points

*Dice* - A total of six six-sided dice

*Stay* - Deciding to no longer continue to roll and to then sum the points 
earned during their turn with their points on the score board, resulting
in a new total score for that player

## Requirements
* A player rolls all six dice at the beginning of their turn
* A player must get to 1000 points in a single turn to be placed on the score 
board
* A player must score some points each roll to continue their turn
* A player must keep the dice that scored points and continue to roll the
remaining after their first roll, only rolling all six once they have rolled all others
* When a player reaches 10,000 points or higher, they are temporarily
declared the winner, while each other player has one last turn to make more points than
the temporary winner

## Scoring

* Single ones = 100 points
* Single fives = 50 points
* A straight from one to six = 1500 points
* Three pairs = 1500 points
    * EXAMPLE Player rolled two twos, two threes, and two fours

**The following rules have exceptions when rolling ones**
* 3 of a kind = (100 points * face value of the dice)
    * EXAMPLE Player rolled three threes = 300 points (100 * 3)
* 4 of a kind =
[(100 points * face value of the dice) +
(100 points * face value of the dice)]
    * EXAMPLE Player rolled four threes = 600 points
    [(100 * 3) + (100 * 3)]
* 5 of a kind = [(100 points * face value of the dice) +
(100 points * face value of the dice) +
(100 points * face value of the dice)]
    * EXAMPLE Player rolled five threes = 900 points
    [(100 * 3) + (100 * 3) + (100 * 3)]
* 6 of a kind = [(100 points * face value of the dice) +
(100 points * face value of the dice) +
(100 points * face value of the dice) +
(100 points * face value of the dice)]
    * EXAMPLE Player rolled six threes = 900 points
    [(100 * 3) + (100 * 3) + (100 * 3) + (100 * 3)]

**The following rules are the exceptions for ones from the
previous rules**
* 3 of a kind = 1000 points
* 4 of a kind = 2000 points
* 5 of a kind = 3000 points
* 6 of a kind = 4000 points

## How to Play
1. The first player rolls all six die
2. The player may keep all or some of the dice in which points can be calculated from
3. The player rolls the remaining, non-scoring, dice
4. Steps 1 - 3 repeat until either:
    * A player reaches 1,000 points or higher and is one the board, and chooses to stay at the points they've earned
    * A player who is already on the board may choose to stop whenever they want to accumulate the points they've rolled so far
    * A player did not score any points in the roll, ending a players turn with no accumulation of the points earned in the previous rolls

# Example Game Play
Player Sophia rolls all six die which are: 1, 2, 3, 1, 6, 6.

This roll produced two potentially scoring die, the two ones.
Sophia may choose to keep both ones, or just one of the ones.
Sophia decides to keep both ones, meaning they can roll four dice, and update the score to 200 points.

The following roll produces: 5, 4, 4, 6.

Sophia must choose to take the 5 since it is the only scoring value, and roll the remaining three dice,
updating the score to 250 points.

The following roll produces: 2, 4, 6.

Sophia didn't reach 1,000 points and did not receive any scoring values this turn, resulting in 0
points total and the end of her turn.

Player Max then rolls all six die and rolls: 1, 1, 1, 4, 5, 6.

Max rolled 1,050 points from the three ones, and the five.
Max can now choose to stay, or keep all three ones, and roll the remaining three die.
Max would be on the score board if he chooses to stay
and won't risk losing all points like Sophia did.
Max chooses to roll again because he's feeling risky.

Player max rolls: 2, 4, 6.

Max just rolled a non-scoring roll, and now receives 0 points,
and does not make it on the score board.

It's Sophia's turn again and she rolls: 1, 1, 1, 4, 5, 6.

Sophia rolled 1,050 points from the three ones, and the five.
Sophia can now choose to stay, or keep all three ones, and roll the remaining three die.
Sophia would be on the score board if she chooses to stay
and won't risk losing all points like Max did.
Sophia chooses to stay, and is on the scoreboard with 1050 points.

The game now continues until Sophia has reached 10,001 points while Max is close at 8,000 points.
It's Max's final chance to beat Sophia by gaining over 2,001 points in his next turn.

Max rolls and gets: 4, 5, 6, 5, 3, 3.

Max gets 100 points from the two fives rolled and can choose to keep the two fives or continue.
Max decides to continue and finally loses because he did not get a score on one of his rolls