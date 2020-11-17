# Hindernislauf EInführung
## ~avatar avatar @unplugged

Dies ist eine Einführung in das Programmieren von Spielen mit dem @boardname@. 





## ~ @unplugged
Es soll ein Hindernislauf programmiert werden.
Ziel des Spieles bewege die Spielfigur mit den Tasten A und B, so soll den Hindernissen aus, welche vom oberen Bildschirmrand nach unten bewegt werden um Punkte zu sammeln.


## ~ @unplugged
In dieser Einführung soll erstmal nur die Spielfigur erstellt werden und in das Thema der Sprites aus dem Bereich  ``||game:Spiele||`` eingeführt werden.

## Schritt 1: Erstelle eine Spielfigur
Als erstes erstellen wir uns eine ``||Variables: Variable||`` namens ``||Variables: Spielfigur||``. Diese kommt in den Block ``||basic: Beim Start|``.
```blocks
let Spielfigur: game.LedSprite = 0

```

## Schritt 2: Einen Sprite auf die Variable speichern
Im Bereich ``||game: Spiel||`` Wird mit den sogenannten Sprites gearbeitet. Diese sind Objekte welche mehrere Eigenschaften haben. Wie z.B. eine Ausrichtung (z.B. in x-Richtung oder y-Richtung), Einen X- bzw. Y- Wert haben, eine gewisse Helligkeit speichern können oder erkennen können ob sie einen Rand oder andere Sprites berühren.
Nehme nun aus dem Bereich ``||game: Spiel||`` den Block ``||game: erzeuge Sprite an Position x y ||``. Dieser wird in den Block unserer ``||Variables: Variable||`` geschoben.
Danach Sollte im Simulator eine LED in der Mitte des Calliope Displays leuchten, eben an der Position x=2 und y=2. Ändere nun den Y-Wert auf 4 um den Sprite an unteren Displayrand erscheinen zu lassen.

```blocks 
let Spielfigur = game.createSprite(2, 4)
```

## Schritt 3: Bewegen der Spielfigur
Lass die Spielfigur mit dem A-Knopf ein Feld nach links bewegen und mit dem B-Knopf ein Feld nach rechts.
Dazu benötigst du aus dem Bereich ``||Input: Eingabe||`` den Block ``||Input: Wenn Knopf A gedrückt||`` in diesen kannst du den Block ``||game: Sprite bewege um 1 ||`` hineinschieben. Wird nun der Knopf A gedrückt sollte sich deine Spielfigur um eins nach rechts bewegen. Um die spielfigur nach links zu bewegen kannst du sie um -1 bewegen.
Die Spielfigur bewegt sich auf der x-Achse, da sie eben in diese Richtung ausgerichtet ist. Dies ist für den Hindernislauf schon richtig. Testweise kannst du ``||basic: Beim Start|`` den Block ``||game: drehe rechts um 90° ||`` einschieben um die Spielfigur hoch und runter zu bewegen. 

```blocks


input.onButtonPressed(Button.A, function () {
    Spielfigur.move(-1)
})

input.onButtonPressed(Button.B, function () {
    Spielfigur.move(1)
})

let Spielfigur = game.createSprite(2, 4)
```

## ~avatar avatar @unplugged
Unter : [https://github.com/r00b1nh00d/SpieleBausteine/blob/master/KurzHilfe%20Spiele.pdf] findest du auch nochmal eine kurze Übersicht zu den Befehlen aus dem Bereich ``||game: Spiele||``.
Jetzt ist es an dir von dieses Tutorial zu verlassen und in den Editor zu wechseln. Füre dort die Hindernisse 1 bis 3 dem Programm hinzu und lass diese ``||basic: Dauerhauft||`` und immer wieder neu auf der Anzeige des @boardname@ von oben nach unten bewegen. Berührt ein Hindernis die Spielfigur ist das Spiel vorbei. Sind die Hindernisse am unteren Rand angelangt sollen sie erneut an ``||math: zufälliger||`` Stelle auftauchen und mittels ein Punkt vergeben werden.



> Diese Seite bei [https://r00b1nh00d.github.io/spiele_programmieren_lernen_hindernislauf/](https://r00b1nh00d.github.io/spiele_programmieren_lernen_hindernislauf/) öffnen

## Als Erweiterung verwenden

Dieses Repository kann als **Erweiterung** in MakeCode hinzugefügt werden.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Neues Projekt**
* klicke auf **Erweiterungen** unter dem Zahnrad-Menü
* nach **https://github.com/r00b1nh00d/spiele_programmieren_lernen_hindernislauf** suchen und importieren

## Dieses Projekt bearbeiten ![Build Status Abzeichen](https://github.com/r00b1nh00d/spiele_programmieren_lernen_hindernislauf/workflows/MakeCode/badge.svg)

Um dieses Repository in MakeCode zu bearbeiten.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Importieren** und dann auf **Importiere URL**
* füge **https://github.com/r00b1nh00d/spiele_programmieren_lernen_hindernislauf** ein und klicke auf Importieren

## Blockvorschau

Dieses Bild zeigt den Blockcode vom letzten Commit im Master an.
Die Aktualisierung dieses Bildes kann einige Minuten dauern.

![Eine gerenderte Ansicht der Blöcke](https://github.com/r00b1nh00d/spiele_programmieren_lernen_hindernislauf/raw/master/.github/makecode/blocks.png)

#### Metadaten (verwendet für Suche, Rendering)

* for PXT/calliopemini
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
