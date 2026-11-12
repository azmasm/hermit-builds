# Hermit builds

azmasm's own builds of Nintendo Switch 2 games for the Mac, used by [Hermit](https://github.com/azmasm/hermit), the Mac app that turns your own game dump into a native Mac game. **To play, get Hermit**: it fetches the right build for your game and your Mac by itself. This repository is for people who want to read or change the code.

These builds used to live in a repository called `switch2mac-engine`, then `hermit-engine`.

## The builds

Each build is a full copy of the engine with the changes its game needs, kept on **its own branch**. The folders in [`builds/`](builds) describe them:

| Game | Folder | Its code | In Hermit |
|---|---|---|---|
| Mario Kart World 1.0.0 | [`builds/mario-kart-world`](builds/mario-kart-world) | branch [`switch2mac`](https://github.com/azmasm/hermit-builds/tree/switch2mac) | "azmasm's build", recommended on M1 and M2 Macs with 24 GB or more |
| The Legend of Zelda: Ocarina of Time (Switch 2) | [`builds/the-legend-of-zelda-ocarina-of-time`](builds/the-legend-of-zelda-ocarina-of-time) | branch [`ocarina`](https://github.com/azmasm/hermit-builds/tree/ocarina) | "azmasm's build", recommended on M1 and M2 Macs with 32 GB or more |

Why branches and not folders of code: each build is the whole of [nxnative](https://github.com/seedds/nxnative) (thousands of files) at a different point, with the changes its game needs. Kept as branches, each one can still take nxnative's fixes as they come, and Hermit pins each game to one exact commit of its branch. nxnative's own code, unchanged and kept up to date, is in azmasm's fork: [azmasm/nxnative](https://github.com/azmasm/nxnative).

## Adding a build

1. Start a new branch from nxnative's newest code ([azmasm/nxnative](https://github.com/azmasm/nxnative), branch `main`) and name it after the game.
2. Make the game's changes on that branch and push it here.
3. Add a folder for it in [`builds/`](builds) on this branch, with a page like the others.
4. In Hermit, add the build to the game's `game.json` with this repository, the branch's name and the commit to use. Hermit's update bot follows the branch from then on.

## What is not here

No game, no game file, no key and no Nintendo artwork: you bring your own dump of a game you own ([Hermit's LEGAL.md](https://github.com/azmasm/hermit/blob/main/LEGAL.md)).

## Licence and credit

MIT ([LICENSE](LICENSE)), as nxnative by seedds, on which every build here stands; each branch carries its own notices for the code it takes from others (see also [Hermit's NOTICE.md](https://github.com/azmasm/hermit/blob/main/NOTICE.md)). Nintendo, Nintendo Switch 2 and the game names are trademarks of their owners. This project is not affiliated with or endorsed by Nintendo.
