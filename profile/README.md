# Doomwarriors Clan

Wir betreiben Quake III Arena Server mit dem OSP-Mod: **Duel**, **Team Deathmatch**,
**Capture The Flag** und **Instagib**. Hier liegt der Code, mit dem sie laufen.

🌐 [doomwarriors.de](https://www.doomwarriors.de)

## Repositories

| Repo | Inhalt | Upstream |
|---|---|---|
| [Quake3e](https://github.com/doomwarriors-clan/Quake3e) | Die Server-Engine. Unser Fork von Quake3e mit serverseitigen Multiview-Demos, `sv_onRestart` und lernenden Bots. | [ec-/Quake3e](https://github.com/ec-/Quake3e) |
| osp *(in Vorbereitung)* | **OSP 1.03a-dwc**: OSP 1.03a mit den Security-Fixes von xq3osp und unseren eigenen Änderungen. | [JKornev/xq3osp](https://github.com/JKornev/xq3osp) |
| [dwc-hp](https://github.com/doomwarriors-clan/dwc-hp) | Die Clan-Homepage. Sie zeigt Demos und Spielstatistiken der Server. | – |
| q3-servers *(privat)* | Das Deployment der vier Server mit Docker Compose. | – |

## Wie die Teile zusammenhängen

Engine und OSP veröffentlichen versionierte Releases. Die Server verwenden fest
eingetragene Versionen davon und werden erst auf einer Testinstanz geprüft.
Alle vier Server laufen mit derselben Engine und demselben OSP. Welche Funktionen,
etwa die Bots, ein Server nutzt, legt er selbst in seiner Config fest.

Engine-Branches im Fork:

- `main` spiegelt ec-/Quake3e ohne eigene Änderungen.
- `multiview` und `bots` sind eigenständige Features auf Basis von `main`. Sie sind so gebaut,
  dass wir sie auch als PR an den Upstream geben können.
- `dwc` fasst alles zusammen. Daraus entstehen die Releases (`dwc-YYYY.MM.DD`).

## Mitspielen

Du brauchst einen beliebigen Quake-III-Client, wir empfehlen
[Quake3e](https://github.com/ec-/Quake3e). Wähle in der Konsole den Mod mit
`/fs_game osp` und verbinde dich mit `/connect <server>:<port>`.

## Mitmachen

Bugs und Ideen kannst du als Issue im passenden Repo melden. Änderungen an `dwc`
(Engine) und `main` (OSP) laufen nur über Pull Requests mit Review.

## Lizenzen

Quake3e steht unter der GPLv2. Die Spieldaten von Quake III Arena (`pak0.pk3` usw.)
sind urheberrechtlich geschützt und nicht in diesen Repos enthalten.
