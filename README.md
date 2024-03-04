# Tutorials-01

## Rem vs EM

### Rem (Root em):
- "Rem" er baseret på størrelsen af den rodfont, der er defineret i HTML-dokumentet.
- En rem er lig med størrelsen af den aktuelle fontstørrelse af roden, som er html elementet.
- Rodfontstørrelsen er som standard 16px, som svarer til "1rem". "2rem" er det dobbelte, altså 32px.

Use Case for "rem":
```
{
 fontsize: 1rem; /*Størrelsen på en font bliver angivet til 1rem, eller 16px*/
}
```
### Em (Emphasized):
- "Em" er baseret på størrelsen af det nærmeste parent-element med en defineret fontstørrelse.
- Fontstørrelserne fungere på samme måde som "rem", så hvis man har "5em", er det 5 * 16px.

Use Case for "em":
```
{
 border: 7em solid #f00; /*En border får en bredde på 7em, eller 112px, efterfulgt af andre værdier der definere en border style.*/
}
```

### Forskellen på rem og em:
- Rem er mere forudsigeligt, da det altid er baseret på rodfontstørrelsen, hvilket giver mere ensartede størrelser på tværs af ens website.
- Det at "em" kan variere afhængigt af det nærmeste parent-element med en defineret fontstørrelse, er med til at gøre "em" mere fleksibelt, men også mindre forudsigeligt.

## Responsive vs adaptive CSS

### Responsiv CSS:
- Responsivt design bruger en fleksibel grid-struktur og flydende layoutteknikker for at tilpasse sig forskellige skærmstørrelser og enheder.
- Responsiv design reagerer dynamisk på ændringer i skærmstørrelse ved hjælp af media queries, der ændrer layoutet baseret på skærmens bredde og højde.
- En responsiv webside tilpasser sig flydende, hvilket giver en konsistent brugeroplevelse på tværs af forskellige enheder, uanset om det er en stor computerskærm, en tablet eller en smartphone.


Use Case for responsiv CSS:

```
.sidebar {
    width: 25%; /* Flydende bredde */
}

main {
    width: 75%;
}
```

### Adaptiv CSS:
- Adaptivt design indebærer at oprette forskellige layout og designs til forskellige enhedsstørrelser eller skærmopløsninger.
- Når en bruger besøger websiden, detekterer den enheden eller skærmstørrelsen og indlæser det tilsvarende design.
- Adaptivt design kan være mere omkostningstungt at udvikle, da det kræver oprettelse af flere designs, men det kan også give mere kontrol over brugeroplevelsen på hver enhed.

Use Case for adaptiv CSS:

```
.sidebar {
    width: 25px; /* Fast bredde */
}

main {
    width: 75px;
}

@media screen and (max-width: 768px) {
    /* Der ændres på bredden hvis skærmstørrelsen er 768px eller under */
    .sidebar,
    main {
        width: 100px;
    }
}
```

### Forskellen på responsiv og adaptiv CSS:

Responsiv design:
- Bruger en enkelt, flydende layoutstruktur.
- Tilpasser sig dynamisk ændringer i skærmstørrelsen.
- Kræver færre ressourcer og kan give en mere konsistent brugeroplevelse.
- Velegnet til et bredt spektrum af enheder.

Adaptiv CSS:
- Bruger separate, faste layoutstrukturer til forskellige enheder.
- Indlæser det specifikke layout baseret på enhedens detektering.
- Kræver mere udviklingstid og ressourcer.
- Kan give mere skræddersyede brugeroplevelser, men kan være mindre fleksible på tværs af enheder.
