Souboj je turn-based, hráč má na výběr v základu Basic Attack a Basic Defend, po dosažení levelu 5 se hráči odemknou frakce a vybere si jednu z nich. Frakce dají hráč speciální Damage a Defend abilitu a Basic Defend je zruší, ale Basic Attack zůstává.
# Logic
- **Basic Attack**: vždy dostupný, 0 cooldown, škálovaný podle vybavené zbraně.
    - Meč = melee strike
    - Luk = střelba
    - Kladivo = těžký úder  
    - Dýka = rychlý double strike  
    
- **DMG abilita**: unikátní pro frakci (4 kola CD, nebo variace).
    
- **DEFEND abilita**: unikátní pro frakci (2–3 kola CD).
# Factions
| Frakce                     | Odkaz na hru                 | DMG abilita (CD ~4)                                                            | DEFEND abilita (CD ~2–3)                                                   | Lore / poznámka                                          |
| -------------------------- | ---------------------------- | ------------------------------------------------------------------------------ | -------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Hollow Order** ⚔️        | Dark Souls / Elden Ring      | **Soul Crash** – obrovský delayed hit (aktivuje se až na konci příštího kola)  | **Dodge Roll** – vyhne se útoku, malá šance fail                           | Fanatici utrpení, věří, že „You Died“ je posvátný rituál |
| **Ghost Unit** 🎯          | Call of Duty                 | **360 Noscope** – 200% dmg, 40% šance miss, 20% šance na crit                  | **Flashbang.exe** – soupeř má sníženou přesnost 1 kolo                     | Digitální veteráni FPS bitev, žijí pro killstreaky       |
| **Eternal Realm** 💎       | World of Warcraft / MMO      | **Grinding Strike** – šance na extra follow-up hit                             | **Logout Shield** – sníží dmg o 75 %, ale příští kolo neútočíš             | Nekoneční farmáři XP a lootů, věří že život je jen grind |
| **The Glitchers** 🐺       | The Witcher 3 (Wither odkaz) | **Silver Slash** – silný útok, který ignoruje část obrany soupeře (např. 30 %) | **Glitched Quen** – štít, který pohltí dmg, ale může selhat (error chance) | Potulní bug-lovci, inspirovaní Zaklínačem                |
| **Red Plumbers** 🍄        | Super Mario Bros             | **Stomp Chain** – skočí na nepřítele, šance odrazit se na další (chain dmg)    | **Pipe Warp** – vyhne se příštímu útoku úplně, vrátí se s +initiative      | Kdysi instalatéři, dnes bug-skippers reality             |
| **Last Zone Survivors** 🪂 | Fortnite / PUBG              | **Closing Circle** – dmg roste podle HP nepřítele                              | **Build Wall** – absorbuje dmg z příštího útoku                            | Přeživší battle royale, stále čekají na drop             |
| **Pocket Tamers** 🐾       | Pokémon / Digimon            | **Bugmon Roulette** – vyvolá random pet s unikátním útokem                     | **Pet Shield** – mazlíček dostane dmg místo hráče                          | Lovci glitchnutých mazlíčků, tvoří „zoo frakci“          |
| **Voxel Architects** 🧱    | Minecraft                    | **TNT Toss** – AOE dmg, malá šance zasáhnout i hráče                           | **Block Wall** – vytvoří štít, malá šance že se rozpadne                   | Stavitelé glitch-kostek, kteří věří, že realita je voxel |
