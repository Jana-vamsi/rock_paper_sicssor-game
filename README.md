Rock-Paper-Scissors Game
Overview
This is a simple command-line Rock-Paper-Scissors game implemented in Python. The user plays against the computer, and the game determines the winner based on the classic rules of Rock-Paper-Scissors.

Features
User can choose between rock, paper, or scissors.
The computer randomly selects one of the three options.
The game determines the winner based on the choices made.
The result of each round is displayed to the user.
Requirements
Python 3.x
How to Run the Game
Clone the Repository (if applicable):

bash
Run
Copy code
git clone <repository-url>
cd <repository-directory>
Run the Script:

Open a terminal or command prompt.
Navigate to the directory where the script is located.
Run the following command:
bash
Run
Copy code
python rock_paper_scissors.py
Follow the Prompts:

Enter your choice when prompted (rock, paper, or scissors).
The computer will make its choice, and the result will be displayed.
Code Explanation
Here is the code for the Rock-Paper-Scissors game:

python
Run
Copy code
import random

def get_computer_choice():
    choices = ['rock', 'paper', 'scissors']
    return random.choice(choices)

def get_user_choice():
    user_input = input("Enter your choice (rock, paper, scissors): ").lower()
    while user_input not in ['rock', 'paper', 'scissors']:
        print("Invalid choice. Please try again.")
        user_input = input("Enter your choice (rock, paper, scissors): ").lower()
    return user_input

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It's a tie!"
    elif (user_choice == 'rock' and computer_choice == 'scissors') or \
         (user_choice == 'paper' and computer_choice == 'rock') or \
         (user_choice == 'scissors' and computer_choice == 'paper'):
        return "You win!"
    else:
        return "You lose!"

def play_game():
    print("Welcome to Rock-Paper-Scissors!")
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    
    print(f"You chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")
    
    result = determine_winner(user_choice, computer_choice)
    print(result)

if __name__ == "__main__":
    play_game()
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Inspired by classic games and programming challenges.
