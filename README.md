# Grundrissplaner

Grundriss-App fürs eigene Haus: Wände, Räume, Türen, Fenster und Einrichtung eintragen, Elemente miteinander verknüpfen und alles in 3D ansehen und begehen. Funktioniert am PC und am Handy.

**Online:** https://ostelai.github.io/Grundrissapp/

## Starten

- Am einfachsten über den Link oben.
- Am Handy lässt sich die App über das Menü (⋮) → *Als App installieren* auf den Home-Bildschirm legen. Am iPhone geht das in Safari über *Teilen → Zum Home-Bildschirm*.
- Nach dem ersten Öffnen läuft sie auch offline.

Lokal geht es auch, mit einem kleinen Server:

```bash
python -m http.server 8765
```

Danach http://localhost:8765 öffnen.

## Hauptmenü

Beim Öffnen erscheint das Hauptmenü mit allen deinen Projekten als Vorschaubild. Neue Projekte legst du so an:

- **Haus nach Maß**: Breite, Tiefe, Stockwerke, Außenwand und Keller angeben, dann stehen die Außenwände sofort.
- **Leeres Projekt**: Du zeichnest alles selbst.
- **Beispielhaus**: Ein fertiges Haus zum Ausprobieren.
- **Datei öffnen**: Ein gesichertes Projekt (`.json`) laden.

Über ⋮ an einem Projekt kannst du es umbenennen, duplizieren, sichern oder löschen. Mit dem Haus-Symbol oben links kommst du aus jedem Projekt zurück ins Menü.

## Bedienung

| Werkzeug | Taste | Funktion |
|---|---|---|
| Auswahl | `V` | Anklicken/antippen & ziehen; leere Fläche ziehen = verschieben; Mausrad bzw. zwei Finger = Zoom |
| Wand | `W` | Punkte setzen. Für eine exakte Länge die Zahl tippen + Enter, oder oben Länge eingeben und Richtung (→ ↓ ← ↑) wählen |
| Raum | `R` | In einen umschlossenen Bereich klicken; der Raum wird erkannt (Alt+Klick = frei zeichnen) |
| Tür / Fenster / Durchgang | `T` / `F` / `G` | Auf eine Wand klicken |
| Objekt | `O` | Möbel, Küche, Bad, Elektro (Steckdose, Schalter, Lampe, Sicherungskasten …), Treppe |
| Verknüpfen | `L` | Zwei Elemente anklicken, z. B. Schalter → Lampe; geht auch über Stockwerke hinweg |
| Messen | `M` | Zwei Punkte setzen. Die Bemaßung bleibt mit Maßzahl im Plan stehen |

Weitere Tasten am PC:

| Taste | Funktion |
|---|---|
| `Entf` | Auswahl löschen |
| `Q` / `E` | Objekt drehen |
| `Strg+D` | Objekt duplizieren |
| `Strg+Z` / `Strg+Y` | Rückgängig / Wiederholen |
| `Strg+S` | Projekt als Datei sichern |

**Am Handy:**
- Unten ist die Werkzeugleiste. Darüber liegt eine Leiste mit Details zum gewählten Element; zum Aufklappen tippst du sie an.
- Mit zwei Fingern zoomst und verschiebst du den Plan.
- Doppeltippen beendet eine Wand.

**Jedes Element** kann Fotos (z. B. vom Sicherungskasten), eigene Angaben (Hersteller, Preis, Kaufdatum …) und Notizen bekommen. Angaben mit „Preis“ oder „Kosten“ im Namen werden in der Übersicht zu einer **Kostenübersicht** addiert. Über die **Suche** in der Übersicht findest du jedes Element in allen Stockwerken.

## 3D & Rundgang

- Die 3D-Ansicht zeigt alle Stockwerke. Mit *Schnitt* werden die Wände niedrig angezeigt, so siehst du von oben hinein.
- **Rundgang** startet die Ego-Perspektive. Am PC läufst du mit `WASD` und schaust mit der Maus. Am Handy läufst du mit dem Joystick links unten und schaust dich durch Wischen um. Treppen führen automatisch ins nächste Stockwerk.

## Speichern

- Alle Projekte werden automatisch auf dem jeweiligen Gerät gespeichert, im Browser.
- **Wichtig:** Sichere wichtige Projekte als Datei, über ⋮ → *Projekt sichern (.json)*. Die Datei enthält auch die Fotos. So überträgst du ein Projekt auch vom PC aufs Handy.
- Exportieren kannst du außerdem den Grundriss als Bild (`.png`) und das 3D-Modell (`.glb`, z. B. für Blender).
