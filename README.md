# VocabularyTrainer

# 📚 Vokabeltrainer – Englisch ↔ Deutsch

Ein schlanker, vollständig **offline nutzbarer** Vokabeltrainer in einer einzigen HTML-Datei. Vokabeln werden aus Excel (CSV oder Copy & Paste) geladen und in verschiedenen Übungsmodi abgefragt – mit **eindeutiger, regelbasierter Auswertung** (keine KI-Schätzung), Aussprache des englischen Wortes und exportierbaren Ergebnissen.

> **Hinweis:** Nur für den persönlichen Gebrauch – Kontakt: arpyka@hotmail.com

---

## Inhaltsverzeichnis

- [Funktionen](#-funktionen)
- [Schnellstart](#-schnellstart)
- [Bedienung Schritt für Schritt](#-bedienung-schritt-für-schritt)
  - [1. Vokabeln](#1-vokabeln)
  - [2. Quiz-Einstellungen](#2-quiz-einstellungen)
  - [3. Üben](#3-üben)
  - [4. Ergebnisse](#4-ergebnisse)
- [Datenformat (CSV / Excel)](#-datenformat-csv--excel)
- [Regeln für die Auswertung](#-regeln-für-die-auswertung)
- [Aussprache](#-aussprache)
- [Tastaturbedienung](#-tastaturbedienung)
- [Datenschutz](#-datenschutz)
- [Fehlerbehebung (FAQ)](#-fehlerbehebung-faq)
- [Bekannte Einschränkungen](#-bekannte-einschränkungen)

---

## ✨ Funktionen

- **Keine Installation, kein Server** – einfach die HTML-Datei im Browser öffnen.
- **Vokabeln laden** per CSV-Datei (Drag & Drop oder Dateiauswahl) oder direkt aus Excel einfügen.
- **Automatische Validierung** mit Vorschau-Tabelle, Fehlerzählung und markierten Fehlerzeilen.
- **Fünf Übungsmodi:** zufällige Aufgabentypen, Englisch → Deutsch, Deutsch → Englisch, Sätze ergänzen, Übersetzungen eintippen.
- **Kategorien** zum gezielten Üben einzelner Themen.
- **Alternative Antworten** (Synonyme) pro Wort definierbar.
- **Wiederholung** falsch beantworteter Wörter am Ende der Sitzung.
- **Aussprache** des englischen Wortes (britisch oder amerikanisch) über die Sprachausgabe des Browsers.
- **Live-Statistik:** Punktzahl, richtig/falsch, aktuelle und beste Serie.
- **Ergebnis-Export** als CSV.
- **Zweisprachige Oberfläche** (Deutsch/Englisch) per Umschalt-Button.
- **Dark Mode** – passt sich automatisch der Systemeinstellung an.
- **Responsive** – funktioniert auf Desktop, Tablet und Smartphone.

---

## 🚀 Schnellstart

1. Datei `vocabulary_trainer.html` herunterladen.
2. Per Doppelklick in einem aktuellen Browser öffnen (Edge, Chrome, Firefox oder Safari).
3. Beim Start sind bereits **15 Beispielwörter** geladen – du kannst sofort ausprobieren:
   **2. Quiz-Einstellungen** → **Quiz starten**.
4. Für eigene Vokabeln: unter **1. Vokabeln** eine CSV-Datei laden oder Daten aus Excel einfügen.

> 💡 Mit dem Button **English / Deutsch** oben rechts wechselst du die Sprache der Oberfläche.

---

## 🧭 Bedienung Schritt für Schritt

Die App ist in vier Reiter gegliedert, die der Reihe nach durchlaufen werden.

### 1. Vokabeln

Hier werden die Vokabeln geladen und geprüft.

| Aktion | Beschreibung |
|---|---|
| **CSV-Datei hier ablegen** / **CSV auswählen** | Eine aus Excel exportierte CSV-Datei per Drag & Drop oder Dateidialog laden. Nur Dateien mit der Endung `.csv` werden akzeptiert. |
| **Direkt aus Excel einfügen** | Zellen in Excel markieren (inkl. Überschriftenzeile), kopieren und in das Textfeld einfügen. Dann **Eingefügte Daten laden** klicken. |
| **Beispieldaten laden** | Lädt die integrierten Beispielvokabeln erneut. |
| **Leeren** | Entfernt alle geladenen Vokabeln und leert das Textfeld. |
| **CSV-Vorlage herunterladen** | Lädt `vocabulary_template.csv` mit allen unterstützten Spalten und einer Beispielzeile herunter. |

Rechts im Bereich **Validierung** siehst du die Anzahl der **gültigen Wörter** und der **Fehler**. Die Tabelle **Validierte Vokabeln** zeigt alle Zeilen; abgelehnte Zeilen sind rot markiert und nennen den Grund in der Spalte *Status*:

- `Missing English or German value` – Englisch- oder Deutschwert fehlt.
- `Duplicate pair` – das Englisch-Deutsch-Paar ist bereits vorhanden (Groß-/Kleinschreibung wird dabei ignoriert).

### 2. Quiz-Einstellungen

| Einstellung | Optionen | Beschreibung |
|---|---|---|
| **Übungsmodus** | Zufällige Aufgabentypen | Mischt Englisch → Deutsch, Deutsch → Englisch und – wenn möglich – Satzergänzungen (Multiple Choice). |
| | Nur Englisch → Deutsch | Englisches Wort wird gezeigt, deutsche Übersetzung auswählen. |
| | Nur Deutsch → Englisch | Deutsches Wort wird gezeigt, englische Übersetzung auswählen. |
| | Nur Sätze ergänzen | Zwei englische Beispielsätze mit Lücke (`...`) – das fehlende englische Wort auswählen. |
| | Übersetzungen eintippen (gemischt) | Übersetzung frei eintippen; Richtung (EN → DE oder DE → EN) wird pro Frage zufällig gewählt. |
| **Anzahl der Fragen** | 1–100 (Standard: 10) | Wird automatisch auf die Anzahl verfügbarer Wörter begrenzt. |
| **Antwortmöglichkeiten pro Frage** | 2, 3 oder 4 (Standard: 4) | Gilt für Multiple-Choice-Aufgaben. |
| **Kategorie** | Alle Kategorien oder eine einzelne | Fragt nur Wörter der gewählten Kategorie ab. |

Zusätzliche Optionen:

- ☑️ **Falsch beantwortete Wörter am Ende einmal wiederholen** (Standard: an) – jedes falsch beantwortete Wort wird einmal ans Ende der Sitzung angehängt.
- ☐ **Bei eingetippten Antworten Groß- und Kleinschreibung beachten** (Standard: aus).
- ☑️ **Englisches Wort nach einer richtigen Antwort automatisch vorlesen** (Standard: an).

Mit **Quiz starten** beginnt die Übung und die App wechselt automatisch zum Reiter **3. Üben**.

### 3. Üben

- Oben: aktuelle Frage (*Frage X von Y*), aktuelle **Serie** und Fortschrittsbalken.
- **Multiple Choice:** auf die richtige Antwort klicken. Die richtige Antwort wird grün, eine falsche Auswahl rot markiert.
- **Eintippen:** Antwort ins Feld schreiben und **Prüfen** klicken (oder `Enter` drücken).
- Nach jeder Antwort erscheinen:
  - eine Rückmeldung mit dem korrekten Wortpaar,
  - der **Beispielsatz** (Englisch und Deutsch), sofern vorhanden,
  - der Button **🔊 Wort erneut anhören**.
- Bei falscher Antwort ertönt ein kurzer Signalton.
- **Nächste Frage** führt weiter; **Sitzung beenden** bricht ab und zeigt sofort die Ergebnisse.

Rechts zeigt **Aktuelle Sitzung** live: Punktzahl in %, richtig, falsch und beste Serie.

### 4. Ergebnisse

- Übersicht: **Punktzahl**, **richtig**, **falsch**, **beantwortet**.
- Ab 80 % erscheint eine Lob-Nachricht, darunter ein Hinweis zum Wiederholen.
- **Zu wiederholende Wörter:** Liste aller falsch beantworteten Wortpaare.
- **Erneut üben** führt zurück zu den Quiz-Einstellungen.
- **Ergebnisse als CSV exportieren** speichert `vocabulary_results.csv` mit den Spalten:

  `Question, English, German, Direction, English sentence, German sentence, Given answer, Correct`

---

## 📄 Datenformat (CSV / Excel)

### Spalten

| Spalte | Pflicht | Beschreibung |
|---|:---:|---|
| `English` | ✅ | Englisches Wort (auch `Englisch` oder `EN` wird erkannt). |
| `German` | ✅ | Deutsche Übersetzung (auch `Deutsch` oder `DE`). |
| `Accepted English` | – | Weitere zulässige englische Antworten, getrennt durch `\|` oder `/`. |
| `Accepted German` | – | Weitere zulässige deutsche Antworten, getrennt durch `\|` oder `/`. |
| `Category` / `Kategorie` | – | Thema/Kategorie. Ohne Angabe: `General`. |
| `English_Sentence` / `German_Sentence` | – | Beispielsatzpaar. |
| `English_Sentence1` … `English_Sentence3` / `German_Sentence1` … `German_Sentence3` | – | Bis zu drei weitere Beispielsatzpaare. |

**Hinweise:**

- Die erste Zeile muss die **Spaltenüberschriften** enthalten. Groß-/Kleinschreibung, Leer- und Sonderzeichen in den Überschriften spielen keine Rolle.
- Das **Trennzeichen** wird automatisch erkannt: Komma `,`, Semikolon `;` oder Tabulator. Damit funktionieren auch CSV-Exporte aus deutschem Excel (Semikolon).
- Felder, die das Trennzeichen (z. B. ein Komma) enthalten, müssen in **Anführungszeichen** stehen.
- Datei als **CSV UTF-8** speichern, damit Umlaute (ä, ö, ü, ß) korrekt erscheinen.
- Die alternativen Antworten (`Accepted …`) werden nur bei **eingetippten** Antworten berücksichtigt.

### Beispiel

```csv
English,German,Accepted English,Accepted German,Category,English_Sentence,German_Sentence,English_Sentence1,German_Sentence1
window,Fenster,,,House,The window is open.,Das Fenster ist offen.,Open the window.,Öffne das Fenster.
house,Haus,home,,House,,,,
street,Straße,road,Gasse|Weg,Outside,,,,
children (pl),Kinder,,,People,,,,
apartment (AE),Wohnung,flat,,House,,,,
```

### Excel → CSV exportieren

1. In Excel: **Datei** → **Speichern unter** (bzw. **Kopie speichern**).
2. Dateityp **CSV UTF-8 (durch Trennzeichen getrennt) (*.csv)** wählen.
3. Die Datei in der App unter **1. Vokabeln** laden.

### Markierungen im englischen Wort

| Markierung | Bedeutung |
|---|---|
| `(pl)` | Pluralform – wird angezeigt, aber **nicht vorgelesen**. |
| `(AE)` | Amerikanisches Englisch – Aussprache erfolgt mit US-Stimme, Markierung wird nicht vorgelesen. |

---

## ✅ Regeln für die Auswertung

Die Bewertung ist **deterministisch** – die Richtigkeit wird nie durch KI geschätzt.

- Jede Antwort bleibt der zugehörigen Vokabelzeile (ID) zugeordnet.
- Bei Multiple Choice wird zuerst die richtige Antwort festgelegt, danach werden die Antwortmöglichkeiten gemischt. Die falschen Optionen stammen aus derselben Kategorie.
- **Eingetippte Antworten** werden vor dem Vergleich vereinheitlicht:
  - Leerzeichen am Anfang/Ende entfernt, mehrfache Leerzeichen zusammengefasst,
  - Satzzeichen `.`, `!`, `?` **am Ende** ignoriert,
  - Groß-/Kleinschreibung ignoriert (sofern die Option nicht aktiviert ist).
- Als richtig gilt das Hauptwort **oder** eine der zulässigen Alternativen aus `Accepted English` / `Accepted German`.
- **Satzergänzung:** Ein Wort ist nur dafür geeignet, wenn **mindestens zwei** seiner englischen Beispielsätze das Wort als ganzes Wort enthalten. Es werden zwei solcher Sätze mit Lücke gezeigt; nach der Antwort erscheinen beide deutschen Übersetzungen.
- Die Punktzahl ist der Anteil richtiger Antworten an allen beantworteten Fragen (inkl. Wiederholungen).

---

## 🔊 Aussprache

- Nach einer **richtigen** Antwort wird das englische Wort automatisch vorgelesen (abschaltbar in den Einstellungen).
- Nach **jeder** ausgewerteten Antwort kann das Wort mit **🔊 Wort erneut anhören** abgespielt werden.
- Standard ist **britisches Englisch** (`en-GB`); Wörter mit `(AE)` werden **amerikanisch** (`en-US`) ausgesprochen.
- Die Sprechgeschwindigkeit ist leicht reduziert, um das Mitsprechen zu erleichtern.
- Genutzt wird die Sprachausgabe des Browsers bzw. Betriebssystems. Ist keine passende Stimme installiert, nutzt der Browser seine Standardstimme.

---

## ⌨️ Tastaturbedienung

| Taste | Funktion |
|---|---|
| `Enter` (im Eingabefeld) | Antwort prüfen – nach der Auswertung: nächste Frage |
| `Tab` / `Shift + Tab` | Zwischen Buttons und Antwortmöglichkeiten wechseln |
| `Leertaste` / `Enter` (auf Button) | Antwortmöglichkeit oder Button auslösen |

---

## 🔒 Datenschutz

- Die gesamte Verarbeitung erfolgt **lokal im Browser-Tab** – es werden keine Daten an einen Server gesendet.
- Es werden keine Daten dauerhaft gespeichert. **Beim Schließen oder Neuladen der Seite wird die Sitzung gelöscht** (inkl. geladener Vokabeln).
- Tipp: Ergebnisse vor dem Schließen über **Ergebnisse als CSV exportieren** sichern.

---

## ❓ Fehlerbehebung (FAQ)

**„Required columns not found. Use headers English and German.“**
Die Überschriftenzeile fehlt oder die Pflichtspalten heißen anders. Verwende `English` und `German` (oder `Englisch`/`Deutsch`).

**„Please export the Excel sheet as CSV UTF-8 and load that file.“**
Es wurde eine Datei geladen, die nicht auf `.csv` endet (z. B. `.xlsx`). Die Tabelle zuerst als CSV UTF-8 speichern.

**Umlaute werden falsch angezeigt (z. B. `Ã¼` statt `ü`).**
Die CSV wurde nicht als UTF-8 gespeichert. In Excel den Dateityp **CSV UTF-8** wählen.

**„This mode needs at least N words in the selected category.“**
Für Multiple Choice werden mindestens so viele Wörter benötigt, wie Antwortmöglichkeiten eingestellt sind. Mehr Wörter laden, eine andere Kategorie wählen oder die Anzahl der Antwortmöglichkeiten verringern. Der Modus *Übersetzungen eintippen* hat diese Einschränkung nicht.

**„Keine geeigneten Satzergänzungsaufgaben gefunden.“**
Für den Modus *Nur Sätze ergänzen* braucht ein Wort mindestens zwei englische Beispielsätze, die das Wort exakt enthalten (z. B. `window` in „The **window** is open.“ – aber nicht in „The windows are open.“).

**Es werden weniger Fragen gestellt als eingestellt.**
Jedes Wort wird pro Sitzung nur einmal abgefragt (zzgl. Wiederholungen). Bei weniger Wörtern in der Kategorie wird die Anzahl entsprechend begrenzt.

**Es ist kein Ton zu hören.**
Lautstärke prüfen, die Option „Englisches Wort … automatisch vorlesen“ aktivieren und sicherstellen, dass das Betriebssystem eine englische Stimme installiert hat (Windows: *Einstellungen → Zeit und Sprache → Sprache*).

---

## ⚠️ Bekannte Einschränkungen

- Einige System- und Fehlermeldungen erscheinen unabhängig von der gewählten Oberflächensprache auf Englisch.
- Der Hinweistext „mindestens vier gültige Zeilen“ bezieht sich auf die Standardeinstellung von 4 Antwortmöglichkeiten; tatsächlich richtet sich das Minimum nach der eingestellten Anzahl (2–4).
- Excel-Dateien (`.xlsx`) können nicht direkt geladen werden – bitte als CSV exportieren oder per Copy & Paste einfügen.
- Kein dauerhafter Lernfortschritt: Jede Sitzung startet neu.

---

## 🛠️ Technik

- Eine einzige, eigenständige HTML-Datei (HTML, CSS, JavaScript) ohne externe Abhängigkeiten.
- Sprachausgabe über die **Web Speech API** (`speechSynthesis`), Signalton über die **Web Audio API**.
- Läuft in aktuellen Browsern (Edge, Chrome, Firefox, Safari); die verfügbaren Stimmen für die Aussprache hängen vom Betriebssystem ab.

---

## 📬 Kontakt & Nutzung

Nur für den persönlichen Gebrauch. Fragen oder Anregungen: **arpyka@hotmail.com**
