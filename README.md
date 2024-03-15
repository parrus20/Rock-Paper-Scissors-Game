# Rock-Paper-Scissors-Game
Welcome to my first Python project! This is a simple rock-paper-scissors game where you can play against the computer. It's a fun way to practice your coding skills and have some entertainment at the same time. Give it a try and see if you can beat the computer!


This is a simple rock-paper-scissors game implemented in Python.

## How to Play

1. Run the Python script `rock_paper_scissors.py`.
2. Enter your choice when prompted (rock, paper, or scissors).
3. The computer will randomly select its choice.
4. The result of the game will be displayed.

#CODE
import random


def get_choices():
  player_choice = input("Enter a choice (rock, paper, scissors): ")
  options = ["rock", "paper", "scissors"]
  computer_choice = random.choice(options)
  choices = {"player": player_choice, "computer": computer_choice}
  return choices


def check_win(player, computer):
  print(f"You chose {player}, Computer chose {computer}")
  if player == computer:
    return "It's a tie!"
  elif player == "rock":
    if computer == "scissors":
      return "Rock smashes scissors! You win!"
    else:
      return "Paper covers rock! You lose."
  elif player == "paper":
    if computer == "rock":
      return "Paper covers rock! You win!"
    else:
      return "Scissors cuts paper! You lose."
  elif player == "scissors":
    if computer == "paper":
      return "Scissors cuts paper! You win!"
    else:
      return "Rock smashes scissors! You lose."


choices = get_choices()
result = check_win(choices["player"], choices["computer"])
print(result)


