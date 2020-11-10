# Deck of card
> Following a tutorial on NBdev.


## Install

```
## pip install nbdev_deck_of_cards
```

## How to use

Some code examples:

```
from nbdev_deck_of_cards.core import *
```

```
deck = Deck()
deck.shuffle()
```

```
deck
```




    <nbdev_deck_of_cards.core.Deck at 0x21d1c4f2e20>



```
print(deck)
```

    Queen of Hearts
    10 of Clubs
    9 of Spades
    10 of Spades
    6 of Clubs
    9 of Hearts
    8 of Spades
    Jack of Spades
    6 of Spades
    King of Hearts
    Queen of Spades
    Jack of Hearts
    6 of Hearts
    King of Spades
    7 of Clubs
    8 of Hearts
    3 of Diamonds
    2 of Diamonds
    6 of Diamonds
    4 of Diamonds
    5 of Hearts
    3 of Hearts
    Ace of Clubs
    Jack of Diamonds
    7 of Diamonds
    Ace of Spades
    8 of Diamonds
    2 of Clubs
    5 of Clubs
    10 of Diamonds
    10 of Hearts
    3 of Clubs
    Jack of Clubs
    King of Diamonds
    8 of Clubs
    9 of Diamonds
    4 of Clubs
    7 of Spades
    4 of Spades
    Queen of Clubs
    Ace of Hearts
    2 of Spades
    King of Clubs
    7 of Hearts
    Ace of Diamonds
    5 of Diamonds
    2 of Hearts
    4 of Hearts
    9 of Clubs
    3 of Spades
    5 of Spades
    Queen of Diamonds
    

```
len(deck)
```




    52



```
# Create one hand
hand = Hand()
```

```
# Deal 5 cards from deck
deck.move_cards(hand, 5)
hand.sort()
print(hand)

```

    9 of Clubs
    Queen of Diamonds
    4 of Hearts
    3 of Spades
    5 of Spades
    

```
len(deck)
```




    47



## Tests

```
c1 = Card(suit=2, rank=3)
assert str(c1) == '3 of Hearts'
```

```
c2 = Card(suit=1, rank=13)
assert(str(c2) == 'King of Diamonds')
```

```
c3 = Card(suit=1, rank=12)
assert(str(c3) == 'Queen of Diamonds')
```

```
assert c1 > c2
```

```
assert c3 < c2
```
