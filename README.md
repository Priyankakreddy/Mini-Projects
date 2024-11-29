#number guessing
import random
#generate a random number between 1 to 100
def number_guessing_game():
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guess = None
    print("Welcome to number guessing game")
    print("I have selected a number between 1 to 100, try to guess it")

  while guess != number_to_guess:
        try:
            #get user input
            guess = int(input("Enter your guess: "))
            attempts += 1

            #check the guess
  if guess < number_to_guess:
                print("Too low! try again")
            elif guess > number_to_guess:
                print("Too high! Try again")  
            else:
                print("Congratulations! You have guessed the number {number_to_guess} in {attempts} attempts") 
        except ValueError:
            print("Invalid Input. Please input a number")         


#Run the game
number_guessing_game()
