Logic point A: Collision

| Boundary input | Why it’s a boundary |
| :---- | :---- |
| Lowest possible input: Where the player is at. | It’s the lowest boundary point because it’s where the player is at before they move. |
| Highest possible input: The wall that is the farthest possible wall they can reach. | The game calculates which wall they are heading toward so the game can prevent the player from no-clipping. |
| Unexpected or incorrect input: The player somehow got no-clipped. | The player might start flying through the walls of the game without stopping.  |

Logic point B: Health

| Boundary input | Why it’s a boundary |
| :---- | :---- |
| Lowest possible input: Zero | To prevent the player’s health going into the negatives. |
| Highest possible input: One hundred | To prevent the player from going above the threshold. |
| Unexpected or incorrect input: The player has less health than the game is supposed to. | It has the possibility of not letting the player progress. |

Logic point C: Temperature

| Boundary input | Why it’s a boundary |
| :---- | :---- |
| Lowest possible input: Zero | To prevent the player’s health going into the negatives. |
| Highest possible input: One hundred | To prevent the player from going above the threshold. |
| Unexpected or incorrect input: The player has more or less temperature than the game is supposed to allow you. | It has the possibility of not letting the player progress. |

| Boundary input | Test data | Expected outcome |
| :---- | :---- | :---- |
| If the player hits a wall. | The player begins to no-clip through the wall | The player will stop at where they hit a wall. |
| The player's health goes below zero. | The player's health is below 0\. | The game will cap their health at that exact amount. |
| The player’s temperature goes below \-50 or above 200\. | The player's temperature is either \-51 or 201\. | The game will cap their temperature at that exact amount. |

“Which logic point feels the most fragile?”  
“What will I need to watch out for when coding player collision?”  
“Which boundary case surprised me?”: