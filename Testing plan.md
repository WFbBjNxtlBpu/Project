Testing Plan — 

1\. Overview

This google doc will cover user stories and their acceptance criteria as well as test boundaries.

\---

2\. User Stories and Acceptance Criteria

User Story 1: As a player that already played the game, I want to skip the tutorial, so that I can get to the main game.

\- Acceptance Criterion 1 

    \- Requirement(s): The player can skip the tutorial section of the game

    \- Purpose:  It allows players to get through the part when they already know how to play the game.

    \- Test Case: 

        a) Feature: Skip tutorial feature

        b) Test: If the tutorial skip feature works

        c) Expected Result / Behavior: Upon stepping on a skip tutorial teleporter, you skip to the end.

        d) Automation Candidate: Repetitive tests

User Story 2: As a big fan of the lore, I want a panel in the title screen, so that I can read over some and recall the lore that is accessible to you when you complete a section of the game.

\- Acceptance Criterion 1 

    \- Requirement(s): The player can access a lore encyclopedia.

    \- Purpose: Acts as a diary for the player so players can look back on the lore they found.

    \- Test Case:

        a) Feature: Lore encyclopedia in the menu.

        b) Test: If the lore cyclopedia stores and saves the information.

        c) Expected Result / Behavior: Upon finding a “scrap” or piece of lore, the lore cyclopedia stores the information.

        d) Automation Candidate: Rule-based

User Story 3: As a speedrunner, I want a timer that tracks how long a run has been, so that I can see how much time I have finished a game in.

\- Acceptance Criterion 1 

    \- Requirement(s): The player can turn on a setting that says timer.

    \- Purpose: Adds a timer for a specific group of players.

    \- Test Case:

        a) Feature: Speedrun timer

        b) Test: If the timer counts up.

        c) Expected Result / Behavior: The timer starts counting up upon the player reaching the end of the tutorial.

        d) Automation Candidate: Repetitive tests  
\---

3\. Boundary and Edge Testing

Boundary / Edge 1:  Collision

    \- Requirement(s): The game has to check if the player is going to make contact with an object.

    \- Purpose: To prevent the player from phasing through an obstacle.

    \- Test Case 1:

        a) Upper Boundary: The wall that is the farthest possible wall the player can reach.

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player stops where the wall is.

        d) Automation Candidate: Repetitive

    \- Test Case 2:

        a) Lower Boundary: The position the player is at.

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player will not move at all.

        d) Automation Candidate: Rule-based

Boundary / Edge 2: Health

    \- Requirement(s): The game has a health value

    \- Purpose: Changes the story of the game depending on the players health.

    \- Test Case 1:

        a) Upper Boundary: 100 hp

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player's hp stops at 100\.

        d) Automation Candidate: Rule based

    \- Test Case 2:

        a) Lower Boundary: 0 hp

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player's hp stops at 0\.

        d) Automation Candidate: Rule based

Boundary / Edge 3: Temperature

    \- Requirement(s): The player has a temperature value that checks which temperature the player is at.

    \- Purpose: Changes the story of the game depending on the player's health.

    \- Test Case 1:

        a) Upper Boundary: 200

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player's temperature stops at 200\.

        d) Automation Candidate: Rule based

    \- Test Case 2:

        a) Lower Boundary: \-50

        b) Testing data used: \< x \- 1 , x, x \+ 1 \>

        c) Expected Result / Behavior: The player’s temperature stops at 0\.

        d) Automation Candidate: Rule-based

\---

4\. Automated Test List

Repetitive

- Tutorial skip  
- Speedrun timer  
- Collision upper boundary

  Rule-based

- Lore encyclopedia  
- Collision lower boundary  
- Health upper boundary  
- Health lower boundary  
- Temperature lower boundary  
- Temperature upper boundary

