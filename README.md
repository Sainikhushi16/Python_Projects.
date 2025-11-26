# Snake-Water-Gun-Game-Code

import random

# Options
choices = ['snake', 'water', 'gun']

# Score initialization
user_score = 0
computer_score = 0

# Number of rounds
rounds = int(input("Kitne rounds khelna chahte ho? "))

for i in range(rounds):
    user_choice = input("Choose snake, water, or gun: ").lower()
    computer_choice = random.choice(choices)
    print(f"Computer chose: {computer_choice}")
    
    if user_choice == computer_choice:
        print("It's a tie!")
    elif (user_choice == 'snake' and computer_choice == 'water') or \
         (user_choice == 'water' and computer_choice == 'gun') or \
         (user_choice == 'gun' and computer_choice == 'snake'):
        print("You win this round!")
        user_score += 1
    else:
        print("Computer wins this round!")
        computer_score += 1

    print(f"Score -> You: {user_score}, Computer: {computer_score}\n")

# Final Result
if user_score > computer_score:
    print("Congratulations! You won the game 🥳")
elif user_score < computer_score:
    print("Computer won the game! 😢")
else:
    print("The game is a tie! 😎")
