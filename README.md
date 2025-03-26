# Code of Rock Paper Scissor game
import random
def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])
def determine_winner(player, computer):
    if player==computer:
      return "It's a Tie!"
    elif (player=='rock' and computer=='scissors') or \
         (player=='paper' and computer=='rock') or \
         (player=='scissors' and computer=='paper'):
         return "You Win!"
    else:
        return "Computer Wins!"
def main():
    print("Welcome to Rock, Paper, Scissors!")
    while True:
        player_choice= input("Enter rock, paper, scissors (or 'quit' to exit): ").lower()
        if player_choice=='quit':
            print("Thanks for playing!")
            break
        elif player_choice not in ['rock', 'paper', 'scissors']:
            print("Invalid choice. Try again.")
            continue
        computer_choice=get_computer_choice()
        print(f"Computer chose: {computer_choice}")
        result= determine_winner(player_choice, computer_choice)
        print(result)
        print("----------------------")
if __name__ == "__main__":
    main()
