# Guida HTML/CSS - Definizioni e Utilizzi

## HTML

### Elementi base

#### Struttura documento HTML
La struttura base di un documento HTML include `<!DOCTYPE html>`, `<html>`, `<head>` (con metadati, titolo, link a CSS), e `<body>` (con il contenuto visibile). Fornisce l'architettura fondamentale della pagina web.

#### Immagini
Tag `<img>` per inserire immagini. Attributi principali: `src` (percorso), `alt` (testo alternativo), `width` e `height`. Supporta formati JPG, PNG, GIF, SVG, WebP.

#### Audio
Tag `<audio>` per incorporare file audio. Attributi: `controls` (mostra controlli), `autoplay`, `loop`, `src`. Supporta MP3, WAV, OGG. Può contenere più `<source>` per compatibilità browser.

#### Video
Tag `<video>` per incorporare video. Attributi: `controls`, `autoplay`, `loop`, `muted`, `poster` (immagine anteprima), `width`, `height`. Formati: MP4, WebM, OGG.

#### Tabelle
Struttura dati tabulari con `<table>`, `<tr>` (righe), `<td>` (celle), `<th>` (intestazioni). Elementi aggiuntivi: `<thead>`, `<tbody>`, `<tfoot>`, `<caption>`. Attributi `colspan` e `rowspan` per celle unite.

#### Liste
Liste ordinate `<ol>` (numerate), non ordinate `<ul>` (puntate), e di definizione `<dl>`. Gli elementi sono contenuti in `<li>` per ol/ul, o `<dt>` e `<dd>` per dl.

#### Form
Tag `<form>` per creare moduli interattivi. Contiene elementi input come `<input>`, `<textarea>`, `<select>`, `<button>`. Attributi chiave: `action` (URL destinazione), `method` (GET/POST), `name`.

#### Link
Tag `<a>` per creare collegamenti ipertestuali. Attributo `href` specifica la destinazione. Altri attributi: `target` (_blank per nuova finestra), `rel`, `download`, `title`.

#### Testo e formattazione testo
Tag semantici per il testo: `<p>` (paragrafi), `<h1>`-`<h6>` (titoli), `<strong>` (grassetto importante), `<em>` (corsivo enfatico), `<span>` (inline generico), `<br>` (interruzione), `<hr>` (linea orizzontale).

#### Header & Footers
Tag semantici `<header>` e `<footer>` per definire intestazione e piè di pagina. Header contiene tipicamente logo, navigazione, titolo. Footer include copyright, link, contatti.

#### Favicons
Icona del sito che appare nella tab del browser. Si collega nell'head con `<link rel="icon" href="favicon.ico">`. Formati comuni: ICO, PNG, SVG. Dimensioni standard: 16x16, 32x32, 48x48 pixel.

---

## CSS Base

### Selettori e combinatori

#### Combinators
Operatori che definiscono relazioni tra selettori: discendente (spazio), figlio diretto (`>`), fratello adiacente (`+`), fratelli generali (`~`). Es: `div p` seleziona tutti i p dentro div.

#### Pseudo-classi
Selettori che definiscono uno stato speciale: `:hover` (mouse sopra), `:active` (clic), `:focus` (focus input), `:first-child`, `:nth-child()`, `:visited`, `:disabled`, `:checked`.

#### Pseudo-elements
Selettori per stilizzare parti specifiche: `::before` e `::after` (contenuto generato), `::first-letter` (prima lettera), `::first-line` (prima riga), `::selection` (testo selezionato).

### Proprietà di stile

#### Colori (CSScolors)
Definiscono colori usando diverse notazioni: nomi (`red`), esadecimale (`#FF0000`), RGB (`rgb(255,0,0)`), RGBA (con trasparenza), HSL (`hsl(0,100%,50%)`). Si applicano a `color`, `background-color`, `border-color`.

#### Font e tipografia
Proprietà per il testo: `font-family` (tipo carattere), `font-size` (dimensione), `font-weight` (spessore), `font-style` (italico), `line-height` (interlinea), `letter-spacing`, `text-transform`.

#### BackgroundIMG
Proprietà per immagini di sfondo: `background-image: url()`, `background-size` (cover/contain), `background-position`, `background-repeat` (repeat/no-repeat), `background-attachment` (fixed/scroll).

#### Borders
Definiscono bordi con `border`: `border-width`, `border-style` (solid/dashed/dotted), `border-color`, `border-radius` (angoli arrotondati). Possono essere specificati per lato (top/right/bottom/left).

#### Shadows
Creano ombre: `box-shadow` (ombre su elementi, parametri: x y blur spread color), `text-shadow` (ombre su testo). Possono essere multiple separate da virgola.

#### TextFormatting
Formattazione avanzata del testo: `text-align` (allineamento), `text-decoration` (underline/line-through), `text-indent` (rientro), `white-space`, `word-spacing`, `text-overflow`.

### Layout e posizionamento

#### Display
Definisce come un elemento è visualizzato: `block` (occupa tutta la larghezza), `inline` (in linea), `inline-block`, `none` (nascosto), `flex`, `grid`, `table`. Fondamentale per il layout.

#### Position
Controlla il posizionamento: `static` (default), `relative` (rispetto a posizione normale), `absolute` (rispetto al parent posizionato), `fixed` (rispetto al viewport), `sticky` (ibrido scroll-based).

#### Float
Proprietà legacy per layout: `left`, `right`, `none`. Fa "galleggiare" elementi permettendo al testo di scorrervi attorno. Spesso sostituito da Flexbox/Grid. Richiede `clear` per elementi successivi.

#### Z-index
Controlla l'ordine di sovrapposizione degli elementi posizionati sull'asse Z. Valori più alti appaiono sopra. Funziona solo con `position` diverso da static.

#### HeightWidth
Definiscono dimensioni: `width`, `height` (valori: px, %, em, vh/vw). Varianti: `min-width`, `max-width`, `min-height`, `max-height` per limiti. `box-sizing` controlla se padding/border sono inclusi.

#### Margins
Spazio esterno agli elementi: `margin-top`, `margin-right`, `margin-bottom`, `margin-left`, o shorthand `margin`. Valori: px, %, auto (per centrare). Margin collapsing tra elementi verticali adiacenti.

#### Overflow
Gestisce contenuto che supera le dimensioni: `visible` (default, esce), `hidden` (nascosto), `scroll` (sempre scrollbar), `auto` (scrollbar se necessario). Separabile in `overflow-x` e `overflow-y`.

---

## Componenti UI

### Elementi interattivi

#### Buttons
Pulsanti cliccabili creati con `<button>` o `<input type="button">`. Stilizzati con padding, background, border-radius, hover states. Attributi: `type` (submit/button/reset), `disabled`.

#### Dropdown
Menu a tendina con `<select>` e `<option>`, o custom con div+CSS+JS. Mostra/nasconde contenuto al click. Stilizzazione: frecce custom, animazioni, `z-index` per sovrapposizione.

#### NavigationBar
Menu di navigazione principale del sito. Struttura: `<nav>` con liste `<ul><li><a>`. Stili: orientamento orizzontale/verticale, sticky, responsive hamburger menu, active states.

#### Pagination
Navigazione tra pagine di contenuto. Lista di link numerati con prev/next. Stili: numeri circolari, active page evidenziata, hover effects, disabled states per limiti.

### Media e contenuti

#### Images
Gestione responsive delle immagini: `max-width: 100%`, `height: auto`, `object-fit` (cover/contain), filtri CSS, lazy loading, aspect-ratio, picture element per diverse risoluzioni.

#### ImgGallery
Raccolta di immagini in griglia. Layout con Flexbox/Grid, thumbnail cliccabili, lightbox per visualizzazione ingrandita, transizioni, hover effects, masonry layout opzionale.

#### Music
Player audio personalizzato oltre `<audio>` standard. Controlli custom (play/pause, volume, progress bar), playlist, visualizzazione traccia corrente, styling coerente cross-browser.

#### Video
Player video oltre `<video>` standard. Controlli custom, overlay, autoplay policies, picture-in-picture, fullscreen, captions/sottotitoli, poster frames, responsive sizing.

#### COOLicons
Set di icone (presumibilmente una libreria custom). Icone vettoriali SVG o icon font, scalabili, colorabili via CSS, leggere, usage: decorazione UI, pulsanti, indicatori stati.

---

## Flexbox

### Proprietà container

#### Flex Display
`display: flex` (o `inline-flex`) attiva il flexbox sul container. Trasforma figli in flex items con layout flessibile monodimensionale (riga o colonna).

#### Flex Direction
`flex-direction` definisce l'asse principale: `row` (default, orizzontale), `row-reverse`, `column` (verticale), `column-reverse`. Inverte anche start/end dell'asse.

#### Flex Wrap
`flex-wrap` controlla se gli items vanno a capo: `nowrap` (default, singola riga), `wrap` (multiple righe), `wrap-reverse` (wrap in direzione inversa).

#### Flex Flow
Shorthand per `flex-direction` e `flex-wrap`: `flex-flow: row wrap`. Combina entrambe le proprietà in una dichiarazione.

#### Justify Content
Allinea items lungo l'asse principale: `flex-start`, `flex-end`, `center`, `space-between` (spazio tra items), `space-around` (spazio attorno), `space-evenly` (spazio uguale).

#### Align Items
Allinea items lungo l'asse trasversale (singola riga): `stretch` (default), `flex-start`, `flex-end`, `center`, `baseline` (allinea baseline del testo).

#### Align Content
Allinea righe multiple quando c'è wrap: `stretch`, `flex-start`, `flex-end`, `center`, `space-between`, `space-around`. No effetto con singola riga.

### Proprietà elementi figli

#### Order
`order` cambia l'ordine visuale dei flex items. Default 0. Valori più bassi appaiono prima. Non modifica l'ordine DOM/tab order.

#### Flex Grow
`flex-grow` definisce la capacità di crescita dell'item. Default 0 (no crescita). Valori positivi distribuiscono spazio extra proporzionalmente.

#### Flex Shrink
`flex-shrink` definisce la capacità di restringersi. Default 1 (si restringe). 0 previene restringimento. Valori maggiori si restringono di più.

#### Flex Basis
`flex-basis` imposta dimensione base iniziale prima di distribuire spazio. Valori: px, %, auto. Override width/height lungo l'asse principale.

#### Align
`align-self` permette override di `align-items` per singolo item. Valori: `auto`, `flex-start`, `flex-end`, `center`, `baseline`, `stretch`. Allinea lungo asse trasversale.

# Grid

## Proprietà container

### Grid Display
`display: grid` (o `inline-grid`) attiva il grid sul container. Trasforma figli in grid items con layout flessibile bidimensionale (righe e colonne).

### Grid Template Columns
`grid-template-columns` definisce larghezza e numero delle colonne: valori fissi (`200px`), flessibili (`1fr`), percentuali, `auto`. Usa `repeat(3, 1fr)` per pattern ripetuti.

### Grid Template Rows
`grid-template-rows` definisce altezza e numero delle righe. Sintassi identica a columns: `100px auto 1fr`. Le righe possono essere implicite se non definite.

### Grid Template Areas
`grid-template-areas` definisce layout tramite stringhe di testo. Ogni stringa = riga. Ripetere nomi crea aree multi-cella: `"header header" "sidebar main"`. Usa `.` per celle vuote.

### Grid Template
Shorthand per `grid-template-rows`, `grid-template-columns` e `grid-template-areas`: `grid-template: "header" 100px "main" 1fr / 200px 1fr`. Divide rows/columns con `/`.

### Grid Gap / Gap
`gap` (o `grid-gap`) imposta spaziatura tra righe/colonne: `gap: 20px` (uguale) o `gap: 20px 10px` (row column). Sostituisce `grid-row-gap` e `grid-column-gap`.

### Justify Items
Allinea items orizzontalmente dentro le celle: `start`, `end`, `center`, `stretch` (default, riempie cella). Agisce su asse inline (colonne).

### Align Items
Allinea items verticalmente dentro le celle: `start`, `end`, `center`, `stretch` (default). Agisce su asse block (righe). Allineamento dentro singola cella.

### Justify Content
Allinea l'intera griglia orizzontalmente nel container: `start`, `end`, `center`, `stretch`, `space-between`, `space-around`, `space-evenly`. Utile quando griglia < container.

### Align Content
Allinea l'intera griglia verticalmente nel container: `start`, `end`, `center`, `stretch`, `space-between`, `space-around`, `space-evenly`. Distribuisce spazio extra tra righe.

### Grid Auto Columns
`grid-auto-columns` definisce dimensione delle colonne implicite (create automaticamente). Default `auto`. Valori: `100px`, `1fr`, `minmax(100px, 1fr)`.

### Grid Auto Rows
`grid-auto-rows` definisce dimensione delle righe implicite. Utile quando items superano righe definite. Esempio: `grid-auto-rows: 150px` crea righe uniformi.

### Grid Auto Flow
`grid-auto-flow` controlla posizionamento automatico: `row` (default, riempie righe), `column` (riempie colonne), `dense` (riempie buchi, modifica ordine visuale).

## Proprietà elementi figli

### Grid Column Start / End
`grid-column-start` e `grid-column-end` posizionano item sulle linee verticali: `grid-column-start: 1; grid-column-end: 3`. Le linee partono da 1. Usa `span 2` per estensione relativa.

### Grid Row Start / End
`grid-row-start` e `grid-row-end` posizionano item sulle linee orizzontali. Sintassi identica a column. Esempio: `grid-row: 1 / 4` (shorthand).

### Grid Column
Shorthand per `grid-column-start` e `grid-column-end`: `grid-column: 1 / 3` o `grid-column: 1 / span 2`. Posiziona item su range di colonne.

### Grid Row
Shorthand per `grid-row-start` e `grid-row-end`: `grid-row: 2 / 4` o `grid-row: span 2`. Posiziona item su range di righe.

### Grid Area
Shorthand per tutte le proprietà di posizionamento: `grid-area: row-start / col-start / row-end / col-end` oppure nome area: `grid-area: header` (da `grid-template-areas`).

### Justify Self
`justify-self` override di `justify-items` per singolo item. Valori: `start`, `end`, `center`, `stretch`. Allinea item orizzontalmente nella propria cella.

### Align Self
`align-self` override di `align-items` per singolo item. Valori: `start`, `end`, `center`, `stretch`. Allinea item verticalmente nella propria cella.

### Place Self
Shorthand per `align-self` e `justify-self`: `place-self: center` (entrambi) o `place-self: start end` (align justify). Centra o posiziona item in cella.

## Funzioni e valori utili

### Repeat
`repeat(count, size)` ripete pattern: `repeat(3, 1fr)` = `1fr 1fr 1fr`. Usa `auto-fit` o `auto-fill` per colonne responsive: `repeat(auto-fit, minmax(200px, 1fr))`.

### Minmax
`minmax(min, max)` definisce range dimensioni: `minmax(100px, 1fr)` (minimo 100px, cresce con spazio disponibile). Previene collassi e overflow.

### Fr Unit
`fr` (fraction) distribuisce spazio disponibile proporzionalmente. `1fr 2fr` = 1/3 e 2/3 della larghezza. Flessibile e responsive, considera gap automaticamente.

### Auto-fit vs Auto-fill
`auto-fit` collassa tracce vuote, `auto-fill` le mantiene. Con `repeat(auto-fit, minmax(200px, 1fr))` crea layout responsive senza media query. Tracce si adattano al container.

### Media Query

Le media query adattano il layout grid a diverse dimensioni schermo. Modificano `grid-template-columns/rows`, `gap`, o passano da grid multi-colonna a singola colonna su mobile.

Esempio comune: `@media (max-width: 768px) { grid-template-columns: 1fr; }` imposta layout a colonna singola. Usa `min-width` per approccio mobile-first progressivo.