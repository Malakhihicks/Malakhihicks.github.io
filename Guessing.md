# Random Number Guessing Game

```mermaid
flowchart TD
  Start([Start]) --> Generate[Generate a random number between 1 and 100]
  Generate --> Prompt[Prompt user to guess the number]
  Prompt --> Input[User inputs a guess]
  Input --> CheckValid{Is the input a valid number?}
  CheckValid -- Yes --> Compare{Is guess correct?}
  CheckValid -- No --> Invalid[Show error: Please enter a number]
  Invalid --> Prompt
  Compare -- Yes --> Win[Display: You guessed the number correctly!]
  Compare -- No --> HighLow{Is the guess too low or high?}
  HighLow -- Low --> lowMsg[Display: Too low]
  HighLow -- High --> highMsg[Display: Too high]
  lowMsg --> Prompt
  highMsg --> Prompt
  Win --> End([End])
