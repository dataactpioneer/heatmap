# Heat Map Data Act – Hinweise zur Pflege

## Dateien

- `index.html` – Gerüst, Gestaltung und Logik der Matrix. Hier steht kein Inhalt.
- `daten.js` – sämtliche Inhalte.
- `Heat-Map-Data-Act.html` – beide Dateien in einer einzigen Datei zusammengefasst, zum Weitergeben und Öffnen ohne Entpacken.

Zum Bearbeiten `index.html` und `daten.js` im selben Ordner belassen und `index.html` im Browser öffnen.

## Inhalte ändern

Alle Änderungen finden in `daten.js` statt. Die Matrix passt sich automatisch an, es muss nichts an `index.html` angefasst werden.

- `KRITERIEN` – die Spalten der Matrix. Ein neuer Block ergibt eine neue Spalte.
- `SKALA` – die Lesehilfe unter der Farbskala und im zugehörigen Detailfeld.
- `KATEGORIEN` – die Zwischenüberschriften, nach denen die Zeilen gruppiert werden.
- `FRAGEN` – die Rechtsfragen, also die Zeilen der Matrix. Ein neuer Block ergibt eine neue Zeile.
- `ABSCHLUSSHINWEIS` und `DISCLAIMER` – die beiden Absätze unter der Matrix.

## Aufbau eines Frageblocks

| Feld | Bedeutung |
| --- | --- |
| `id` | eindeutiger Schlüssel, kleingeschrieben, ohne Leerzeichen |
| `kategorie` | muss einer `id` aus `KATEGORIEN` entsprechen |
| `kurztitel` | Beschriftung der Zeile in der Matrix |
| `frage` | die ausformulierte Rechtsfrage, erscheint im Detailfeld |
| `normen` | die Rechtsgrundlagen, erscheinen klein unter dem Kurztitel |
| `einleitung` | Liste von Absätzen zur Einordnung |
| `abschnitte` | Liste von Abschnitten, je mit `titel`, `absaetze` und wahlweise `punkte` |
| `fazit` | ein Absatz |
| `empfehlungen` | Liste von Handlungsempfehlungen |
| `literatur` | Liste der herangezogenen Quellen |
| `bewertungen` | je ein Eintrag pro Kriterium, mit `score`, wahlweise `spanne`, und `text` als Begründung |

Die Schlüssel in `bewertungen` müssen mit den `id`-Werten in `KRITERIEN` übereinstimmen, sonst bleibt die Zelle leer.

## Nach dem Bearbeiten

`Heat-Map-Data-Act.html` wird aus `index.html` und `daten.js` erzeugt und aktualisiert sich nicht von selbst. Wenn die Einzeldatei weitergegeben werden soll, muss sie nach einer Änderung neu erstellt werden.
