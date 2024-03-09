class hangman():
  def core(self):
    guesses = 0
    letter_used = ""
    word = "codingclass"
    progress = ("?", "?", "?", "?", "?", "?", "?", "?", "?", "?", "?", "?")

    while guesses < 7:
      guess = input("Guess a letter: ")
      if guess in word and not in letter_used:
        print(guess, "is in the word")
        letter_used += guess
        self.hangman_graphic(guesses)
        print ("profress: ")+ self.progress_updater(guess, word, progress)
        print ("Letters used: ") + letter_used
      elif guess not in word and not (in letter_used):
