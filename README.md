# 2021-advent-of-BASIC

Join [Advent of Code](https://adventofcode.com/), complete a puzzle every day in the language of your choice.

I'll be doing it in BBC BASIC - a coding language from a computer called the [BBC Micro](https://en.wikipedia.org/wiki/BBC_Micro) first released in 1981. Just like me.

Solution code is provided per day, and you can explore each at [bbcmic.ro](https://bbcmic.ro/) - just copy it in to the editor, and press `run`.

## Notes

**Day 3** was the first where the data was too large to operate on in an array. (Well, I could store the data but I couldn't then copy it into an array for random access. I was forced to use it sequentially only.) The workaround: iterating over the input data to build a matching prefix that eventually became the solution.

**Day 4** also bumped against several limits of the poor little machine. I had a lot of data, and not enough room to track all the highlighted numbers after each call. I had to get creative, and ended up modifying the cards to remove numbers as they were highlighted.

* Silly mistake: As the scoring works by summing all _non-highlighted_ numbers, I figured I could just zero highlighted numbers - which makes it possible to spot a complete row or column, and very easy to calculate the score of a card. However, 0 is a legitimate number for a board. I had to switch to using -1. (There's no NULL in BBC BASIC.)
* Silly mistake: I was waiting for a board to have a row AND a column. Should have been OR.
* Silly mistake: Bingo cards can only win once! 
