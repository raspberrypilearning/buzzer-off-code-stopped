Un utilisateur peut arrêter manuellement le code en cours d'exécution à l'aide de l'icône d'arrêt rouge dans Thonny. À ce stade, si un buzzer émet un son, le son continuera à jouer - cela peut être très ennuyeux !

Le code en surbrillance suivant utilise `try:` et `finally:` pour désactiver le buzzer lorsque le code est arrêté par un utilisateur :

--- code ---
---
language: python
filename: sound_machine.py
line_numbers: false
line_number_start: 1
line_highlights: 14, 18-19
---
RYTHME = 0.4

liten_mus = [ ['d5', RYTHME / 2], ['d#5', RYTHME / 2], ['f5', RYTHME], ['d6', RYTHME], ['a#5', RYTHME], ['d5', RYTHME],  
              ['f5', RYTHME], ['d#5', RYTHME], ['d#5', RYTHME], ['c5', RYTHME / 2],['d5', RYTHME / 2], ['d#5', RYTHME], 
              ['c6', RYTHME], ['a5', RYTHME], ['d5', RYTHME], ['g5', RYTHME], ['f5', RYTHME], ['f5', RYTHME], ['d5', RYTHME / 2],
              ['d#5', RYTHME / 2], ['f5', RYTHME], ['g5', RYTHME], ['a5', RYTHME], ['a#5', RYTHME], ['a5', RYTHME], ['g5', RYTHME],
              ['g5', RYTHME], ['', RYTHME / 2], ['a#5', RYTHME / 2], ['c6', RYTHME / 2], ['d6', RYTHME / 2], ['c6', RYTHME / 2],
              ['a#5', RYTHME / 2], ['a5', RYTHME / 2], ['g5', RYTHME / 2], ['a5', RYTHME / 2], ['a#5', RYTHME / 2], ['c6', RYTHME],
              ['f5', RYTHME], ['f5', RYTHME], ['f5', RYTHME / 2], ['d#5', RYTHME / 2], ['d5', RYTHME], ['f5', RYTHME], ['d6', RYTHME],
              ['d6', RYTHME / 2], ['c6', RYTHME / 2], ['b5', RYTHME], ['g5', RYTHME], ['g5', RYTHME], ['c6', RYTHME / 2],
              ['a#5', RYTHME / 2], ['a5', RYTHME], ['f5', RYTHME], ['d6', RYTHME], ['a5', RYTHME], ['a#5', RYTHME * 1.5] ]

try:
    for note in liten_mus:
        haut_parleur.play(note) 

finally:
    haut_parleur.off() # éteint le haut-parleur lorsque le code est arrêté par l'utilisateur

--- /code ---
