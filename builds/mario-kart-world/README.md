# Mario Kart World: azmasm's build

- **Code:** branch [`switch2mac`](https://github.com/azmasm/hermit-engine/tree/switch2mac) of this repository (the branch keeps its old name: Hermit, its reports and its shader lists know this build by the id `switch2mac`).
- **Game:** Mario Kart World 1.0.0 (title ID `0400C3F00006E000`), from your own dump.
- **What it is:** a fork of nxnative with Switch 2 graphics (NVN2) on Metal, mesh and task shaders, movies, a Performance mode and the preparing screen. The game's shaders are lowered to Switch 1 shader code and translated from there, which runs faster on M1 and M2 chips.
- **How it runs:** about 58 fps in races on an M1 Max at 2560x1440. It uses 13 to 20 GB of memory, so Macs with 24 GB or more are recommended.
- **In Hermit:** [the game's page](https://github.com/azmasm/hermit/tree/main/games/mario-kart-world), with its known issues and players' reports. Its profile is [`dm/games/0400C3F00006E000`](https://github.com/azmasm/hermit-engine/tree/switch2mac/dm/games/0400C3F00006E000) on the branch.

To build it, use Hermit: choose your dump, press Build.
