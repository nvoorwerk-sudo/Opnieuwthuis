# Opnieuw Thuis

Een open-source, no-code tool om een oproeppagina te maken voor mensen die
opnieuw beginnen: na een scheiding, de eerste eigen woning, na een brand
of verlies, of om welke andere reden dan ook. In plaats van alles nieuw te
kopen, kun je met deze pagina vrienden, familie en buren vragen of zij
spullen hebben die ze toch willen wegdoen.

**Live proberen:** open `index.html` lokaal, of publiceer de repo via
GitHub Pages (zie hieronder) en open `https://<jouw-gebruikersnaam>.github.io/<repo-naam>/`.

Een kant-en-klaar voorbeeld van wat de tool oplevert staat in
[`voorbeeld.html`](./voorbeeld.html).

## Bestandsstructuur

```
.
├── index.html        de generator zelf — formulier + live voorbeeld + download/kopieer
├── voorbeeld.html     een pasklaar gegenereerd voorbeeld, ter illustratie
├── README.md
├── CONTRIBUTING.md
├── LICENSE
└── .gitignore
```

Er is geen build-stap, geen package.json, geen dependencies. Alles draait
volledig in de browser.

## Hoe het werkt

1. Open `index.html` (dubbelklikken volstaat, of host het ergens).
2. Vul je verhaal, kleurthema en de spullen in die je zoekt.
3. Bekijk rechts direct een live voorbeeld.
4. Klik op **"Download jouw pagina"** of **"Kopieer HTML"**.
5. Plak het resultaat op je eigen site.

**In WordPress:** maak een nieuwe pagina, voeg een blok **"Aangepaste
HTML"** (Gutenberg) of **"Raw HTML"** (WPBakery) toe, en plak de code
erin. Publiceren.

De gegenereerde pagina is één zelfstandig HTML-bestand — het werkt net zo
goed op WordPress als op GitHub Pages, Netlify, Squarespace (via een
HTML-blok) of gewoon als los bestand.

## Hoe het contact verloopt

Als een bezoeker op **"ik bied dit aan"** klikt, vult diegene alleen zijn
naam in (en eventueel een aantal, als er meerdere van iets nodig zijn).
Er opent daarna een kant-en-klaar bericht via **e-mail of WhatsApp** —
dat de bezoeker zelf verstuurt naar het adres/nummer dat jij hebt
ingesteld.

Er wordt dus **niets automatisch bijgehouden of opgeslagen**. Bewust:
zo werkt de pagina altijd, op elke site, zonder database, account of
privacygevoelige opslag van gegevens van bezoekers. Is iets geregeld?
Dan pas je zelf de lijst aan (item verwijderen of aantal aanpassen) en
plaats je de bijgewerkte versie terug.

## Zelf aanpassen zonder de generator

Wie liever direct in code werkt, kan de HTML die de generator oplevert
ook met de hand bewerken. Alle content staat bovenaan het
`<script>`-blok in een leesbaar `itemsData`-blok; de kleuren staan als
CSS-variabelen (`--sand`, `--sage`, `--clay`, etc.) bovenin de `<style>`.

## Publiceren via GitHub Pages

Zo zet je je eigen kopie (of de generator zelf) live, gratis, via GitHub:

1. Maak op GitHub een nieuwe repository aan en push deze map ernaartoe:
   ```
   git init
   git add .
   git commit -m "Eerste versie van Opnieuw Thuis"
   git branch -M main
   git remote add origin https://github.com/<jouw-gebruikersnaam>/<repo-naam>.git
   git push -u origin main
   ```
2. Ga in de GitHub-repository naar **Settings → Pages**.
3. Kies bij **Source**: branch `main`, map `/ (root)`.
4. Opslaan. Na een paar minuten staat de site live op
   `https://<jouw-gebruikersnaam>.github.io/<repo-naam>/` — die pagina
   toont automatisch `index.html`, dus de generator zelf.
5. Wil je in plaats daarvan direct jouw *eigen ingevulde oproeppagina*
   live zetten (in plaats van de generator)? Genereer 'm via de tool,
   download het bestand, hernoem het naar `index.html`, en vervang
   daarmee het bestand in de repository.

## Licentie

MIT — zie [`LICENSE`](./LICENSE). Vrij te gebruiken, aan te passen en te
delen, ook voor eigen (commerciële) doeleinden.

## Bijdragen

Zie [`CONTRIBUTING.md`](./CONTRIBUTING.md). Dit project leent zich goed
voor meebouwen: extra kleurthema's, andere talen, of een variant voor
specifieke situaties (bijv. een opvang na brand, of een welkomstpagina
voor nieuwe buurtbewoners).
