# Einstichstellen-Tracker

Ein kleines, eigenständiges Web-Tool zur Rotation von Spritzen-Einstichstellen (Bauch und Oberschenkel, je 3 Stellen pro Seite = 12 Stellen insgesamt).

## Nutzung

Einfach `index.html` im Browser öffnen (lokal per Doppelklick oder über GitHub Pages/einen beliebigen Webserver). Es wird keine Internetverbindung und kein Backend benötigt — alle Daten werden lokal im Browser (`localStorage`) gespeichert.

## Funktionen

- **Körperkarte**: 12 Einstichstellen (Bauch links/rechts × 3, Oberschenkel links/rechts × 3), farblich nach Ruhezeit markiert.
- **Automatische Empfehlung**: Für zwei Spritzen werden gleichzeitig zwei Stellen vorgeschlagen — jeweils die am längsten unbenutzte Stelle. Standardmäßig ist der Bauch für Spritze 1 und der Oberschenkel für Spritze 2 reserviert, damit beide Spritzen nicht denselben Bereich beanspruchen (in den Einstellungen abschaltbar oder vertauschbar). Zusätzlich wird wenn möglich nach jeder Injektion auch die Körperseite (links/rechts) innerhalb des jeweiligen Bereichs gewechselt.
- **Protokoll**: Jede Injektion wird mit Datum/Uhrzeit gespeichert und in einer Tabelle aufgelistet.
- **Überspringen**: Eine vorgeschlagene Stelle kann übersprungen werden — sie gilt dann als "berührt" und rutscht ans Ende der Rotation, ohne als tatsächliche Injektion gezählt zu werden.
- **Überschreiben/Bearbeiten**: Jede beliebige Stelle kann manuell ausgewählt werden (unabhängig vom Vorschlag), und jeder Protokolleintrag lässt sich nachträglich bearbeiten oder löschen.
- **Export/Import**: Die Daten lassen sich als JSON-Datei sichern und wieder einspielen.

## Hinweis

Dieses Tool dient nur der persönlichen Organisation der Einstichstellen-Rotation. Es ersetzt keine medizinische Beratung — allgemeine Empfehlungen zu Mindestabständen zwischen Injektionen an derselben Stelle bitte mit Arzt/Ärztin oder Packungsbeilage abstimmen.
