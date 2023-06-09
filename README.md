### Tasks

## Hangman game

Implement the play(String word, int lives) function as a basic hangman game.

- The function uses the word parameter as the word to guess and the lives parameter as the number of available mistakes.
- The initial game state is displayed as _ _ _ _ _ _ _ _ (one underscore for each letter in word).
- The game state is displayed as _ o d _ _ o o _ if letters 'd' and 'o' are revealed.
- It is possible to make guesses, and letters that occur in the word are revealed.
- When a guessed letter does not occur in word, the player loses one life.
- When a guess is repeated (regardless of its occurrences), the player is notified, and nothing happens.
- When a guess is wrong (either a new or a repeated letter), the previous wrong letters are shown to the user.
- The player wins when all letters in word are revealed.
- The player loses when the number of wrong guesses is higher than the initial value of lives parameter (not counting repeated guesses).
- When the player types 'quit' as input, the program says good-bye and terminates.

## Case sensitivity

The gameplay is case insensitive, the word display is case sensitive.

- Both uppercase and lowercase letters are considered valid input.
- Uppercase and lowercase letter guesses reveal the same letters (e.g. both c and C guesses reveal all the cs in the word, regardless of their case).
- Letters of different cases behave as if they were the same when checking repetitions (e.g. entering c after a C would count as a repetition).
- On the displaying side, however, letters are revealed as they originally appear in word (e.g. successfully guessing c shows C _ _ _ c _ _ _ for Codecool).

## Graphics

Add ASCII art to visualize lives left.

- The game state display is accompanied by an ASCII art depending on the number of lives left.
- The art sequence is adapted to the starting value of the lives parameter (at least between 3 and 7) – this means that the game over art is always the same.

# Load words

The game uses a random word from a pre-defined word collection.

- The game randomly picks a word at each run.
- The game randomly picks a country from the returned array of Countries.getAll() function.

## Different levels

The program allows the user to play on different levels.

- The game starts with a menu for picking a difficulty level. The play() function is not changed.
- The word-pool and the number of lives depend on the chosen level.