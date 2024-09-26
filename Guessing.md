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
