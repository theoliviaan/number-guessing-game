# number-guessing-game
A simple number guessing game using conditional statements and functions in python


```

from art import logo
import random


# Welcome message
print(logo)
print("Welcome to the number guessing game,where you try and figure out the number i chose\n\nSo, I am thinking of a number between 1 to 100")

# Computer guessed number
number = random.randint(1, 100)
# print(number)

# Choose a level

difficulty_level = True

# The question keeps getting asked if the user chooses an option that is not part of the options, lmaooo
while difficulty_level:
    difficulty = input("\nChoose a difficulty level. Do you want it  'easy' or 'hard'?: ").lower()

    if difficulty == "easy":
        attempts = 10
        print(f"\nYou chose the {difficulty.upper()} road, you have {attempts} attempts")
        difficulty_level = False
    elif difficulty == "hard":
        attempts = 5
        print(f"\nYou chose the {difficulty.upper()} road, you have {attempts} attempts")
        difficulty_level = False
    else:
        print("Not part of the options")






def play_game():
    game_is_on = True

    global attempts
    while game_is_on:
        user_guess = int(input("Try to guess the number, Choose from 1 to 100: "))


        if attempts == 1:
            print("\nNo more attempts, you lose")
            game_is_on = False
        elif user_guess < number:
            attempts -= 1
            print(f"\nToo low, you have {attempts} left")
        elif user_guess > number:
            attempts -= 1
            print(f"\nToo high, you have {attempts} left")
        else :
            print("\nYOU GOT IT, WE HAVE A WINNER!")
            game_is_on = False

play_game()







```
