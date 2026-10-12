# CHANGELOG — eInvoice Viewer ( App )

Die Fassungsnummer dieses App-Pakets steht **nur hier**. `build-package.mjs` liest sie von hier,
`check-app-package.php` prüft sie, und der ZIP-Name entsteht daraus.

⚠️ **Eine zweite Stelle läuft auseinander.** Die Nummer in `index.html`, `config.js` oder im
Dateinamen zu wiederholen heisst, sie beim nächsten Mal an einer davon zu vergessen — und gemerkt
wird es beim Kunden.

⚠️ **Das ist nicht die Fassung des Plugins.** `einvoice-viewer-for-peppol-en16931` steht bei 2.17.x
und zählt seine eigene Reihe; dieses Paket ist eine andere Auslieferungsform desselben Werkzeugs und
beginnt bei 1.0.0.

---

## 1.10.0 — 2026-10-11

- Jedes Bankkonto und jedes Zahlungsmittel der Rechnung wird angezeigt, nicht nur das erste.
- Der Hinweiskasten über markierten Feldern nennt jetzt, was der Viewer prüft: die Pflichtfelder, die
  Regeln der Umsatzsteuer-Kategorien, die Reihenfolge der Daten, die Prüfziffer der IBAN und ob die
  Summen aufgehen.

## 1.9.0 — 2026-10-09

- Bei einer UBL-Rechnung erscheinen jetzt Felder, die bisher immer leer blieben, darunter die
  Spezifikationskennung, der Zahlungsempfänger, der Steuerbevollmächtigte des Verkäufers, das Datum
  der Steuerfälligkeit, die Gläubiger-Kennung und die Bemerkungen zur Rechnung.
- Der Geschäftsprozesstyp der Rechnung wird jetzt angezeigt, bei UBL und bei CII.
- Die Daten einer UBL-Rechnung stehen in der Schreibweise der eingestellten Sprache.
- Ein Bruttopreis, eine Basismenge, der Grundbetrag oder Prozentsatz eines Zu- oder Abschlags oder
  ein Steuersatz, den die Rechnung nicht nennt, bleibt leer, statt 0 zu zeigen.
- Eine Rechnung nach EXTENDED-CTC-FR wird in der Zeile über der Rechnung beim Namen genannt.
- Die Seite des Ordners heisst jetzt `einvoice-viewer.html`; `index.html` führt nur noch dorthin
  weiter. Das ZIP enthält keine Einzeldateien mehr.
- Die App gibt auch eine UBL-Rechnung an den Zusatz „Extended Profiles“ weiter. Die Angaben der
  XRechnung Extension zeigt erst eine kommende Fassung des Zusatzes; mit der heutigen bleibt die
  Ansicht, wie sie war.

## 1.8.0 — 2026-10-08

- Verletzt ein Feld eine Regel, die aus der Rechnung selbst folgt, etwa ein fehlendes Pflichtfeld, eine
  Regel seiner Umsatzsteuerkategorie, ein Fälligkeitsdatum vor dem Rechnungsdatum oder eine falsche
  IBAN, ist das Feld rot markiert und trägt einen Hinweis. Ein Kasten über der Rechnung sagt, dass das
  Hinweise und keine vollständige Prüfung sind.
- Der Knopf „Zurücksetzen“ folgt dem Design-Kit.
- Die Kurzanleitungen sagen, was die Ansicht zeigt und was nicht.

## 1.7.0 — 2026-10-08

- Vergabenummer und Objektkennung stehen jetzt mit dem Schema der Objektkennung unter den Bestell- und
  Vertragsdaten und nicht mehr als rechnungsbegründende Unterlagen.
- Der Steuerbetrag in Buchungswährung wird an seiner Währung erkannt und nicht mehr an seiner Stellung,
  und der Rechenhinweis unter dem Gesamtbetrag nennt den richtigen Betrag.

## 1.6.1 — 2026-10-08

- Mit dem Zusatz „Extended Profiles“ erscheinen die Karten der Erweiterung in der eingestellten
  Sprache statt immer englisch. Dafür ist die Fassung 1.1.1 des Zusatzes nötig.

## 1.6.0 — 2026-10-08

- Mit dem Zusatz „Extended Profiles“ im Ordner zeigt eine EXTENDED-Rechnung zusätzliche Karten mit den
  Angaben der Erweiterung: weitere Handelsparteien, Dokumentkennzeichen, Skonto und Verzugszinsen sowie
  weitere Referenzen. Die Felder der Erweiterung tragen ihren Namen im Tooltip.
- Ohne den Zusatz steht unter einer solchen Rechnung ein Hinweis, dass sie eine Erweiterung benutzt.
  Die Kernfelder werden weiterhin vollständig gezeigt.

## 1.5.0 — 2026-10-08

- Die Karten „Rechnungsbegründende Unterlagen“ innerhalb der Rechnung entfallen. Dieselben Anlagen
  stehen im Abschnitt „Anlagen“ unter der Rechnung, und dort stehen sie nur noch einmal.

## 1.4.0 — 2026-10-08

- Unter der Rechnung steht ein Abschnitt „Anlagen“ mit Kennung, Beschreibung, Dateiname, Dateityp und
  Größe jeder Anlage. Eine PDF oder ein Bild lässt sich dort ansehen, und jede Anlage eines der sechs
  erlaubten Typen lässt sich speichern.

## 1.3.0 — 2026-10-08

- Geht ein Betrag der Rechnung nicht aus seinen Teilen auf, ist das Feld rot markiert, und darunter
  steht der ausgewiesene und der nachgerechnete Betrag, etwa „Ausgewiesen 39,62 EUR, gerechnet
  37,62 EUR.“ Der Wert aus der Rechnung bleibt dabei unverändert stehen.

## 1.2.2 — 2026-10-08

- In `config.js` gibt es kein Feld für einen Lizenzschlüssel mehr. Ein gekaufter Zusatz liegt
  künftig als eigener Ordner neben der App, statt über einen Schlüssel freigeschaltet zu werden.
- Summen, die die Rechnung nicht nennt, erscheinen leer statt als 0,00.
- Die mitgelieferten Felddaten sind auf dem Stand vom 08.10.2026.

---

## 1.2.1 — 2026-10-07

- Die Ablagefläche kommt aus dem Gestaltungskit 1.5 und sieht in jedem Werkzeug der Reihe gleich
  aus. Die Formatnamen PDF und XML stehen weiter als Marken im Hinweissatz.

## 1.2.0 — 2026-10-07

- **Beide Formen liegen im ZIP.** Neben dem Ordner `einvoice-viewer/` stehen drei Einzeldateien:
  `einvoice-viewer.de.html`, `einvoice-viewer.en.html` und `einvoice-viewer.fr.html`. Jede ist das
  ganze Werkzeug in einer Datei und in einer Sprache, zum Weitergeben per Mail oder auf einem Stick.
- **Die Belegansicht sieht aus wie ein Beleg.** Jede Business Group steht in einem Block, dessen Name
  als Fahne oben links auf dem Rahmen sitzt — dunkel mit Werten, hell ohne. Die Beschriftung steht
  links, der Wert rechts in einem hellblauen Feld; ein breiter Block zeigt zwei Feldzeilen
  nebeneinander. Der Haftungshinweis ist gelb.
- **Die Positionsgruppen heissen auf Deutsch „Position" und auf Französisch „Ligne"**, nicht mehr
  „Item".
- **Eine eingebettete Ansicht hat ihre Farben, auch ohne dass die umgebende Seite das Kit lädt.** Das
  Element bekommt dafür über `data-css` drei Dateien: das Stylesheet des Werkzeugs,
  `assets/css/kit-h.tokens.css` und `assets/css/kit-h.css`. `examples/embed.html` zeigt es.

---

## 1.1.0 — 2026-10-06

- **Die Einzeldatei kann jetzt dieselben Sprachen wie das Ordnerpaket.** Die Sprachtabellen sind in
  `index.html` eingebettet, statt dort zu fehlen. Bis dahin trug die Datei zwar die französischen
  Feldbeschriftungen, ihre Knöpfe und Meldungen blieben aber englisch.
- Die Zahlen- und Datumsschreibweise folgt der eingestellten Sprache: deutsche Tausenderpunkte und
  Dezimalkommas, französische schmale Leerzeichen, englische Schreibweise mit Punkt als
  Dezimaltrenner.
- Fehlt eine Übersetzung, erscheint durchgehend der englische Originaltext statt einer teilweise
  übersetzten Seite.
- Der Fremdwährungsbetrag der Steuer ( BT-111 ) wird angezeigt, wenn der Beleg ihn trägt.

---

## 1.0.0 — 2026-10-06

Erstes App-Paket nach dem Aufbau aus `apps/docs/app-paket.md` ( ToDo P1.3 ).

- Ordnerpaket statt Einzeldatei: `index.html`, `einvoice-viewer.js`, `app.js`, `config.js`,
  `assets/`, `data/`, `examples/embed.html`, drei Kurzanleitungen, `LICENSE`.
- Die Kataloge liegen als Skriptdateien in `data/` und tragen sich selbst ein. Aus `file://` kann
  `fetch` den Nachbarordner nicht lesen; `<script src>` dagegen schon.
- Die Schriften liegen bei ( `assets/fonts/`, 20 Dateien, 420,1 KB ) und werden **ab Werk von dort
  geladen** — `fontsLocal: true`. Damit macht das Paket in seiner Voreinstellung keinen einzigen
  Abruf nach aussen. Wer den gemeinsamen Cache von Google Fonts nutzen will, setzt den Schalter auf
  `false`; die Adresse steht im Schriftlader bereit.
- `config.js` mit `lang`, `dataSource`, `onlineUpdates`, `fontsLocal`, `licenseKey`, `serviceUrl`,
  `allowedProfiles`. Vorgabe `dataSource: 'local'` und `fontsLocal: true` — beides so, dass das Paket
  im Intranet, in SharePoint oder von der Festplatte ohne Netz vollständig arbeitet.
- Das Einbettungspaket ( `embed/`, 05.10.2026 ) ist hierin aufgegangen.

Die Einzeldatei bleibt: `node build.mjs` baut sie weiter, und sie ist das Ding, das man per E-Mail
weitergibt.
