# Python-animal-quiz-game

import random

# List of animal names
animals = ['lion', 'tiger', 'bear', 'wolf', 'panda']

# Randomly choose an animal from the list
answer = random.choice(animals)

# Obfuscate the animal name by replacing characters with underscores
obfuscated_answer = ['_' for _ in answer]

# Number of tries the user has
tries = 5

while tries > 0:
    print("Current status: ", "".join(obfuscated_answer))
    guess = input("Guess the animal name: ")

    if guess == answer:
        print("Congratulations! You guessed the correct animal.")
        break
    else:
        print("Sorry, that is incorrect. Try again.")
        tries -= 1

if tries == 0:
    print("You have run out of tries. The correct answer was:", answer)
