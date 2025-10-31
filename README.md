-----

# 🐄 Bulls and Cows 🐂

A classic number guessing and code-breaking game, also known as **4-Digit Mastermind**, implemented as a simple Python console application.

-----

## 📝 Overview

**Bulls and Cows** is a game of logic and deduction where the player attempts to guess a secret 4-digit number.

The game generates a **4-digit secret number** where **all digits are unique**. After each guess, the player receives feedback in the form of **Cows** and **Bulls**:

  * **🐂 Bulls:** The number of digits in the guess that are **correct** and in the **correct position**.
  * **🐄 Cows:** The number of digits in the guess that are **correct** but in the **wrong position**.

The goal is to guess the number with the fewest attempts\!

-----

## 🚀 Getting Started

### Prerequisites

You only need **Python 3** installed on your system.

### Installation and Running

This project consists of a single file, `cows_and_bulls_game.py`.

1.  **Clone the repository** (or simply download the file):

    ```bash
    git clone https://github.com/AHG03/Bulls-and-Cows-Python.git
    cd Bulls-and-Cows-Python
    ```

2.  **Run the game** from your terminal:

    ```bash
    python cows_and_bulls_game.py
    ```

-----

## 🎮 How to Play

The game will prompt you to enter your guess.

### Guess Rules

Your guess **must** meet the following criteria:

  * It must be exactly **4 digits** long.
  * It must contain **only numbers** (`0-9`).
  * **All four digits must be unique** (e.g., `1234` is valid, but `1123` is not).

### Example Gameplay

When you run the script, you'll see a prompt:

```
Guess: 1478
1 cows, 1 bulls.
Guess: 9876
0 cows, 2 bulls.
Guess: 5063
4 cows, 0 bulls.
Guess: 3605
4 cows, 4 bulls.
Congratulations, you guessed the correct number!
```

-----

## 🧠 Game Logic Explained

The core logic is contained in two simple functions:

  * `generate_secret()`: Uses the `random.shuffle` function to create a random, 4-digit number with guaranteed unique digits.
  * `calculate_cows_and_bulls(secret, guess)`:
      * **Bulls** are calculated first by comparing digits at the exact same index.
      * **Cows** are calculated by finding all correct digits within the secret and then subtracting the count of **Bulls**.

-----
