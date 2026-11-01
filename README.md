# PV-Anlagenrechner

Browserbasierter Rechner für Ertrag, Verschaltung und Wirtschaftlichkeit von Photovoltaikanlagen mit optionalem Batteriespeicher. Eine einzige HTML-Datei, ohne Installation, ohne Server, ohne Build.

## Funktionen

- **Stündliche Jahressimulation (8.760 h)** mit Sonnenstand, Transposition auf die Modulebene (Hay-Davies), Reflexion, Modultemperatur, Schwachlicht, Horizont- und Reihenverschattung (auch Ost-West)
- **Dachflächen:** Rechteck, Trapez, Dreieck; Dachform-Assistent für Sattel-, Walm-, Pult-, Zelt- und Flachdach
- **Wechselrichter-Empfehlung:** Leistungsklasse, Anzahl, MPP-Tracker und Stringaufteilung inkl. Spannungsnachweis (DIN VDE 0100-712); alternativ manuelle Gerätedaten
- **Belegungsplan** mit Stringverlauf, Übersichtsschaltplan, MPPT-Prüfung, DC-Leitungen und Stückliste
- **Verbrauch:** BDEW-Lastprofil H0, Büro, Schule, Gewerbe oder eigener Lastgang (8.760 h / 35.040 ¼h); Wärmepumpe und E-Auto mit Überschussladen
- **Speicher:** technische und wirtschaftliche Größenempfehlung, Größenvergleich, DC-/AC-Kopplung
- **Wirtschaftlichkeit:** Kapitalwert, interner Zinsfuß, Amortisation, Stromgestehungskosten, Cashflow, Finanzierung, Ersatzinvestitionen
- **EEG 2026:** Vergütungssätze ab 01.08.2026, 60-%-Einspeisegrenze, keine Vergütung bei negativen Preisen (Solarspitzengesetz)
- **Auswertungen:** Einstrahlungsfächer nach Ausrichtung und Neigung, Sensitivität, Einfluss des Wetterjahres
- Infotexte zu allen Eingaben und Kennzahlen, Beispielszenarien, Export von Parametern und Ergebnissen (CSV)

## Nutzung

**Lokal:** `index.html` im Browser öffnen. Für die Diagramme ist eine Internetverbindung nötig (Chart.js über CDN).

**GitHub Pages:**

1. `index.html` ins Hauptverzeichnis des Repositorys legen.
2. Eine leere Datei `.nojekyll` anlegen (`touch .nojekyll`). Sonst macht GitHub Pages aus dieser README die Startseite.
3. *Settings → Pages → Source: Deploy from a branch*, Branch `main`, Ordner `/ (root)`.
4. Nach ca. einer Minute erreichbar unter `https://<benutzername>.github.io/<repository>/`.

Eingaben werden lokal im Browser gespeichert (localStorage) und nicht übertragen.

## Abhängigkeiten

- [Chart.js 4.4.1](https://www.chartjs.org/) (CDN)
- Schriften IBM Plex Sans / Mono und Barlow Condensed (Google Fonts)

## Hinweise

Strahlungs- und Temperaturwerte der Regionen sind gerundete Mittelwerte; für genaue Ergebnisse die Jahresstrahlung des Standorts aus [PVGIS](https://re.jrc.ec.europa.eu/pvg_tools/) übernehmen. Preise und Wechselrichterdaten sind generische Richtwerte (Stand 11/2026).

Der Rechner dient der Vorplanung und Lehre. Er ersetzt keine Fachplanung nach DIN VDE 0100-712, keine Herstellerauslegung des Wechselrichters und keine statische Prüfung des Daches.
