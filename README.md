# Reset Watch

Ein unabhängiges, deutschsprachiges Observatorium für außerplanmäßige kostenlose Claude-Nutzungslimit-Resets und Modellveröffentlichungen. Ein Projekt von Ruwens Instinct. Nicht von Anthropic.

## Was die Seite beantwortet

- Welche Zusatz-Resets wurden öffentlich bestätigt, für welche Tarife und bis wann?
- Gibt es belastbare Hinweise auf einen weiteren Reset oder Modellstart?
- Welche früheren Ereignisse sind dokumentiert, und wie gut sind sie belegt?

Ein Modellstart kann ein Anlass für Resets sein. Ein automatischer Zusammenhang oder ein verlässlicher Zeitplan ist nicht belegt. Die Seite erfindet keine Prozentwerte. Reguläre Quotenzyklen sind keine Sonder-Resets.

## Betrieb und tägliche Analyse

Die tägliche redaktionelle Recherche läuft morgens in der Zeitzone Europe/Berlin. Sie prüft öffentliche Originalankündigungen, offizielle Hilfeseiten, Release-Notizen und unabhängige Hinweise. Es gibt keine privaten Claude-Kontoabfragen und keine automatische Reset-Einlösung. Der betreibende Assistent pflegt `data.json`; GitHub Pages veröffentlicht die Website aus `main`, Verzeichnis `/`.

Ein neuer Zeitstempel wird nur nach echter Recherche gesetzt, nicht durch einen simplen Cron-Touch. Ein Quellencheck allein ist keine neue Analyse. Neue Angebote werden nur nach Prüfung von Zielgruppe, Wirkung und Ablauf als bestätigt geführt. Ein Reset kann im individuellen Konto bereits verbraucht sein. Das kann diese Website nicht sehen.

Nach 36 Stunden ohne neue Analyse zeigt die Website einen Warnhinweis. Ablaufzeiten werden beim Laden zusätzlich gegen die aktuelle Uhrzeit geprüft. Der Betrieb ist ohne bezahlte APIs und ohne Secrets im Repository angelegt. Es gibt bewusst keinen automatischen Scraper, der aus Stichwörtern ungeprüft einen Reset als verfügbar ausgibt.

## Dateien

- `index.html`: vollständige responsive Website, ohne Build-Schritt und ohne externe JavaScript-Bibliotheken.
- `data.json`: öffentlicher Datenstand mit Angeboten, Fristen, Ereignishistorie, Quellen und Tagesprotokoll.
- `DESIGN.md`: gestalterische Entscheidungen und verwendete öffentliche Designhilfe.
- `PRODUCT.md`: Zweck, Zielgruppe und Grenzen.

## Aktualisierung

1. Aktuellen Live-Datenstand und bestehende Ereignisse lesen.
2. Anthropic Newsroom, Claude Platform Release Notes, Claude Help Center und relevante Originalankündigungen prüfen. Community-Archive nur als Suchhinweise verwenden. Unterschiedliche Belege und Widersprüche dokumentieren.
3. Aktive Angebote und abgelaufene Fristen abgleichen. Nicht aus Nichtfinden auf Nichtvorhandensein schließen.
4. `offers`, `forecast`, `signals` und `sources` aktualisieren. Bestehende `events` nicht löschen; Korrekturen kenntlich machen und neue Ereignisse ergänzen. Ältere sekundäre Archivhinweise dürfen erst nach Originalprüfung zu bestätigt wechseln.
5. Eine datierte Zusammenfassung an `analyses` anhängen, geprüfte Quellen benennen und erst dann `as_of` setzen.
6. JSON validieren, Code und Darstellung prüfen, committen. Live-Seite nach dem Pages-Build kontrollieren. Überalterungs- und Fehlerzustände nicht entfernen.

## Datenqualität

Der Erststand vom 11. November 2026 enthält drei hier primär geprüfte Ankündigungen und 13 weitere ältere, ausdrücklich als Archivhinweis markierte Ereignisse aus claudereset.org. Diese sind keine vollständig primär verifizierte historische Datenbank. Einlösbare Credits, globale Resets und Teil-Resets werden getrennt kategorisiert. Die Stichprobe ist nicht vollständig und nicht geeignet, aus einfachen Häufigkeiten eine Tageswahrscheinlichkeit abzuleiten.

Quellen und ihre Prüfhinweise stehen in `data.json` und sind auf der Website zugänglich. Zeitangaben werden mit ihrer Ursprungszeitzone gespeichert; sichtbare Termine verwenden Europe/Berlin. Eine Prognose ist kein Versprechen.

## Design und Datenschutz

Eigenständige redaktionelle Gestaltung, geprüft anhand öffentlich gelesener Impeccable-Designreferenzen von Paul Bakaus: https://impeccable.style und https://github.com/pbakaus/impeccable . Keine fremden Installer, Hooks oder Live-Agent-Mechanismen ausgeführt.

Keine Analytics, keine Cookies durch eigenen Anwendungscode, kein Login. Die Schrift Barlow Condensed wird über Google Fonts geladen, weshalb eine Verbindung zu Google-Fontservern entsteht. GitHub stellt Hosting und Zugriffsprotokolle bereit. `noindex,nofollow` bittet Suchmaschinen um Nichtindexierung; das Repository und die Website sind öffentlich und kein Geheimnis.

## Lokal prüfen

Im Verzeichnis `python -m http.server 8000` starten und `http://localhost:8000` öffnen. Die Seite lädt `data.json` per Fetch; ein direkter `file://`-Aufruf kann deshalb scheitern. Keine Abhängigkeiten und kein API-Schlüssel erforderlich.

## Weiterverwenden

Eigener Anwendungscode und eigene Texte: MIT, siehe `LICENSE`. Verlinkte Quellen, Markennamen und die externe Schrift behalten ihre eigenen Rechte und Bedingungen. Keine Zugehörigkeit zu Anthropic.
