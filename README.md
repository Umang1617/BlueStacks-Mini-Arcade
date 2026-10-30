# BlueStacks MINI Arcade: design preview site

A linked, clickable design preview of the MINI Arcade. Plain HTML, CSS and JavaScript. No build step, no dependencies. Fonts load from Google Fonts (Lilita One, Rubik).

## Run it
Keep every file in this folder together, then open `index.html` in a browser (or serve the folder with any static server, for example `python3 -m http.server`).

## Pages and flow
| File | Page |
|---|---|
| `index.html` | Landing: register or log in, claw machine |
| `avatar.html` | Avatar select: pick a mascot (Pixel, Giga, Ping, Twix) |
| `lobby.html` | Lobby: today's five games, daily shuffle from a pool of 30 |
| `game.html#<id>` | Game page: intro, countdown, play, game over (30 games) |
| `leaderboard.html` | Weekly leaderboard with a tab per game |
| `profile.html` | Player settings, mascot, country, score history |
| `nav.js` | Links the pages together and remembers username and mascot |

Flow: landing → avatar select → lobby → game → leaderboard / profile. Register goes to avatar select; log in goes to the lobby. The header (logo, trophy, settings), Back buttons and footer links work on every page.

## Assets
- `av/` 24 mascot images (webp)
- `icons/` 30 game icons (svg)

## Game ids
runner, jump, flappy, snake, memory, bubble, color, pattern, puzzle, shooter, typer, number, reflex, whack, merge, word, stack, drift, brick, lane, beats, piano, gravity, bowling, slice, oddout, balloon, timing, sort, coin.
Open a game directly with `game.html#word`.

## Controls
- Most games: tap or click. Space, arrow keys and A/D also work where noted on the game's intro screen.
- Drift Racer: A / D or ← → to steer (tap left or right half on phones).
- Nitro Word: type or use the on-screen keyboard. Three hints, 30 points each.

## What is preview only
- Sign-up and login do not create real accounts.
- Scores, ranks, player names and score history are sample data.
- Nitro Word accepts any 5 letters (no dictionary check).
- Discord and Help links show a message instead of opening.
- Username and mascot are saved only in the visitor's own browser (localStorage).

## Applying to the live site
This is a design reference, not the production code. Rebuild the layout, colours and behaviour in the live Lovable project (bluestacks-mini-arcade.lovable.app) and connect real auth, scores and leaderboard data there.
