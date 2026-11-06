# Doomwarriors Clan

We run Quake III Arena servers with the OSP mod: **Duel**, **Team Deathmatch**,
**Capture The Flag** and **Instagib**. This is the code they run on.

🌐 [doomwarriors.de](https://www.doomwarriors.de)

## Repositories

| Repo | What | Upstream |
|---|---|---|
| [Quake3e](https://github.com/doomwarriors-clan/Quake3e) | The server engine. Our fork of Quake3e with server-side multiview demos, `sv_onRestart` and learning bots. | [ec-/Quake3e](https://github.com/ec-/Quake3e) |
| [osp](https://github.com/doomwarriors-clan/osp) | **OSP 1.03a-dwc**: OSP 1.03a with the security fixes of xq3osp and our own changes. | [JKornev/xq3osp](https://github.com/JKornev/xq3osp) |
| [dwc-hp](https://github.com/doomwarriors-clan/dwc-hp) | The clan homepage. It shows the servers' demos and game statistics. | – |
| q3-servers *(private)* | The deployment of the four servers with Docker Compose. | – |
| [qbot](https://github.com/doomwarriors-clan/qbot) | Discord bot with live stats of matches on the doomwarriors servers and overall stats from the doomwarriors.de homepage. | Heavily modified from [QBot](https://github.com/andreagiavatto/QBot) |
| [dwc-bots](https://github.com/doomwarriors-clan/dwc-bots) | The original Quake 3 bots with new weights and new names, delivered as `zzz_dwc_bots.pk3`. | – |

## How the parts fit together

The engine and OSP publish versioned releases. The servers use pinned versions
of them, which are tried on a test instance first. All four servers run the
same engine and the same OSP. Which features, such as the bots, a server uses
is set in its own config.

Engine branches in the fork:

- `main` mirrors ec-/Quake3e without changes of our own.
- `multiview` is a standalone feature based on `main`, built so that we can
  also offer it upstream as a pull request.
- `dwc` combines everything (multiview, bot memory, our server tweaks). The
  releases (`dwc-YYYY.MM.DD`) are built from it.

## Play

Any Quake III client works; we recommend
[Quake3e](https://github.com/ec-/Quake3e). Select the mod in the console with
`/fs_game osp` and connect with `/connect <server>:<port>`.

## Contribute

Report bugs and ideas as an issue in the matching repo. Changes to the main
branches only go in through pull requests.

## Licenses

Quake3e is licensed under GPLv2. The Quake III Arena game data (`pak0.pk3`
etc.) is copyrighted and not included in these repos.
