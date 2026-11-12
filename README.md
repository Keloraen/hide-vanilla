# Hide vanilla

**hide-vanilla** removes standard *Heroes III* content from random maps, map templates, the starting town picker and taverns — while keeping every object loaded, so existing maps and saves that reference them keep working. It is meant for setups where VCMI runs without the original game content and only mod-provided towns, heroes, creatures, artifacts, skills and spells should appear.

- **Version:** 1.0.0
- **Engine:** VCMI 1.7.x
- **Structure:** 14 independent submods, each switchable in the launcher

Nothing is deleted: vanilla objects are flagged, so the engine stops offering them, but the definitions stay loaded and merge with everything else.

## Submods

| Submod | What it does |
|---|---|
| `castle`, `rampart`, `tower`, `inferno`, `necropolis`, `dungeon`, `stronghold`, `fortress`, `conflux`, `neutral` | hides the faction with its heroes and creatures; switch one off to keep that town playable |
| `artifacts` | hides every vanilla artifact except the Grail and spell scrolls, and adds the *Poor Man's Valor* set so artifact pools never go empty |
| `skills` | vanilla secondary skills are no longer offered on level-up or taught by huts, scholars and universities; starting skills can still be raised to expert |
| `spells` | removes every vanilla spell from guilds, shrines and scrolls — **off by default**, requires a spell mod |
| `campaign-heroes` | keeps the twelve campaign heroes out of random maps and taverns |

## Requirements

- VCMI **1.7** or newer.
- **At least one mod that adds creatures.** With every vanilla creature hidden the pool of random monsters is empty and random map generation stops with `Cannot pick a random creature!`.
- The `spells` submod additionally requires **new-old-spells-plus** (it is declared as a hard dependency and moves one of that mod's third-level spells down to second level so all five spell levels are covered).

## Installation

1. Open the VCMI launcher → **Mods**, find *Hide vanilla content* and install it, or unpack this repository into `Documents/My Games/vcmi/Mods/hide-vanilla`.
2. Enable the submods you need. The `spells` submod stays off until a spell mod is installed.
3. Start a random map — vanilla towns, heroes, creatures, artifacts, skills and spells will no longer be offered.

## Known interactions

- **preserve-town** — incompatible with the `skills` submod: that town has a building offering a choice of vanilla secondary skills.
- **campaign-heroes** — incompatible with the `campaign-heroes` submod by design: the mod exists to make those very heroes playable.
- **hota**, **tears-of-ashan**, **the-lost-tales** — they re-enable some campaign heroes; the submod declares soft dependencies so its own setting is applied last and wins.
- Maps made by hand (`.h3m`) carry their own lists of allowed heroes, creatures, artifacts and spells in the map header, and those take priority over this mod. Random maps and templates always follow it.

## Repository layout

```
mod.json                  main mod description
description.md            launcher description (english / russian)
mods/<submod>/mod.json    submods, each with its own Content/
mods/artifacts/Content/   artifacts, translations and sprites of the Poor Man's Valor set
```

## Credits

Author: Keloraen. Artifact icons and adventure-map animations were drawn for this mod.

## Licence

Not chosen yet — contact the author before redistributing the artwork.

---

## По-русски

Мод скрывает стандартный контент *Heroes III* на случайных картах, в шаблонах, при выборе стартового города и в тавернах, но оставляет все объекты загруженными — поэтому старые карты и сохранения продолжают работать.

Состоит из 14 независимых сабмодов (по одному на фракцию, плюс артефакты, вторичные навыки, заклинания и кампанейские герои); каждый включается и отключается в лаунчере отдельно.

**Важно:** нужен хотя бы один мод, добавляющий существ, иначе пул случайных монстров опустеет и генерация карт остановится. Сабмод `spells` дополнительно требует мод заклинаний `new-old-spells-plus`.