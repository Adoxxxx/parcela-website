# Parcela Website

Statische Website ohne Build-Schritt. Was im Repository liegt, ist genau das, was ausgeliefert wird.

## Aufbau

| Pfad | Inhalt |
|---|---|
| `index.html` | Landingpage für das Ausklapphaus 73 m² |
| `modelle/index.html` | Alle Bauweisen mit Haus-Finder |
| `impressum/index.html` | Impressum und Datenschutzerklärung |
| `assets/config.js` | Preise und WhatsApp-Nummer |
| `assets/fonts/` | Schriften (Archivo, Barlow Semi Condensed, SIL Open Font License 1.1) |
| `media/` | Videos und Bilder der Landingpage |

## Preise ändern

Alle Preise stehen in `assets/config.js`. Zahl ändern, speichern, committen, pushen.

- `f73` ist der Preis der Landingpage. Er erscheint im Hero, im Preisvergleich, im Abschluss, in der Handy-Leiste und in den WhatsApp-Nachrichten.
- `f38`, `r85` und `k38` stehen auf `null`. Sobald dort eine Zahl steht, zeigt die Seite bei diesem Haus „ab … €".
- Der Vergleichswert „160.600 bis 292.000 €" (73 m² zu 2.200 bis 4.000 € pro m², Quelle Infina, März 2026) steht fest in `index.html`.

Texte stehen in den HTML-Dateien jeweils im Block `const T={ de:{…}, bs:{…}, en:{…} }`, nach Sprache getrennt.

## Videos und Bilder tauschen

Neue Datei unter demselben Namen in `media/` ablegen (`hero.mp4`, `hero.jpg`, `orbit.mp4`, `orbit.jpg`, `living.jpg`, `bedroom.jpg`, `dusk.jpg`). Videos ohne Ton, H.264, möglichst unter 5 MB. Wenn echtes Material die KI-Bilder ersetzt, den Hinweis „Visualisierung" in `index.html` entfernen (Texte `viz`, `orbit.cap`, `foot`).

## Veröffentlichen

Die Seite läuft über GitHub Pages aus dem Zweig `main` unter https://www.parcela.at. Jeder Push auf `main` aktualisiert sie nach ein bis zwei Minuten.

## Domain

Die Seite läuft unter https://www.parcela.at. Die Datei `CNAME` im Repository legt das fest und darf nicht gelöscht werden.

DNS bei Hostinger:

| Typ | Name | Ziel |
|---|---|---|
| CNAME | www | adoxxxx.github.io |
| A | @ | 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 |

Aufrufe von parcela.at leitet GitHub auf www.parcela.at weiter.

## Firmendaten

Impressum und Datenschutz ziehen die Firmendaten aus dem Block `const F={…}` am Anfang des Skripts in `impressum/index.html`.
