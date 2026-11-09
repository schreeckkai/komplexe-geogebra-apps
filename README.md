# Komplexere GeoGebra-Apps

Sammlung interaktiver GeoGebra-Lernapps mit nachvollziehbarer Mathematik, responsivem Layout und wiederverwendbarer Struktur.

## Erste App: Substitution

`apps/substitution-vergleich/index.html` stellt ein bestimmtes Integral auf der x-Achse und sein substituiertes Gegenstück auf der u-Achse gegenüber. Die App verwendet GeoGebra Graphing Calculator als eingebettete Applets und benötigt beim Aufruf eine Internetverbindung.

### Lokal öffnen

Nicht per Doppelklick als `file://` öffnen. Im Ordner `apps/substitution-vergleich` einen lokalen Webserver starten:

```sh
python3 -m http.server 8000
```

Dann im Browser `http://localhost:8000` öffnen. Alternativ kann die Datei auf einem Webserver oder über GitHub Pages bereitgestellt werden.

## Mathematik

Für `u = ax + b` mit `a > 0` gilt `du = a dx`, also `dx = du/a`. Damit wird

`∫[x₁,x₂] (ax+b)^n dx = ∫[ax₁+b, ax₂+b] u^n/a du`.

Verglichen werden orientierte Integralwerte, nicht notwendigerweise geometrische Flächeninhalte. Derzeit beschränkt sich die App bewusst auf diese parametrisierte Funktionsfamilie.

## Ausbauprinzip

- Jede App erhält ein eigenes Verzeichnis unter `apps/`.
- Quelldatei und eine knappe Erklärung/Bedienungsanleitung gehören zusammen.
- GeoGebra-Dateien (`.ggb`) können ergänzend aufgenommen werden, wenn sie unabhängig von der HTML-Einbettung direkt in GeoGebra nutzbar sind.
