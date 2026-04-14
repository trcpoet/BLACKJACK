Blackjack — Python OOP
A fully playable command-line Blackjack game built with Python, demonstrating object-oriented programming design patterns.
What It Does
Simulates a complete game of Blackjack against a dealer. The player can hit or stand, bets chips, and the dealer plays by casino rules (hits until reaching 17+). Aces automatically adjust between 11 and 1 to avoid busting.
How to Run
bash# Clone the repo
git clone https://github.com/trcpoet/BLACKJACK.git
cd BLACKJACK

# Open in Jupyter
jupyter notebook BLACKJACK.ipynb

# Or run directly with Python
jupyter nbconvert --to script BLACKJACK.ipynb
python BLACKJACK.py
OOP Design
The project is structured around five classes that each own a specific responsibility:
Card — Represents a single playing card with suit and rank. The __str__ method returns a human-readable string like "King of Hearts".
Deck — Builds all 52 Card objects, shuffles them using Python's random module, and deals cards one at a time using pop().
Hand — Holds the cards dealt to a player or dealer. Tracks total value and automatically adjusts for Aces — if the hand exceeds 21 and contains an Ace, the Ace's value drops from 11 to 1.
Chips — Tracks the player's chip total and current bet. win_bet() and lose_bet() update the total after each round.
Game functions — take_bet(), hit(), hit_or_stand(), show_some(), show_all(), and outcome functions (player_busts, player_wins, dealer_busts, dealer_wins, push) handle the game loop logic cleanly outside the classes.
Game Rules Implemented

Standard 52-card deck, shuffled before each game
Dealer hits until reaching 17 or above (soft 17 rule)
Aces count as 11 or 1 — automatically adjusted to avoid busting
Player bet validated against available chips before each round
One dealer card hidden until the player stands
Player can replay after each hand

Python Concepts Demonstrated

Object-oriented programming: classes, __init__, __str__, instance methods
Exception handling with try/except for bet input validation
Global variable control for game state (playing)
List manipulation: append(), pop(), iteration
f-strings and string formatting
While loops with break/continue for game flow control

Related Projects:
WAR — Card game War implemented in Python OOP
blackjack-api — This game converted into a production FastAPI REST API with PostgreSQL persistence
