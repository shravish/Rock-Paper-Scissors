# Rock-Paper-Scissors
## Python program to implement Rock Paper Scissor game
Python is a multipurpose language and one can do anything with it. Python can also be used for game development. Let’s create a simple command-line Rock-Paper-Scissor game without using any external game libraries like PyGame. In this game, the user gets the first chance to pick the option between Rock, paper, and scissors. After the computer select from the remaining two choices(randomly), the winner is decided as per the rules.

```
Winning Rules as follows:
Rock vs paper-> paper wins
Rock vs scissor-> Rock wins
paper vs scissor-> scissor wins.
```
In this game, randint() inbuilt function is used for generating random integer values within the given range.

## Implementation: 

```
import random

# Print multiline instruction
print('Winning rules of the game ROCK PAPER SCISSORS are:\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissors wins \n")

while True:

    print("Enter your choice \n 1 - Rock \n 2 - Paper \n 3 - Scissors \n")

    # Take the input from user
    choice = int(input("Enter your choice: "))

    # Looping until user enters valid input
    while choice > 3 or choice < 1:
        choice = int(input('Enter a valid choice please : '))

    # Initialize value of choice_name variable corresponding to the choice value
    if choice == 1:
        choice_name = 'Rock'
    elif choice == 2:
        choice_name = 'Paper'
    else:
        choice_name = 'Scissors'

    # Print user choice
    print('User choice is:', choice_name)
    print("Now it's Computer's Turn...")

    # Computer chooses randomly any number among 1, 2, and 3
    comp_choice = random.randint(1, 3)

    # Initialize value of comp_choice_name variable corresponding to the choice value
    if comp_choice == 1:
        comp_choice_name = 'Rock'
    elif comp_choice == 2:
        comp_choice_name = 'Paper'
    else:
        comp_choice_name = 'Scissors'

    print("Computer choice is:", comp_choice_name)
    print(choice_name, 'vs', comp_choice_name)

    # Determine the winner
    if choice == comp_choice:
        result = "DRAW"
    elif (choice == 1 and comp_choice == 2) or (comp_choice == 1 and choice == 2):
        result = 'Paper'
    elif (choice == 1 and comp_choice == 3) or (comp_choice == 1 and choice == 3):
        result = 'Rock'
    elif (choice == 2 and comp_choice == 3) or (comp_choice == 2 and choice == 3):
        result = 'Scissors'

    # Print the result
    if result == "DRAW":
        print("<== It's a tie! ==>")
    elif result == choice_name:
        print("<== User wins! ==>")
    else:
        print("<== Computer wins! ==>")

    # Ask if the user wants to play again
    print("Do you want to play again? (Y/N)")
    ans = input().lower()
    if ans == 'n':
        break

# After coming out of the while loop, print thanks for playing
print("Thanks for playing!")

```

## Output: 

```
Winning rules of the game ROCK PAPER SCISSORS are:
Rock vs Paper -> Paper wins 
Rock vs Scissors -> Rock wins 
Paper vs Scissors -> Scissors wins 

Enter your choice 
 1 - Rock 
 2 - Paper 
 3 - Scissors 

Enter your choice: 1
User choice is: Rock
Now it's Computer's Turn...
Computer choice is: Paper
Rock vs Paper
<== Computer wins! ==>
Do you want to play again? (Y/N)
y
Enter your choice 
 1 - Rock 
 2 - Paper 
 3 - Scissors 

Enter your choice: 2
User choice is: Paper
Now it's Computer's Turn...
Computer choice is: Paper
Paper vs Paper
<== It's a tie! ==>
Do you want to play again? (Y/N)
n
Thanks for playing!

```

## Code Explanation:

    1.The code starts by printing a message that states the rules of the game.
    2.The first line in the code prints “Rock vs paper->paper wins.”
    3.This is because if you have a rock, and you play against someone who has a piece of paper, the rock will beat the paper.
    4.The next line in the code prints “Rock vs scissor->Rock wins.”
    5.This is because if you have a rock, and you play against someone who has a scissors, the rock will beat the scissors.
    6.The last line in the code prints “paper vs scissor->scissor wins.”
    7.This is because if you have a piece of paper, and you play against someone who has a scissors, then the piece of paper will beat the scissors.
    8.The code will print the following output: Winning Rules of the Rock paper scissor game as follows: Rock vs paper->paper wins Rock vs scissor->Rock wins paper vs scissor->scissor wins
    9.The code starts by asking the user for a choice.
    10.The code then checks to see if the input is 1, 2, or 3.
    11.If it is not one of those values, the code sets the choice_name variable to ‘Rock’ if choice == 1, ‘paper’ if choice == 2, and ‘scissor’ if choice == 3.
    12.The next part of the code asks the user for their computer turn.
    13.The code uses a random number generator to choose between 1, 2, and 3.
    14.This value is stored in comp_choice_name.
    15.Next, the code loops until comp_choice equals choice.
    16.In each loop iteration, comp_choice will be randomly chosen from 1-3 and stored in comp_choice_name.
    17.Once comp_choice equals choice, this means that the computer has chosen rock as its turn!
    18.Finally, it prints out both choices so that everyone can see what happened (user choice is: Rock V/s paper; Computer choice is: Rock V/s scissor).
    19.The code will ask the user for a choice between rock, paper and scissors.
    20.Once the user enters their choice, the code will randomly choose one of those options as the computer’s turn.
    21.The code then prints out the chosen option and the user’s choice.
    22.Finally, it loops back to ask for another choice from the user.
    
