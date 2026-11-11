# Boom Deck

Draw a card. Pray it isn't a Boom. A multiplayer starter game from [Multiplayer Agent](https://multiplayeragent.com): 2D, turn-based, 2–6 players, with bots that fill empty seats.

![Boom Deck](poster.jpg)

## How it plays

Play action cards, then draw one to end your turn. Draw a Boom and you're out, unless you have a Defuse: then you secretly slip the Boom back into the deck. Peek, Skip, Attack, Shuffle and Steal to dodge it. Last one standing wins.

**Controls:** Click or tap a card to play it, tap the deck to draw.

## Make it yours in the Game Builder

Open the [Game Builder](https://multiplayeragent.com), choose **Start from a starter game** and pick Boom Deck. It opens as version 1 in your studio, ready to play and publish. Then ask for changes, for example:

- Add a Reverse card that changes the turn order
- Put two Booms in the deck for every player
- Make it a pirate ship with powder kegs instead of bombs

## Run it yourself

1. Get a free publishable key (`pk_…`) at [multiplayeragent.com](https://multiplayeragent.com).
2. In `index.html`, put it in place of `pk_REPLACE_ME` in the `MP_CONNECT` block.
3. Open `index.html` in a browser. No build step and no server needed.

Without a key it still runs, offline against bots.

## How it is built

- One `index.html`. The comment at the top of the script maps the code and explains the multiplayer.
- **Hidden info:** Your hand, your peeks and where you hide a Boom are sealed so only you can read them (the host deals, so it can too).
- **Host-run rules:** The host's browser shuffles, deals and checks every card; if it leaves, the next player takes over.
- **Bots:** Bots fill empty seats, peek, steal and dodge, and take over for anyone who leaves.
- **Leaderboard:** Games won, shown after every game.
- `?attract` runs it offline with bots only. The preview video is recorded from it.

## License

MIT.
