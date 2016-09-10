# Dictionary Races and Search Algorithms

Today, I'm going to teach you a game that I played when I was in the third
grade. Then I'm going to relate it to computer science. And finally, we
will play the game as teams, and the winning team will get the grand prize.

The game is called Dictionary Races. The object of the game is to be the
first to find a word that is chosen at random from the dictionary.

Here are the rules:

1. Dictionaries start closed, on the table.
2. I (or your teacher, if you play this game again) open my dictionary to a
   random page, choose a word, and say it out loud.
3. Once we've verified everyone knows the word, I will say "Ready? Go!"
   and the players find the word as quickly as possible. When you find the 
   word, raise your hand, and say "got it", or the equivalent, to get my 
   attention.
4. When you're called on, say the word, say the page number that the word is 
   on, spell the word, and read the first definition. If you are correct, you 
   get a point. If you are incorrect, play resumes, and the next person to 
   raise their hand gets a chance.
5. Once the correct word and definition are found, dictionaries are closed,
   and we play again.

Shall we give it a try?

* Play a few rounds.

* Ask one or more winning students what they did to find the word so quickly.

The process you follow to find the word in the dictionary is called an 
algorithm. More specifically, a search algorithm. One of the things computer
scientists do is design algorithms to do things (like search) as quickly as 
possible.

For example, suppose I was searching for a specific card in a deck. To make
things easier, let's limit ourselves to cards of the same suit, so there's only
13 possiblities.

Dictionaries put the words in alphabetical order. A computer scientist would
say it's "sorted". We sort things to make them easier -- and faster -- to find.
So I'm going to sort my search decks Ace to King.

What is the fastest way to find a card? Let's compare two search algorithms: 
the linear search and the binary search.

A linear search is when you go sequentially through the deck searching for the
correct card.

A binary search divides the deck into two smaller decks, compares the value
of the middle card to the search value, then repeats the process with the
appropriate sub-deck until the search value is found.

Let's compare these two algorithms side-by-side. I'm going to shuffle a third 
deck to choose what I'm searching for, and we count how many cards we have to 
look at in each algorithm to find that card.

* Manually step through each algorithm (in parallel) for each search card.
  Record iterations in a table.

    search  linear      binary
    value   iterations  iterations
    ======  ==========  ==========
      A          1           4
      2          2           3
      3          3           4
      4          4           2
      5          5           3
      6          6           4
      7          7           1
      8          8           4
      9          9           3
     10         10           4
      J         11           2
      Q         12           3
      K         13           4

Which algorithm is better? For the best case, the linear search takes 1 check,
but so does the binary search. For the worst case, the linear search takes 13
checks, the binary search takes 4. On average, the linear search takes 7 checks. 
The binary search takes 3.

As your deck size grows, the linear search will take even longer compared to
the binary search, so clearly the binary search is better.

But what about unordered data?

The linear search will still work with unordered data. The binary search will
fall on its face, and won't be able to find what you're looking for a lot of
the time.

This is why dictionaries are ordered. It makes it possible to find the word
you're looking for.

Now, who wants to do more dictionary races?

To make it interesting, let's divide up into teams. One person per team will
play in each round, and we will switch players between rounds. The team with
the most words found will win the grand prize.

I'm not allowed to give actual prizes in these sessions, so the grand prize
is a hearty round of high fives.
