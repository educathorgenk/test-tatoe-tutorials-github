# ventilator

## It's time to code! @showdialog

Zorg voor verluchting in de feesttent! 
Als je op knop A drukt, schakelt de ventilatie in.

## Bij de start

Je wil knop A gebruiken om de ventilator aan te zetten. Maar eens je de
knop loslaat, schakelt de ventilator uit. 
De ventilator gaat aan zolang je de knop ingedrukt houdt, en uit zodra je loslaat.

Dit is een voorwaarde en deze ziet er als volgt uit:

- **Als** button A wordt ingedrukt => *ventilator aan*
- **Anders** = > *ventilator uit*

In de  ``||logic:Logisch||`` categorie vind je **voorwaarden**. 

- Selecteer het ``||logic:als, anders||`` blok.
- Sleep dit blok in het ``||basic:de hele tijd||`` blok.

Dit blok laat je toe deze taak uit te voeren:
- Als je voorwaarde waar is, doe je iets.
- Als je voorwaarde niet waar is, doe je iets anders.

Klik op het lampje voor een tip.

```blocks
basic.forever(function () {
    if (true) {
        
    } else {
        
    }
})

```

## voorwaarde

De voorwaarde ziet er als volgt uit:
- **Als** button A wordt ingedrukt => *ventilator aan*
- **Anders** = > *ventilator uit*

Hoe maak je deze voorwaarde aan?

- In de ``||input:Invoer||`` categorie vind je het blok ``||input:knop A wordt ingedrukt ||``.
- Sleep dit blok in de "als".

Klik op het lampje voor een tip.

```blocks
basic.forever(function () {
    if (input.buttonIsPressed(Button.A)) {
        
    } else {
        
    }
})
```



## zet de ventilator aan

*Als de button A is ingedrukt*, zet je de ventilator aan.

Kan je bij de categorie ``||pins:Pinnen||`` een blok vinden dat de ventilator
op *aan* zet?

- Tip: je ventilator is aangesloten op digitale pin P2.
- De ventilator *aanzetten* doe je door de digitale pin waar hij op aangesloten
 op "1" te zetten.
- Sleep dit blok op de juiste plaats in je code.
- Vergeet de pin niet aan te passen (pin P2).

Klik op het lampje voor een tip.

```blocks
basic.forever(function () {
    if (input.buttonIsPressed(Button.A)) {
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        
    }
})
```


## reset

- **Als** button A wordt ingedrukt => *ventilator aan*
- **Anders** = > *ventilator uit*

Zet nu de ventilator uit zodra je de knop niet loslaat.
Of zet de digitale pin waar de ventilator op is aangesloten op "0".

Klik op het lampje voor een tip.

```blocks
basic.forever(function () {
    if (input.buttonIsPressed(Button.A)) {
        pins.digitalWritePin(DigitalPin.P2, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P2, 0)
    }
})
```


## KLAAR
Download de code op je micro:bit!