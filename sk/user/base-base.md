# Základné vstavané príkazy a funkcie

## Príkazy

### `ping`

Zobrazí latenciu medzi botom a Discord API gateway.
Tento príkaz môže byť použitý pri debugovaní pomalých odpovedí bota.

### `uptime`

Zobrazí čas spustenia bota a ako dlho beží od spustenia.

## Funkcie

### Automatické vlákna

Niektoré kanály môžu vytvárať vlákna pre každú odoslanú správu.

Táto funkcia sa využíva v QnA kanáloch alebo iných typoch kanálov, kde moderátori chcú povoliť diskusiu, no chcú mať všetky ich správy viditeľné. 

### Záložky

Na ktorúkoľvek správu môžeš zareagovať emotikonom 🔖 (**:bookmark:**).

Ak je funkcia povolená, bot ti pošle súkromnú sprácu s obsahom pôvodnej správy s autorovým menom a odkazom na originál.

Môžeš to použiť, aby si si uložil všetky vtipy tvojich kamarátov.

### Používateľský pinning

Možno nemáš povolenú **Správu správ**, ale stále môžeš pripínať správy!

Ak je povolené, ty aj ostatní členovia môžete použiť 📌 (**:pushpin:**) emotikon na ktorúkoľvek správu a ak vás zareaguje dosť, správa bude pripnutá.

### Používateľské vlákna

Aj keď nemáš povolené vytvárať nové vlákna, môžeš to urobiť cez bota.

Ak je povolené, ty aj ostatní členovia môžete použiť🧵 (**:thread:**) emotikon na ktorúkoľvek správu a ak vás zareaguje dosť, vlákno sa vytvorí.

### Odstraňovanie súkromných správ od bota

Bot ti môže odosielať súkromné správy pre niektoré interakcie.
Ak zareaguješ na jeho správu s 🗑 (**:wastebasket:**) emotikonom, tak sa správa zmaže a vyčistí ti históriu chatu.
