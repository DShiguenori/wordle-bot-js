# Dicord BOT

- [Link](https://discord.com/api/oauth2/authorize?client_id=954817412304343131&permissions=0&scope=bot%20applications.commands) for invitation

---

## How to play

The user just have to paste and send in the channel the auto-generated wordle sharing feature.
The bot will read the message and add his input to the database and recalculate his rank.

The user's rank will be enabled when he plays at least 5 games.

---

## Commands

| Command    | Description                                                     |
| ---------- | --------------------------------------------------------------- |
| help       | Shows the commands and how the ranking is built                 |
| rank       | Show the user's current general rank and the total of players   |
| percentual | Show the user's current rank based in percentual                |
| streak     | Show the user's current rank based in curretn streak            |
| maxstreak  | Show the user's current rank based in the max streak            |
| status     | Show only to the user his status on all the games he's playing. |

---

### Status examples:

| Wordle | 6      | 88%   | 2              | 2          |
| ------ | ------ | ----- | -------------- | ---------- |
|        | played | Win % | Current streak | Max streak |

| Termo | 4     | 100%        | 4               | 4                |
| ----- | ----- | ----------- | --------------- | ---------------- |
|       | Jogos | de vitórias | sequência atual | melhor sequência |

| Quarteto | 5     | 88%         | 2               | 2                |
| -------- | ----- | ----------- | --------------- | ---------------- |
|          | Jogos | de vitórias | sequência atual | melhor sequência |

---

## How the rank is built

Each status have it' own weight as follow:

1. Win %
2. Current Streak
3. Max Streak
4. Played games

If there's a draw in all the categories, the user that started to play first will be ranked on top.
The user will be ranked when at least 5 games have been submitted .

---

## Future Ideas

- ### Reverse enginering the answer

The BOT will know the day's word. Based in the user's input, we can try to reverse engineer the answer and submit an ephemeral response with a guess on what the user submitted in his game.

Sometimes this won't be possible (if the word the user submitted has no matching letters). But it's a fun idea to build.

- ### Expand the bot for other similar word games, in other languages or clones.

Like termo and palavradodia in portugues.
The idea is that the bot will know that there's more than one game being played and can build a general ranking with all the games and a game-specific ranking.

We can add a command for the specific game's rank.

- ### Anti-Cheat mechanism

Since the user can paste whatever he wants, there's not a certified way to check if the user is legit or if he's trolling. The bot can emit some alerts for the admins if the user is guessing correctly too much in his first/second tryes, or if he's too quick to submmit an answer.

The game is succetible to cheating, that's it's nature, so try to play with people you know and you can trust. It's just for fun, after all, don't use this ranking as a legit way to compete against other peple.
