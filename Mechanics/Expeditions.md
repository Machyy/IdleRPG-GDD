Expedice je v podstatě quest, akorát více rozsáhlý (je to náš quest systém), každá má svoji cestu (EXPEDITION PATH) skrz, kterou musí hráč kompletně projít aby ji dokončil a získal odměnu ve formě XP, Scrapů, popřípadě itemů
Expedice mohou mít pouze maximum 7 částí, mohou být i různé s méně
## PATH Types
### Story
- Čistě informační část o průběhu příběhu, většinou se bude nacházet na první pozici
- Zde je Title, text a button na pokračování
- GAMEOBJECT: Story
### Event
- Část o rozhodnutí, kde hráč může získat různé odměny (extra item nebo scrap, buff nebo debuff do dalšího boje)
- Hráč má na výběr 1-3 možností + je tam tlačítko "Leave"
	- Každá možnost je vázána na konkrétní atribut (Strength, Intelligence, Luck)
	- Po vybrání se spustí RollCheck (GAMEOBJECT: DiceRoll), každý rollcheck má předem danou hodnotu kterou hráč musí hodit + se přičítá k hozenému číslu hodnota rovna k výšce podle definovaného vybraného statu
	- Pokud hráč uspěje získává odměnu určenou pro tento event, pokud však neuspěje tak dostane náhodný debuff (Status effect) do dalšího souboje v expedici (nepočítá se na PvP nebo budoucí Island)
	- Když hráč se rozhodne neriskovat a vybere možnost "Leave", event přeskakuje a nezískává nic
- GAMEOBJECT: CurrentEvent
## Loot
- Hráč získá tzv. "GLITCH FRIDGE" - je to loot roll, každým kliknutím odhaluje vyšší raritu, do chvíle kdy se rarita stopne a item dané rarity se zobrazí (hráč item získá až po splnění expedice, pokud neuspěje - zemře nebo se rozhodne opustit probíhající expedici, veškeré odměny zmizí)
- Po otevření lootu, jakmile hráč znovu kamkoliv klikne tak PATH pokračuje do další části
- GAMEOBJECT: GlitchFridgeReveal
### Encounter
- Ukáže se opět Title, text a tlačítka - pro spuštění souboje a některé encountery budou mít k dispozici se vyhnout i souboje (opět jako v typu Event podle atributu a poté opět DiceRoll, pokud se povede tak se souboj neuskuteční a odměnu získá jako ze souboje a hráč pokračuje dál v PATH, pokud neuspěje tak získá random debuff a souboj se spustí automaticky)
- Protivník se na scéně ukáže v "ArtworkFrame" jako gameobject "EncounterEnemy"
- Pokud se hráč rozhodne pro souboj, hra se přesuje do CombatScene, po skončení souboje se přesune zpět a pokračuje dál v PATH, pokud prohraje soubor tak expedice končí bez odměny
- GAMEOBJECT: Encounter
### Objective
- Úplně stejně jako Story, akorát je to v modré barvě a je tam tlačítko, kterým získá hráč požadovaný Quest Item, dále pokračuje v PATH
- Tento type nemusí mít každá expedice, některé budou jen čistě na Encounter, tento typ je na questy pro najítí konkrétních předmětů
- GAMEOBJECT: Objective
### Extract
- Stejný jako story, v tmavší modré barvě
- Slouží k oznámení úspěšně splněné expedice
- Button hráče přenese zpět na scénu World
- GAMEOBJECT: Extract