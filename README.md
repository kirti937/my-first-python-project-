import random 

def guess_game():
    number = random.randint(1,10)
    guess = None
    attempts = 0

    print("I'm thinking of a number between 1 and 10.")

    while guess != number:
        try:
            guess = int(input("Enter your guess:"))
            attempts += 1
            if guess < number:
                print("Too low!")
            elif guess > number:
                print("Too high!")
            else:
                print(f"Correct ! You guessed it in {attempts} tries")
        except ValueError:
            print("Please enter a valid number .")

if __name__ == "__main__":
    guess_game()
