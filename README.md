# Umfrage zum Schulklima, Mobbing und Gewalt

Ein umfassendes, anonymes Umfrage- und Analysesystem zur Bewertung von Mobbing, Gewalt und Schulklima für Schülerinnen und Schüler der Klassenstufen 5 bis 12. Durchgeführt an einer deutschen Gesamtschule, um Muster von physischer, verbaler und Cybergewalt zu identifizieren und institutionelle Unterstützungsstrukturen zu bewerten.

## Studiendesign

* **Zielgruppe:** Schülerinnen und Schüler der Klassen 5–12
* **Methode:** Anonymer Online-Fragebogen (Plattform: Tally)
* **Sprache:** Deutsch
* **Antwortformat:** Multiple-Choice, Likert-Skalen (1–5) und Freitextfelder

## Struktur der Umfrage

Der Fragebogen besteht aus 42 strukturierten Fragen in acht Themenbereichen:

**Demografie (2 Fragen)**

- Klassenstufe (5–12)
- Geschlechtsidentität (weiblich, männlich, divers)

**Wohlbefinden & Klassenklima (4 Fragen)**
Bewertung von Peer-Beziehungen, Respekt, Zugehörigkeit und Sicherheit innerhalb der Klasse mittels 5-stufiger Likert-Skalen.

**Schule & Lehrkräfte (4 Fragen)**
Wahrnehmung der Fairness von Lehrkräften, Vertrauen, Fürsorge und allgemeine Zufriedenheit mit der Schule.

**Familie & Freunde (4 Fragen)**
Bewertung von Unterstützungssystemen außerhalb der Schule, einschließlich familiärer Akzeptanz und vertrauensvoller Freundschaften.

**Gewalterfahrungen (15 Fragen)**
Detaillierte Erfassung von drei Gewaltformen:

- Physische Gewalt: Häufigkeit, Formen (Schlagen, Drohungen, Sachbeschädigung), Dauer
- Verbale/soziale Gewalt: Häufigkeit, Formen (Beleidigungen, Ausschluss, Gerüchte), Dauer
- Cybermobbing: Häufigkeit, Formen (Online-Belästigung, Drohungen, Teilen von Bildern), Dauer

_Bedingte Logik: Folgefragen erscheinen nur, wenn Schüler angeben, Gewalt erfahren zu haben._

**Tätercharakteristika (4 Fragen)**
Anzahl der Täter, Beziehung zu Gleichaltrigen, Abwehrreaktionen, Häufigkeit von Beobachtungen.

**Kontext der Vorfälle (2 Fragen)**
Orte (Klassenzimmer, Schulhof, Flure, Toiletten, Online, Schulweg) und Zeitpunkt (während des Unterrichts, in den Pausen, vor/nach der Schule).

**Intervention & Unterstützung (7 Fragen)**

- Bereitschaft zum Eingreifen (Skala 1–5)
- Gefühle und frühere Reaktionen von Beobachtern
- Kenntnis von Ansprechpartnern
- Bevorzugte Hilfsangebote (Vertrauenslehrer, Klassenlehrer, Freunde, Familie, Helpline)

**Wahrnehmungen & Motive (5 Fragen)**

- Wahrgenommene Motive für Mobbing (Geld, Kleidung, Aussehen, Verhalten, Rivalität, Herkunft/Religion/Hautfarbe)
- Wahrnehmung der Aufmerksamkeit und Intervention durch Lehrkräfte
- Dynamik der Unterstützung durch Mitschüler
- Wahrnehmung der Unterstützung durch die Gemeinschaft

**Selbstreflexion (2 Fragen)**
Anonyme Selbstauskunft über eigenes Mobbingverhalten und Motive (Wut, Notwendigkeit, Spaß, Vergeltung).

**Offenes Feedback (1 Frage)**
Freitextfeld für zusätzliche Gedanken, Erfahrungen und Vorschläge.

---

## Datenanalyse

Eine in Python (Jupyter Notebook) implementierte automatisierte Analyse-Pipeline verarbeitet die Umfrageergebnisse zur Erstellung umfassender Berichte.

**Berechnete Kennzahlen:**

_Prävalenzraten_

- Opfer physischer Gewalt: Prozentsatz derer, die in den letzten 6 Monaten physische Gewalt erfahren haben.
- Opfer verbaler/sozialer Gewalt: Prozentsatz derer, die Beleidigungen, Ausschluss oder Gerüchte erfahren haben.
- Opfer von Cybermobbing: Prozentsatz derer, die Online-Belästigung erfahren haben.
- Chronische Opfer: Schüler, die seit mehr als 6 Monaten Gewalt erleben.
- Täter: Häufigkeit des selbstdokumentierten Mobbingverhaltens.
- Täter-Opfer: Schüler, die sowohl Täter als auch Opfer sind.
- Reine Opfer: Opfer, die selbst kein Mobbing ausüben.

_Demografische Auswertungen_

- Gewaltprävalenz nach Klassenstufe und Geschlecht.
- Altersbedingte Trends bei den Gewaltformen.

_Täteranalyse_

- Mobbingmuster (Gruppe vs. Einzelpersonen).
- Interne (Mitschüler) vs. externe Täter.
- Anzahl der Täter pro Vorfall.

_Ort & Zeitpunkt_

- Häufigste Tatorte (Ranking).
- Spitzenzeiten der Vorfälle.

_Unterstützungssysteme_

- Bekanntheitsgrad von Hilfsangeboten.
- Verteilung der bevorzugten Ansprechpartner.
- Tatsächliches Hilfesuchverhalten der Opfer.
- Anteil der Opfer, die keine Hilfe erhalten.

_Effektivität der Lehrkräfte_

- Wahrgenommene Aufmerksamkeit und Interventionsgüte der Lehrer.
- Vertrauen der Schüler in das Lehrpersonal und Fairness-Bewertungen.

_Schutzfaktoren_

- Freundschaftsqualität in der Klasse und familiäre Akzeptanz.
- Korrelationsanalyse zwischen Schutzfaktoren und Gewaltbelastung.

_Zuschauerverhalten (Bystander)_

- Beobachtungshäufigkeit und Interventionsbereitschaft.
- Emotionale Reaktionen beim Beobachten von Mobbing.

---

## Analyse-Workflow

1. **Datenimport**: Laden des CSV-Exports von der Tally-Plattform.
2. **Datenbereinigung**: Umgang mit fehlenden Werten, Standardisierung der Kategorien.
3. **Demografisches Profiling**: Berechnung der Rücklaufquoten und Verteilungen.
4. **Gewaltprävalenz**: Berechnung der Statistiken für alle Gewaltarten.
5. **Musteranalyse**: Identifikation von Trends über Demografie, Orte und Zeiten hinweg.
6. **Evaluierung der Unterstützung**: Bewertung des Hilfesuchverhaltens.
7. **Korrelationsanalyse**: Untersuchung des Zusammenhangs zwischen Wohlbefinden und Gewalt.
8. **Visualisierung**: Erstellung von Diagrammen für die Kernergebnisse.
9. **Berichtserstellung**: Generierung eines umfassenden PDF-Berichts.

## Technisches & Datenschutz

**Anforderungen:**

- **Python-Bibliotheken:** pandas, matplotlib, seaborn, numpy, fpdf/reportlab.
- **Umgebung:** Google Colab, lokales Jupyter Notebook oder VSCode.

**Datenschutz & Ethik:**

- Vollständig anonyme Datenerhebung (keine personenbezogenen Daten).
- Freiwillige Teilnahme mit informierter Einwilligung.
- Bereitstellung von Hilfsressourcen am Ende der Umfrage.
- Ausschließlich aggregierte Daten (keine Rückschlüsse auf Einzelpersonen).

---

## Projektorganisation

Dieses Projekt wurde von der **Schülervertretung (SV)** initiiert und verwaltet, um Mobbing- und Gewaltprobleme innerhalb der Schulgemeinschaft besser zu verstehen und anzugehen, maßgeblich umgesetzt durch JohanGrims.
