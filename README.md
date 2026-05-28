# Python Basics: Guessing Game
This repository contains basic Python projects, starting with a simple number guessing game.

## Guessing Game
Description
The 'Guessing Game' is a classic game where the computer picks a random number between 1 and 100, and the player tries to guess it. The game provides hints ('Too high!' or 'Too low!') until the player guesses the correct number.

## How to Run
Clone the repository (if on GitHub):

git clone <repository-url>
cd python-basics
Open the Python file or Colab Notebook: If you're in a Colab notebook, ensure the code cell containing the guess_the_number() function is present and execute it.

Execute the code: If you have the code in a .py file, run it from your terminal:

 ## python your_game_file.py
In a Colab notebook, simply run the cell containing the guess_the_number() function call.

Play the game: Follow the prompts to enter your guesses. The game will tell you if your guess is too high, too low, or correct.

import random

def guess_the_number():
  number = random.randint(1, 100)
  guess = None

  print("Welcome to the Number Guessing Game!")
  print("I'm thinking of a number between 1 and 100.")

  while guess != number:
    try:
      guess = int(input("Guess the number: "))

      if guess < number:
        print("Too low! Try again.")
      elif guess > number:
        print("Too high! Try again.")
      else:
        print("Correct! You guessed the number.")
    except ValueError:
      print("Invalid input. Please enter a whole number.")

# To play the game, uncomment the line below:
# guess_the_number()
