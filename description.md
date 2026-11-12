# english

Hides standard *Heroes III* content from random maps, templates and the starting town picker, while keeping it loaded in the game, so engine configs and map overrides that reference it keep working. Maps and saves that already contain vanilla towns, heroes, creatures or artifacts keep loading normally.

## How it works

Nothing is deleted. Vanilla objects are flagged so the engine stops offering them: factions and heroes disappear from the start screen and from taverns, creatures drop out of random pools and map generation, artifacts leave the random loot tables. The objects themselves stay loaded — that is why older maps and saves do not break.

## Submods

The mod is a set of independent submods. Each one is switched on and off separately in the launcher; all of them are enabled by default except **Hide vanilla: spells**.

- **Hide vanilla: Castle**, **Rampart**, **Tower**, **Inferno**, **Necropolis**, **Dungeon**, **Stronghold**, **Fortress**, **Conflux**, **Neutral** — one submod per vanilla faction. Each hides its faction together with its heroes and its creatures, so any vanilla town can be kept playable by switching off a single submod.
- **Hide vanilla: artifacts** — every vanilla artifact except the Grail, which the obelisk puzzle and town construction depend on. Spell scrolls stay as well. To keep the random artifact pools non-empty, the submod adds its own set, *Poor Man's Valor*: six cheap artifacts and one combined relic that gives +1 to all primary skills, morale and luck on top of its components.
- **Hide vanilla: secondary skills** — vanilla secondary skills are no longer offered on level-up and are not taught by witch huts, scholars or universities. Skills a hero starts with stay and can still be raised to expert. Secondary skills added by other mods are unaffected.
- **Hide vanilla: spells** — every vanilla spell leaves the mage guilds, shrines and scrolls. **Off by default**, because it requires a spell mod: an empty spell pool breaks random map generation, as the generator places spell scrolls for each of the five levels. The submod therefore hard-depends on *new-old-spells-plus* and moves one of that mod's third-level spells (Levitation) down to second level, so all five levels are covered.
- **Hide vanilla: campaign heroes** — the twelve campaign heroes of *Heroes III* stay out of random maps, the starting hero picker and taverns; their roles in the original campaigns are untouched. Switch the submod off if a mod of yours is supposed to unlock them.

## Notes

- **The mod needs creature mods.** With all vanilla creatures hidden the pool of random monsters becomes empty, and placing a random monster ends with `Cannot pick a random creature!` — random map generation stops. Keep at least one mod that brings its own creatures, or leave one faction submod enabled.
- On hand-made `.h3m` maps the map header carries its own lists of allowed heroes, creatures, artifacts and spells, and those take priority over this mod. Random maps and templates always follow it.
- The spells submod patches the *new-old-spells-plus* mod. If that mod renames or removes Levitation, the patch stops applying and the second spell level becomes empty again.

# russian

Скрывает стандартный контент *Heroes III* на случайных картах, в шаблонах и при выборе стартового города, оставляя его загруженным в игру — конфигурации движка и переопределения на карте продолжают работать. Карты и сохранения, где уже есть стандартные замки, герои, существа или артефакты, загружаются как обычно.

## Как это работает

Ничего не удаляется. Ванильные объекты помечаются так, что движок перестаёт их предлагать: фракции и герои исчезают с экрана старта и из таверн, существа выпадают из случайных пулов и генерации карт, артефакты уходят из случайной добычи. Сами объекты остаются загруженными — поэтому старые карты и сохранения не ломаются.

## Сабмоды

Мод состоит из независимых сабмодов. Каждый включается и отключается в лаунчере отдельно; все включены по умолчанию, кроме **«Скрыть: заклинания»**.

- **«Скрыть: Замок», «Оплот», «Башня», «Инферно», «Некрополис», «Подземелье», «Цитадель», «Крепость», «Сопряжение», «Нейтральные»** — по одному сабмоду на каждую стандартную фракцию. Каждый скрывает свою фракцию вместе с её героями и существами, поэтому любой стандартный замок можно оставить играбельным, отключив один сабмод.
- **«Скрыть: артефакты»** — все стандартные артефакты, кроме Грааля: на нём держатся головоломка обелисков и постройка города. Свитки заклинаний тоже остаются. Чтобы пулы случайных артефактов не опустели, сабмод добавляет собственный набор «Доблесть бедняка»: шесть дешёвых артефактов и один сборный реликт, который поверх эффектов составных частей даёт +1 ко всем базовым характеристикам, боевому духу и удаче.
- **«Скрыть: вторичные навыки»** — стандартные вторичные навыки больше не предлагаются при повышении уровня и не преподаются в ведьминых хижинах, у учёных и в университетах. Навыки, которые у героя есть со старта, остаются и прокачиваются до expert. Вторичные навыки из других модификаций не затрагиваются.
- **«Скрыть: заклинания»** — все стандартные заклинания уходят из гильдий магов, храмов и свитков. **Отключён по умолчанию**, потому что требует мода заклинаний: пустой пул заклинаний ломает генерацию случайных карт, так как генератор расставляет свитки для каждого из пяти уровней. Поэтому сабмод жёстко зависит от *new-old-spells-plus* и переносит одно из его заклинаний 3-го уровня (Levitation) на 2-й уровень, чтобы были закрыты все пять уровней.
- **«Скрыть: кампанейские герои»** — двенадцать кампанейских героев *Heroes III* не появляются на случайных картах, при выборе стартового героя и в тавернах; их роли в оригинальных кампаниях не затрагиваются. Отключите сабмод, если другой ваш мод должен открывать этих героев.

## Примечания

- **Моду нужны моды с существами.** Если скрыть всех ванильных существ, пул случайных монстров опустеет, и при расстановке случайного монстра движок выдаст `Cannot pick a random creature!` — генерация карт остановится. Оставьте хотя бы один мод, добавляющий своих существ, либо не отключайте один из фракционных сабмодов.
- На готовых картах `.h3m` в заголовке карты хранятся собственные списки разрешённых героев, существ, артефактов и заклинаний, и они главнее этого мода. Случайные карты и шаблоны всегда следуют моду.
- Сабмод заклинаний патчит мод *new-old-spells-plus*. Если в том моде заклинание Levitation переименуют или удалят, патч перестанет применяться, и второй уровень заклинаний снова опустеет.
