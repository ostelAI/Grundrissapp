# Grundrissplaner

Grundriss-App fürs eigene Haus: Wände, Räume, Türen, Fenster und Einrichtung eintragen, Elemente miteinander verknüpfen und alles in 3D ansehen.

## Starten

`index.html` per Doppelklick im Browser öffnen (Chrome, Edge oder Firefox). Eine Internetverbindung wird für die 3D-Bibliothek (three.js vom CDN) gebraucht.

Alternativ als lokaler Server:

```bash
python -m http.server 8765
```

Danach http://localhost:8765 öffnen.

## Bedienung

| Taste | Werkzeug | Funktion |
|---|---|---|
| `V` | Auswahl | Anklicken & ziehen; leere Fläche ziehen = Ansicht verschieben; Mausrad = Zoom |
| `W` | Wand | Punkte klicken; **Zahl tippen + Enter = exakte Länge**; `Shift` = 90°; Doppelklick/Esc = fertig |
| `R` | Raum | In einen von Wänden umschlossenen Bereich klicken → Raum wird erkannt (Alt+Klick = frei zeichnen) |
| `T` / `F` / `G` | Tür / Fenster / Durchgang | Auf eine Wand klicken |
| `O` | Objekt | Möbel, Sanitär, Küche, Elektro (Steckdose, Schalter, Lampe, Sicherungskasten …) |
| `L` | Verknüpfen | Zwei Elemente anklicken, z. B. Schalter → Lampe; auch über Stockwerke hinweg |
| `M` | Messen | Abstand zwischen zwei Punkten |

Weitere Tasten: `Entf` löscht, `Q`/`E` drehen ein Objekt (mit Shift um 90°), `Strg+D` dupliziert, `Strg+Z`/`Strg+Y` für Rückgängig/Wiederholen, `Strg+S` speichert als Datei.

**Verknüpfungen im Plan:**
- Wände hängen an gemeinsamen Eckpunkten. Ziehst du einen Eckpunkt, ziehen alle angeschlossenen Wände mit.
- Automatisch erkannte Räume hängen an ihren Wänden, Fläche und Form passen sich also mit an.
- Eigene Verknüpfungen (z. B. Stromkreise oder „schaltet“) kannst du beschriften und einfärben.

Jedes Element kann **Notizen** und **eigene Angaben** bekommen (z. B. Hersteller, Preis, Einbaudatum).

## Rundgang (3D)

Klick in der 3D-Ansicht auf **🚶 Rundgang**. Du startest im größten Raum, oder beim gerade ausgewählten Element.

- Mit `W` `A` `S` `D` oder den Pfeiltasten läufst du, mit der Maus schaust du dich um. `Shift` lässt dich rennen.
- Durch Türen und Durchgänge kannst du gehen, durch Wände und Fenster nicht.
- Treppen kannst du einfach hochlaufen, oben wechselt das Stockwerk automatisch.
- Im 2D-Plan siehst du deine Position mit Blickrichtung. Ein Doppelklick im Plan oder ein Klick auf einen Stockwerk-Tab bringt dich direkt dorthin.
- `Esc` pausiert, ein zweites `Esc` beendet den Rundgang.

## Speichern

- Das Projekt wird automatisch im Browser gespeichert.
- *Datei → Projekt speichern* exportiert es als `.json`, zur Sicherung oder für einen anderen Rechner.
- Export ist auch als PNG (Grundriss) und als `.glb` (3D-Modell, z. B. für Blender) möglich.
