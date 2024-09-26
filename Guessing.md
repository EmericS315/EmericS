```mermaid
flowchart TD
    Start([Start]) --> Generate[("Pick a number (1 to 100)")]
    Generate --> Guess[("Ask for your guess")]
    Guess --> Validate[("Check if valid")]
    
    Validate -->|Valid| Compare[("Check if correct")]
    Validate -->|Invalid| Error[("Show error, ask again")]
    Error --> Guess
    
    Compare -->|Correct| Win[("You got it! You win!")]
    Compare -->|Too High| High[("Too high! Try again.")]
    Compare -->|Too Low| Low[("Too low! Try again.")]
    
    High --> Guess
    Low --> Guess
    Win --> End([End])


Start: The game starts.
Pick a random number (1 to 100): The computer chooses a number between 1 and 100.
Ask for your guess: The user is asked to enter their guess.
Check if the guess is valid: The program checks if the input is a valid number.
Valid: If it is valid, move to check the guess.
Invalid: If not, show an error message and ask for a new guess.
See if the guess is correct: The program compares the guess with the random number.
Correct: Show a message that they won.
Too High: Inform the user that their guess was too high.
Too Low: Inform the user that their guess was too low.
