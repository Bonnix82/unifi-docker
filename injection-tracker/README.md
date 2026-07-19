# Einstichstellen-Tracker

Ein kleines, eigenständiges Web-Tool zur Rotation von Spritzen-Einstichstellen (Bauch und Oberschenkel, je 3 Stellen pro Seite = 12 Stellen insgesamt).

## Nutzung

Einfach `index.html` im Browser öffnen (lokal per Doppelklick oder über GitHub Pages/einen beliebigen Webserver). Es wird keine Internetverbindung und kein Backend benötigt — alle Daten werden lokal im Browser (`localStorage`) gespeichert.

Alle Konfiguration (Spritzen, Bereiche, Intervalle, Einstichstellen verwalten, Export/Import/Reset) liegt gesammelt im Dialog hinter dem "⚙️ Einstellungen"-Button oben rechts, damit die Hauptseite übersichtlich bleibt.

## Funktionen

- **Körperkarte**: anatomisch orientierte SVG-Silhouette mit 12 Einstichstellen (Bauch links/rechts × 3, Oberschenkel links/rechts × 3), farblich nach Ruhezeit markiert. Zeigt außerdem die Bauchnabel-Sperrzone als Referenz.
- **Zwei individuell konfigurierbare Spritzen**: jede Spritze bekommt einen eigenen Namen (z.&nbsp;B. "MTX", "Hyrimoz"), eine frei wählbare Liste einzelner Einstichstellen (nicht nur grob "Bauch" oder "Oberschenkel", sondern jede der 12 Stellen einzeln an-/abwählbar, inkl. Schnellauswahl "Nur Bauch"/"Nur Oberschenkel"/"Alle"/"Keine") und ein eigenes Injektionsintervall (Mindestabstand in Tagen). "Injektion eintragen" ist gesperrt, solange der Mindestabstand nicht erreicht ist — inklusive Hinweistext, ab wann die nächste Injektion frühestens fällig ist.
- **Temporäre Bereichsnutzung**: eine Stelle kann im Protokollier-Dialog bewusst der jeweils anderen Spritze zugeordnet werden (z.&nbsp;B. wenn eine Zone ausnahmsweise mitbenutzt wird), auch wenn sie nicht zu deren regulär zugeordneten Stellen gehört. Die Stelle rutscht dadurch automatisch ans Ende ihrer eigenen Rotation, unabhängig davon, welche Spritze sie genutzt hat.
- **Was verwalten**: Spritze 1, Spritze 2 und der Medikamenten-Tracker lassen sich einzeln ein-/ausblenden — z.&nbsp;B. nur eine Spritze, zwei Spritzen, oder zusätzlich ein Medikament.
- **Automatische Empfehlung**: pro aktiver Spritze wird die am längsten unbenutzte Stelle im jeweiligen Bereich vorgeschlagen, inklusive automatischem Seitenwechsel (links/rechts) wenn möglich.
- **Medikamenten-Tracker**: für Medikamente mit festem Einnahme-Rhythmus (z.&nbsp;B. Folsäure, die typischerweise einen Tag nach MTX genommen wird). Pro Medikament: Name, Mindestabstand zwischen Einnahmen, wahlweise fester Abstand oder "X Tage nach Spritze Y". "Einnahme eintragen" ist ebenfalls durch den Mindestabstand gesperrt, mit Hinweistext.
- **Einstichstellen dauerhaft deaktivieren**: einzelne Stellen (z.&nbsp;B. wegen Narbe/Verhärtung) lassen sich dauerhaft aus der Rotation herausnehmen — sie werden nie mehr vorgeschlagen und erscheinen ausgegraut auf der Körperkarte.
- **Protokoll**: jede Injektion/Einnahme wird mit Datum/Uhrzeit gespeichert und in einer Tabelle aufgelistet.
- **Überspringen**: eine vorgeschlagene Stelle kann übersprungen werden — sie gilt dann als "berührt" und rutscht ans Ende der Rotation, ohne als tatsächliche Injektion gezählt zu werden.
- **Überschreiben/Bearbeiten**: jede beliebige Stelle kann manuell ausgewählt werden (unabhängig vom Vorschlag), und jeder Protokolleintrag lässt sich nachträglich bearbeiten oder löschen.
- **Falscher letzter Eintrag korrigieren**: sperrt der Mindestabstand eine Spritze/ein Medikament aufgrund eines versehentlichen oder falschen letzten Eintrags, führt ein Link direkt in der Warnung zum Bearbeiten/Löschen dieses Eintrags — ohne erst in der Protokoll-Tabelle danach suchen zu müssen.
- **Demo-Modus** (in den Einstellungen unter "Allgemein"): ignoriert alle Mindestabstände, damit man beliebig oft Injektionen/Einnahmen protokollieren kann, z.&nbsp;B. um die App vorzuführen oder auszuprobieren. Ein Banner erinnert daran, solange er aktiv ist; alle währenddessen angelegten Einträge werden im Protokoll mit "Demo" markiert.
- **Export/Import**: die Daten lassen sich als JSON-Datei sichern und wieder einspielen.

## Hinweis

Dieses Tool dient nur der persönlichen Organisation der Einstichstellen-Rotation. Es ersetzt keine medizinische Beratung — die im Tool angegebenen allgemeinen Abstände (z.&nbsp;B. 5&nbsp;cm um den Bauchnabel) stammen aus öffentlichen Packungsbeilagen/Fachinformationen gängiger Fertigspritzen und ersetzen nicht die Anleitung deines konkreten Präparats oder die Rücksprache mit Arzt/Ärztin oder Apotheke.
