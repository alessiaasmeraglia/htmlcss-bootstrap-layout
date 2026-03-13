# htmlcss-bootstrap-layout

## Descrizione

Progetto di esercitazione realizzato con **HTML, CSS e Bootstrap 5.3** per riprodurre un **layout con griglia responsive**.

L’obiettivo dell’esercizio è prendere confidenza con il sistema di **grid layout di Bootstrap**, imparando a gestire righe, colonne e comportamento responsive sui diversi dispositivi.

Il layout deve adattarsi correttamente a:

- **desktop**
- **tablet**
- **mobile**

seguendo gli screenshot forniti nella consegna.

## Tecnologie utilizzate

- HTML5
- CSS3
- Bootstrap 5.3

## Struttura del progetto

```text
htmlcss-bootstrap-layout/
│
├── index.html
├── README.md
└── css/
    └── style.css
```

## Obiettivi dell'esercizio

L'obiettivo era:

- usare correttamente la **Bootstrap Grid**
- organizzare il layout tramite **container**, **row** e **col**
- gestire il comportamento responsive con i breakpoint di Bootstrap
- ridurre al minimo il CSS custom
- ricreare una struttura fedele agli screenshot allegati

## Concetti Bootstrap messi in pratica

Durante l’esercizio vengono utilizzati soprattutto:

- `container` / `container-fluid`
- `row`
- `col`
- `col-*`
- `col-sm-*`
- `col-md-*`
- `col-lg-*`
- `col-xl-*`
- gutter con `g-*`
- utility di spacing come `p-*`, `m-*`, `px-*`, `py-*`
- utility di allineamento come `justify-content-*` e `align-items-*`

## Responsive design

Il layout è stato costruito per adattarsi automaticamente allo spazio disponibile:

- su **mobile** gli elementi tendono a disporsi in colonna
- su **tablet** alcune sezioni possono stare affiancate
- su **desktop** il layout sfrutta meglio la larghezza disponibile con più colonne sulla stessa riga

Bootstrap permette questo comportamento grazie ai suoi breakpoint responsive.

Esempio:

```html
<div class="col-12 col-md-6 col-lg-4">
  Contenuto
</div>
```

In questo caso:

- su schermi piccoli la colonna occupa tutta la larghezza
- da `md` in su occupa metà riga
- da `lg` in su occupa un terzo della riga

## Bonus svolti

### 1. Centralizzare il testo bianco

Sì, è possibile centralizzare il fatto che il testo sia bianco usando una classe Bootstrap già pronta:

```html
class="text-white"
```

Se più elementi condividono questa caratteristica, si può applicare `text-white` direttamente al contenitore padre.

Esempio:

```html
<section class="text-white">
  <h1>Titolo</h1>
  <p>Testo</p>
  <button class="btn btn-light">Pulsante</button>
</section>
```

In questo modo si evita di ripetere la stessa regola su ogni elemento figlio.

### 2. Centralizzare il layout delle colonne con `row-cols`

Sì, Bootstrap mette a disposizione la classe `row-cols-*` per definire in modo rapido quante colonne devono esserci in una riga, senza assegnare manualmente una larghezza a ogni `col`.

Esempio:

```html
<div class="row row-cols-1 row-cols-md-2 row-cols-lg-4 g-3">
  <div class="col">Colonna 1</div>
  <div class="col">Colonna 2</div>
  <div class="col">Colonna 3</div>
  <div class="col">Colonna 4</div>
</div>
```

In questo caso:

- su mobile c’è **1 colonna per riga**
- da `md` in su ci sono **2 colonne per riga**
- da `lg` in su ci sono **4 colonne per riga**

Questo approccio è molto utile quando più elementi hanno tutti la stessa struttura.

## Avvio del progetto

Per visualizzare il progetto:

1. scaricare o clonare la repository
2. aprire il file `index.html` nel browser

Non sono richieste installazioni particolari, perché Bootstrap può essere collegato tramite CDN.

## Note

Questo esercizio ha scopo didattico ed è utile per allenarsi su:

- uso pratico della griglia Bootstrap
- gestione dei breakpoint responsive
- organizzazione pulita del layout
- riduzione del CSS custom grazie alle utility del framework

## Autore

Progetto realizzato come esercizio didattico.
