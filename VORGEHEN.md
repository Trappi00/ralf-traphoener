# Wie die Website entstanden ist

Diese Notiz beschreibt in einfachen Worten, wie die Website für Ralf Traphöner
(Handelsagentur für Möbel) gebaut und veröffentlicht wurde – und wie man sie
später weiter pflegen kann.

## Kurzüberblick

- **Live-Seite:** https://trappi00.github.io/ralf-traphoener/
- **Quelldateien (Repository):** https://github.com/Trappi00/ralf-traphoener
- **Kosten:** 0 € (Hosting über GitHub Pages ist kostenlos)
- **Technik:** eine einzelne HTML-Datei (`index.html`) mit eingebautem Design,
  keine Datenbank, kein Server, den man verwalten müsste

## Schritt 1 – Inhalte gesammelt

Als Ausgangspunkt diente eine bestehende, einfache Visitenkarten-Seite
(erstellt mit Canva). Daraus wurden die wichtigsten Informationen übernommen:

- Name: Ralf Traphöner
- Tätigkeit: Handelsagentur für Möbel
- Kontakt: E-Mail und Telefonnummer
- Vertretene Marken: Nova mobili, Cinquanta 3, Dietsch, La vida

## Schritt 2 – Website gestaltet

Aus diesen Informationen wurde eine neue, eigenständige Website als **eine
einzige HTML-Datei** gebaut (`index.html`). Sie enthält:

- eine Startseite mit Vorstellung
- einen Abschnitt "Über mich"
- eine Übersicht der vertretenen Marken (mit Links zu den Herstellern)
- einen Kontaktbereich mit E-Mail und Telefonnummer

Fotos waren zunächst **Platzhalter** – Design und Aufbau standen zuerst,
echte Bilder wurden danach ergänzt (siehe Schritt 7).

## Schritt 3 – Werkzeuge eingerichtet

Um die Datei später öffentlich sichtbar zu machen, wurden zwei Programme
auf dem Rechner eingerichtet:

- **Git** – ein Werkzeug, das Änderungen an Dateien nachverfolgt (war
  bereits auf dem Rechner vorhanden)
- **GitHub CLI (`gh`)** – ein Werkzeug, um mit dem Online-Dienst GitHub zu
  kommunizieren (wurde neu installiert, ohne dass dafür Systemrechte nötig
  waren)

## Schritt 4 – Bei GitHub angemeldet

GitHub ist ein kostenloser Online-Dienst, auf dem Dateien gespeichert und
veröffentlicht werden können. Die Anmeldung erfolgte über einen sicheren
Code-Login im Browser: GitHub zeigte einen einmaligen Code, der auf
github.com/login/device bestätigt wurde. Zugangsdaten wurden dabei nie an
Dritte weitergegeben.

## Schritt 5 – Repository erstellt und Datei hochgeladen

Ein sogenanntes **Repository** (ein Online-Ordner für Projektdateien) wurde
unter dem Namen `ralf-traphoener` erstellt und öffentlich gestellt. Die
`index.html`-Datei wurde dorthin hochgeladen ("gepusht").

## Schritt 6 – GitHub Pages aktiviert

Über eine Funktion namens **GitHub Pages** wurde festgelegt, dass der
Inhalt des Repositorys als echte Website im Internet angezeigt wird.
Wenige Minuten später war die Seite unter

**https://trappi00.github.io/ralf-traphoener/**

erreichbar.

## Schritt 7 – Modernes Design mit echten Bildern

Die Seite wurde zu einer moderneren Landingpage weiterentwickelt: großes
Titelbild, ein durchlaufendes Marken-Band und Bildkacheln für jede
vertretene Marke. Als Platzhalter dienen aktuell lizenzfreie Fotos
(Unsplash) in einem warmen, stimmigen Stil – sie lassen sich jederzeit
gegen echte Fotos von Ralf Traphöner oder seinen Ausstellungsräumen
austauschen.

Zusätzlich wurden zwei feine Detailverbesserungen eingebaut:

- **Mobiles Menü:** Auf dem Smartphone erscheint statt der Navigation ein
  Hamburger-Symbol; ein Tipp darauf öffnet ein sauberes Dropdown-Menü.
- **Scroll-Animationen:** Abschnitte wie "Über mich", die Markenkacheln
  und der Kontaktbereich blenden sanft ein, sobald man beim Scrollen zu
  ihnen kommt (respektiert dabei die "Bewegung reduzieren"-Einstellung
  des Betriebssystems).

## Schritt 8 – Design-Feedback umgesetzt

Nach Rückmeldung von Ralf wurden zwei Anpassungen vorgenommen:

- **Markenstruktur korrigiert:** Nova mobili und Cinquanta 3 sind Kollektionen
  der **Battistella Company** (bestätigt über die offiziellen Websites der
  beiden Marken). Sie werden jetzt gemeinsam als eine Marke "Battistella
  Company" mit zwei verlinkten Kollektionen dargestellt, statt als zwei
  getrennte Marken.
- **Dunkles, moodiges Design:** Auf Wunsch wurde die Seite stilistisch an
  [miedl.at](https://www.miedl.at) angelehnt (nicht kopiert) – dunkler
  Hintergrund, helle/goldene Akzentfarbe, sowie animierte Zahlen im
  "Über mich"-Bereich (z.B. Anzahl vertretener Marken), die beim Scrollen
  hochzählen.

## Schritt 9 – Rechtliche Pflichtangaben ergänzt

Da die Seite von einem gewerblichen Handelsvertreter betrieben wird, gelten
rechtliche Mindestanforderungen. Ergänzt wurden:

- **Impressum** (`impressum.html`) gemäß § 5 DDG
- **Datenschutzerklärung** (`datenschutz.html`) gemäß Art. 13 DSGVO
- Beide Seiten sind im Footer der Startseite verlinkt

Außerdem wurde ein verstecktes DSGVO-Risiko behoben: Die Seite lud zuvor
Schriftarten direkt von Google-Servern, wodurch die IP-Adresse jedes
Besuchers ohne Einwilligung an Google (USA) übertragen wurde – ein in
Deutschland vielfach abgemahntes Problem. Die Schriften werden jetzt
**selbst gehostet** (`fonts/`-Ordner), es findet keine Verbindung zu Google
mehr statt.

**Wichtig – noch offen:** Im Impressum fehlen die vollständige Postanschrift
(Straße, PLZ, Ort) sowie ggf. die Umsatzsteuer-Identifikationsnummer. Diese
sind gesetzlich zwingend erforderlich und aktuell als gelb markierte
Platzhalter im Impressum sichtbar. Die Seite sollte nicht dauerhaft ohne
diese Angaben online bleiben, da ein unvollständiges Impressum abmahnfähig
ist. Rechtssicherheit im Detail sollte im Zweifel mit einem Anwalt oder
Steuerberater abgestimmt werden – diese Umsetzung ersetzt keine
Rechtsberatung.

## Wie man die Seite später aktualisiert

Jede Änderung läuft nach demselben Prinzip:

1. Die Datei `index.html` bearbeiten (Texte, Bilder, Kontaktdaten).
2. Die Änderung "committen" (speichern mit einer kurzen Beschreibung).
3. Die Änderung "pushen" (zu GitHub hochladen).

Rund eine Minute später ist die Änderung automatisch auf der Live-Seite
sichtbar. Das kann entweder direkt im Browser über die GitHub-Oberfläche
passieren (Datei anklicken → Stift-Symbol → bearbeiten → speichern) oder
lokal auf dem Rechner mit Unterstützung.

## Kurzes Glossar

| Begriff | Bedeutung |
|---|---|
| **Repository ("Repo")** | Ein Online-Ordner für die Projektdateien, inklusive alter Versionen |
| **Git** | Das Werkzeug, das Änderungen an Dateien nachvollziehbar speichert |
| **Commit** | Ein gespeicherter Änderungsstand mit kurzer Beschreibung |
| **Push** | Änderungen vom eigenen Rechner zu GitHub hochladen |
| **GitHub Pages** | Kostenloser Hosting-Dienst, der ein Repository als Website veröffentlicht |
| **Hosting** | Der Vorgang, eine Website dauerhaft im Internet erreichbar zu machen |

## Wichtige Links

- Live-Website: https://trappi00.github.io/ralf-traphoener/
- Projektdateien auf GitHub: https://github.com/Trappi00/ralf-traphoener
- GitHub-Konto: Trappi00
