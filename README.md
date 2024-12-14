# Rock Paper Scissors Game

## Overview
**Rock Paper Scissors Game** is a Java-based console application that brings the classic game to life. Players can compete against the computer in this simple yet engaging game, which leverages core Java concepts like conditionals, loops, and user input handling.

---

## Features
1. **Interactive Gameplay:**
   - Players can choose Rock, Paper, or Scissors and compete against the computer.

2. **Randomized Computer Moves:**
   - The computer's choice is generated randomly for unpredictability.

3. **Win/Lose/Draw Logic:**
   - Implements standard rules of Rock Paper Scissors to determine the winner.

4. **Replay Option:**
   - Players can choose to play multiple rounds.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Snippets](#code-snippets)
- [Contribution](#contribution)
- [License](#license)
- [Contact](#contact)

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/rock-paper-scissors-game.git
   ```
2. Navigate to the project directory:
   ```bash
   cd rock-paper-scissors-game
   ```
3. Compile the Java file:
   ```bash
   javac RockPaperScissors.java
   ```
4. Run the program:
   ```bash
   java RockPaperScissors
   ```

---

## Usage
1. Run the application.
2. Enter your choice (Rock, Paper, or Scissors).
3. The computer will make its choice.
4. View the result of the round (Win/Lose/Draw).
5. Choose to play again or exit the game.

---

## Code Snippets
### Java Example:
```java
import java.util.Random;
import java.util.Scanner;

public class RockPaperScissors {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        String[] options = {"Rock", "Paper", "Scissors"};

        while (true) {
            System.out.println("Enter your choice (Rock, Paper, Scissors): ");
            String userChoice = scanner.nextLine();

            if (!userChoice.equalsIgnoreCase("Rock") &&
                !userChoice.equalsIgnoreCase("Paper") &&
                !userChoice.equalsIgnoreCase("Scissors")) {
                System.out.println("Invalid choice. Try again.");
                continue;
            }

            int computerIndex = random.nextInt(3);
            String computerChoice = options[computerIndex];

            System.out.println("Computer chose: " + computerChoice);

            if (userChoice.equalsIgnoreCase(computerChoice)) {
                System.out.println("It's a draw!");
            } else if ((userChoice.equalsIgnoreCase("Rock") && computerChoice.equals("Scissors")) ||
                       (userChoice.equalsIgnoreCase("Paper") && computerChoice.equals("Rock")) ||
                       (userChoice.equalsIgnoreCase("Scissors") && computerChoice.equals("Paper"))) {
                System.out.println("You win!");
            } else {
                System.out.println("You lose!");
            }

            System.out.println("Do you want to play again? (yes/no): ");
            String playAgain = scanner.nextLine();
            if (!playAgain.equalsIgnoreCase("yes")) {
                break;
            }
        }

        System.out.println("Thank you for playing!");
    }
}
```

---

## Contribution
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add some feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/feature-name
   ```
5. Open a pull request.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Contact
**Author:** Sreerangam
- GitHub: https://github.com/your-username/Sreerangam17
- Email: sreemaha257@gmail.com

---

## Example README
This README provides an overview of the **Rock Paper Scissors Game** project, making it ready for posting in GitHub repositories. Customize it further as needed to align with specific repository requirements.

