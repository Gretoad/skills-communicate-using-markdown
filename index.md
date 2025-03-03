# Mushroom
###### sexy
![image](https://github.com/user-attachments/assets/4fac8c65-9372-474b-9e81-1582910bf5ff)
``` python
from random import randrange
from os import system
#WORDS=[...]
while True:
word = WORDS[randrange(len(WORDS) - 1)]
    trials: list = []
    mistakes: list = []
    playing = True
    system("clear")
    print("_ " * len(word))
    while playing:
        acc = ""
        attempt = ""
        while len(attempt) != 1 or attempt in trials:
            attempt = input("lettre: ").lower()
        system("clear")
        trials.append(attempt)
        for c in word:
            if c in trials:
                acc += c + " "
            else:
                acc += "_ "
        if not attempt in word:
            print(f"Pas de {attempt}.")
            mistakes.append(attempt)
        print(acc)
        print("\n" + ",".join(mistakes))
        if len(mistakes) == 10:
            input(f"Perduuu!!! Le mot à trouver était {word}")
            playing = False
        if not "_" in acc:
            input(f"Gagnééé!!! Le mot à trouver était bien {word}")
            playing = False

```
- [ ] Do all github tutorials
- [ ] Be less lazy
