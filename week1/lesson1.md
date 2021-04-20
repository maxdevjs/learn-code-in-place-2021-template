# Lesson 1 Welcome to Karel April 19th

<details open>
<summary>Learning Goals</summary>
<br />

By the end of class you should know about Code in Place. You should also know basic Karel commands. The Karel material is review from the concepts that you used in the application -- this gives you a chance to get used to the course structure in a gentle way. Learn about the art of writing beautiful programs.
</details>


 ## Videos

- [x] Welcome
- [x] About Code in Place
- [x] Meet Karel

## Assignments Problems

<details>
<summary>Q1: Jigsaw Puzzle Karel</summary>
<details open>
<summary>Description</summary>
During quarantine, Karel has picked up a new hobby: doing puzzles! Karel is almost done with the square puzzle represented by the 4x4 grid of beepers shown below:

<br />
<img img width="600px" src="https://static.us.edusercontent.com/files/NBulki5rUJribfbNf9ScnoFp" />
<br />

The beeper in the bottom most row represents the last piece of the puzzle! Write a program which will get Karel to pick up the last piece, put it in place, and move Karel back to the bottom left corner of the world facing East so she can admire the completed puzzle. Here's what your end result should look like:

<br />
<img img width="600px" src="https://static.us.edusercontent.com/files/KjPIYmUMTfMPW0G2BO6k6jbb" />
<br />

To reiterate, you should write the sequence of commands so that Karel will:

- Move to and pick up the last puzzle piece (the beeper in row 1, column 3)

- Put the puzzle piece in place (row 3, column 4)

- Return Karel to her initial position

Although the program does not have many lines of code, it is still worth getting some practice with decomposition. In your solution, include a function for each of the three steps shown in the outline above.
</details>
<details>
<summary>Code</summary>

`PuzzleKarel.py`
```python
from karel.stanfordkarel import *

"""
File: PuzzleKarel.py
--------------------
Karel should finish the puzzle by picking up the last beeper (puzzle piece) and placing it in the right spot.
Karel should end in the same position Karel starts in -- the bottom left corner of the world.
"""

def main():
    """
    You should write your code to make Karel do its task in
    this function. Make sure to delete the 'pass' line before
    starting to write your own code. You should also delete this
    comment and replace it with a better, more descriptive one.
    """
    pass

if __name__ == '__main__':
    run_karel_program('Puzzle.w')
```

`Puzzle.w`
```yaml
Dimension: (7, 7)
Wall: (3, 2); north
Wall: (6, 4); east
Wall: (5, 3); south
Wall: (2, 6); east
Wall: (6, 5); east
Wall: (6, 6); east
Wall: (6, 7); south
Wall: (3, 3); west
Wall: (2, 4); east
Wall: (6, 3); south
Wall: (2, 5); east
Wall: (5, 7); south
Wall: (6, 3); east
Wall: (4, 6); north
Wall: (3, 6); north
Beeper: (4, 3); 0
Beeper: (5, 3); 1
Beeper: (6, 3); 1
Beeper: (6, 4); 1
Beeper: (5, 4); 1
Beeper: (5, 5); 1
Beeper: (6, 5); 1
Beeper: (6, 6); 1
Beeper: (5, 6); 1
Beeper: (4, 6); 1
Beeper: (3, 6); 1
Beeper: (3, 5); 1
Beeper: (4, 5); 1
Beeper: (4, 4); 1
Beeper: (3, 4); 1
Beeper: (3, 1); 1
Beeper: (3, 3); 1
Beeper: (3, 2); 0
Beeper: (2, 2); 0
Beeper: (2, 3); 0
Beeper: (2, 4); 0
Beeper: (2, 5); 0
Beeper: (2, 6); 0
Karel: (1, 1); east
BeeperBag: 0
```
</details>
</details>

<hr />
<details>
<summary>Q2: Year 2021</summary>
<details open>
<summary>Description</summary>
Congratulations on beginning your coding journey! Karel welcomes you to Code in Place 2021. Your next task is to help Karel celebrate the occasion by placing 20 beepers, moving Karel one step, placing 21 beepers, and moving Karel one more step. The world should ultimately look like this:

<br />
<img width="600px" src="https://static.us.edusercontent.com/files/1I5dc3wVCM4UfOyajbk9cexw" />
<br />

Happy coding!
</details>
<details>
<summary>Code</summary>

`2021.py`
```python
from karel.stanfordkarel import *

"""
File: 2021.py
--------------------
When you finish writing this file, Karel should be able to place 20 beepers,
then 21 beepers, and end facing East to the right of the 21 beepers.
"""

def main():
    """
    You should write your code to make Karel do its task in
    this function. Make sure to delete the 'pass' line before
    starting to write your own code. You should also delete this
    comment and replace it with a better, more descriptive one.
    """
    pass

if __name__ == '__main__':
    run_karel_program('3x3.w')
```

`3x3.w`
```yaml
Dimension: (3, 3)
Karel: (1, 1); east
BeeperBag: INFINITY
```
</details>
</details>

<hr />

<details>
<summary>Q3: Cleanup Karel, Milestone 1</summary>

<details open>
<summary>Description</summary>
Your next task is to execute a "safe pickup" -- Karel can pick up beepers, but not if none are present! Write a program which will check if a beeper is present at the position Karel is currently on and pick up a beeper if one is present (if there are no beepers present, Karel shouldn't do anything).

Two worlds are provided for your to test your code on -- on the world where Karel starts on a beeper, your code should get Karel to pick the beeper up. On the world where Karel stREADMEarts on a blank spot, your code shouldn't do anything.

We've provided you two 1x1 worlds (one with a beeper, one without) on which to test your code. You can toggle from the beeper-present world to the no-beeper world by changing the very last line in the file from run_karel_program('SafePickup1.w') to run_karel_program('SafePickup2.w') (and vice versa).
</details>
<details>
<summary>Code</summary>

`SafePickup1.py`
```python
from karel.stanfordkarel import *

"""
File: SafePickup.py
--------------------
When you finish writing this file, Karel should be able to
pick up a beeper from the current position if one is present
(but do nothing if no beepers are present).
"""

def main():
    """
    You should write your code to make Karel do its task in
    this function. Make sure to delete the 'pass' line before
    starting to write your own code. You should also delete this
    comment and replace it with a better, more descriptive one.
    """
    pass

if __name__ == '__main__':
    run_karel_program('SafePickup1.w')
```

`SafePickup1.w`
```yaml
Dimension: (1, 1)
BeeperBag: INFINITY
Beeper: (1,1); 1
Karel: (1, 1); East
Speed: 0.75
```

`SafePickup2.w`
```yaml
Dimension: (1, 1)
BeeperBag: INFINITY
Karel: (1, 1); East
Speed: 0.75
```
</details>
</details>

<hr />
<details>
<summary>Extension (optional!)</summary>
<details open>
<summary>Description</summary>
If you finish early, you may optionally write a Karel project of your own choice. Modify this file to use Karel to complete any task of your choosing! Extensions are a great chance for practice and to be creative. Make sure to write comments to explain what your program is doing and update the world to be appropriate for your program. (Notice that you can toggle the rows and columns of Karel's world, and if you right click Karel's world, you'll see a dropdown of other things you can do by clicking!)
</details>
<details>
<summary>Code</summary>

`ExtensionKarel.py`
```python
from karel.stanfordkarel import *

"""
File: ExtensionKarel.py
-----------------------
This file is for optional extension programs.
"""

def main():
    """
    You should write your code to make Karel do its task in
    this function. Make sure to delete the 'pass' line before
    starting to write your own code. You should also delete this
    comment and replace it with a better, more descriptive one.
    """
    pass

def turn_right():
   turn_left()
   turn_left()
   turn_left()

def crazy_swing():
    while no_beepers_present():
        if front_is_clear():
            move()
            turn_right()
            if front_is_clear():
                move()
            turn_left()
            if front_is_clear():
                move()
        else:
            turn_left()
            turn_left()
            turn_right()

if __name__ == "__main__":
    run_karel_program()
```

</details>
</details>
<hr />

## Optonal Related Reading

- [ ] [Intro to Karel](https://compedu.stanford.edu/karel-reader/docs/python/en/chapter1.html)
- [ ] [Programming Karel](https://compedu.stanford.edu/karel-reader/docs/python/en/chapter2.html)
- [ ] [New Functions](https://compedu.stanford.edu/karel-reader/docs/python/en/chapter3.html)
- [ ] [Decomposition](https://compedu.stanford.edu/karel-reader/docs/python/en/chapter4.html)
