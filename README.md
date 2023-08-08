
# Wordle

This is a program that behaves similarly to the popular [Wordle](https://www.nytimes.com/games/wordle/index.html) daily word game.
## Background

Odds are, if you’re a Facebook user, at least one of your friends posted something looking like this, particularly back in early 2022 when it was all the rage:

![Wordle results](https://cs50.harvard.edu/x/2023/psets/2/wordle50/wordle.png)

If so, your friend has played Wordle, and are sharing their results for that day! Each day, a new “secret word” is chosen (the same for everyone) and the object is to guess what the secret word is within six tries. Fortunately, given that there are more than six five-letter words in the English language, you may get some clues along the way, and the image above actually shows your friend’s progression through their guesses, using those clues to try to home in on the correct word. Using a scheme similar to the game Mastermind, if after you guess that letter turns green, it means not only is that letter in the secret word that day, but it is also in the correct position. If it turns yellow, it means that the letter guessed appears somewhere in the word, but not in that spot. Letters that turn gray aren’t in the word at all and can be omitted from future guesses.

This is a program called wordle that enables us to recreate this game and play it in our terminal instead. We’ll use red text instead of gray to indicate letters that aren’t in the word at all. At the time the user executes the program, they should decide, by providing a command-line argument, what the length of the word they want to guess is, between 5 and 8 letters.

## Examples

```javascript
$ ./wordle
Usage: ./wordle wordsize
```

```javascript
$ ./wordle 4
Error: wordsize must be either 5, 6, 7, or 8
```

```javascript
$ ./wordle 5
This is WORDLE50
You have 6 tries to guess the 5-letter word I'm thinking of
Input a 5-letter word: crash
Guess 1: crash
Input a 5-letter word: scone
Guess 2: scone
Input a 5-letter word: since
Guess 3: since
You won!
```

