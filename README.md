# 🍎 Öpfelmeister

Ein kleines Browserspiel über versteckte Datenerhebung. Die Spielenden helfen einer Thurgauer Mosterei beim Ernten, Sortieren und Halbieren von Äpfeln. Nebenbei misst das Spiel Reaktionszeiten, Schnittrichtungen und Entscheidungen und leitet daraus ein Profil ab: Alter, Händigkeit, Standort, Farbsehen und mehr. Am Schluss wird aufgedeckt, was das Spiel über die Person «weiss» und wie wacklig diese Schlüsse sind.

Das Spiel ist als Einstieg in Lehrveranstaltungen und Weiterbildungen zu Datenschutz, Tracking und Dark Patterns gedacht. Zielgruppe sind Studierende und Lehrpersonen.

## Entstehung

Öpfelmeister ist inspiriert vom Spiel «CheeseMaster» aus der SRF-Serie «Dataland», das zeigte, was ein harmloses Käsespiel über seine Spielerinnen und Spieler preisgibt ([Artikel auf srf.ch](https://www.srf.ch/news/schweiz/dataland-schweiz-cheesemaster-was-ein-harmloses-kaese-spiel-ueber-sie-preisgibt)). Weil das Originalspiel nicht mehr verfügbar ist, haben wir uns erlaubt, eine ähnliche Version nachzubauen. Sie soll sichtbar machen, welche Daten beim Spielen unbemerkt erhoben und ausgewertet werden können. Gestaltung, Texte und Programmierung sind eigenständig. Öpfelmeister ist kein Angebot von SRF.

## Die Stationen

| Station | Was man tut | Was gemessen wird | Was daraus abgeleitet wird |
|---|---|---|---|
| Nutzungsbedingungen | zustimmen | ob sie geöffnet und bis zum Ende gelesen wurden | Leseverhalten |
| Ernten | gute Äpfel antippen, faule hängen lassen | Reaktionszeit, Fehlgriffe | Alter, Impulskontrolle |
| Marketing | Standort angeben, Apfelquiz | Standort, Antwortzeit pro Frage | Wohnort, Entscheidungsstil |
| Halbieren | Äpfel mit einem Wisch teilen | Richtung und Schräge des Schnitts | Händigkeit |
| Qualitätskontrolle | Äpfel nach Kleber sortieren | Umgang mit rot-grünen Klebern | Hinweis auf Rot-Grün-Sehschwäche |
| nebenbei | nichts | Gerät, Browser, Bildschirm, Sprache, Zeitzone, Akku, Tab-Wechsel, Mausweg u. a. | technisches Profil |

In der Auswertung beurteilen die Spielenden jede Annahme mit «stimmt» oder «stimmt nicht». Eine Bilanz zählt mit, wie viele Annahmen falsch waren. Dazu kommen vier Reflexionsfragen für die Diskussion.

## Datenschutz

Das Spiel speichert nichts und sendet nichts. Es gibt keine Cookies, kein localStorage, kein Tracking und keine externen Ressourcen wie Fonts oder Bibliotheken. Alle Daten liegen nur im Arbeitsspeicher des Browser-Tabs und sind weg, sobald er geschlossen wird. Der Webserver sieht wie bei jeder Webseite die IP-Adresse der Besuchenden. Das wird in der Auswertung auch so erklärt.

## Einsatz in der Lehre

1. Link verteilen, ohne zu verraten, worum es geht. «Spielt das mal kurz durch» reicht.
2. Etwa fünf Minuten spielen lassen, am besten auf dem eigenen Smartphone.
3. Die Auswertung lesen und die Annahmen beurteilen lassen.
4. Im Plenum über die Reflexionsfragen sprechen: Was hat überrascht, was war falsch, wo begegnen uns solche Messungen im Alltag und in Lern-Apps?

Die Standortfreigabe funktioniert nur über https, also auf der veröffentlichten Seite. Lokal geöffnet oder in einer eingebetteten Vorschau ist sie meist blockiert. Für diesen Fall gibt es die Karte als Alternative.

## Veröffentlichen mit GitHub und Vercel

Das Projekt besteht aus einer einzigen Datei (`index.html`) und braucht keinen Build-Schritt.

1. Neues Repository auf GitHub anlegen und `index.html` sowie `README.md` hochladen.
2. Auf [vercel.com](https://vercel.com) «Add New → Project» wählen und das Repository importieren.
3. Bei «Framework Preset» die Option «Other» lassen, Build- und Output-Einstellungen leer lassen.
4. «Deploy» klicken. Jeder neue Commit auf GitHub wird danach automatisch veröffentlicht.

Alternativ läuft die Datei auch auf GitHub Pages oder jedem anderen statischen Hosting.

## Anpassen

Alles steckt im `<script>`-Teil von `index.html`:

- `POOL`: Fragenkatalog für das Quiz (30 Fragen, pro Durchgang werden 4 zufällig gezogen)
- `quiz()`: Regionalfrage, die sich nach dem Standort richtet
- `THURGAU`: Orte, bei denen die Thurgau-Variante der Regionalfrage erscheint
- `CITIES`, `BORDER`, `LAKES`: Orte, Landesgrenze und Seen der Karte (Längen- und Breitengrade, vereinfacht)
- `harvestOrder()`: Verhältnis von guten und faulen Äpfeln beim Ernten
- `analyse()`: Schwellenwerte und Texte der Auswertung

## Grenzen

Die Ableitungen sind absichtlich einfach gebaut und für einzelne Personen oft falsch. Die Altersformel ist eine grobe Faustregel, der Farbtest ist kein medizinischer Test und die Händigkeit lässt sich mit Maus oder Trackpad kaum bestimmen. Genau das ist Teil des Lerneffekts: Auch falsche Profile werden in der Praxis weiterverwendet.

## Impressum

Sabrina Meier  
Dozentin Medien und Informatik  
Co-Leiterin Fachstelle Schule und Digitalität  
Pädagogische Hochschule Thurgau  
Unterer Schulweg 3, CH-8280 Kreuzlingen  
sabrina.meier@phtg.ch

Das Impressum mit Datenschutzhinweisen ist auch im Spiel verlinkt (Fusszeile).

## Lizenz

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de). Du darfst das Spiel frei nutzen, verändern und weitergeben, auch in eigenen Kursen, solange du die Urheberin nennst und angibst, ob du etwas geändert hast.

Vorgeschlagene Namensnennung: «Öpfelmeister» von Sabrina Meier, PH Thurgau, CC BY 4.0
