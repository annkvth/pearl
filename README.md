# FaPra Echtzeitsysteme 2024/2025

**Inhalt**
  * [Links zum Thema PEARL](#links-zum-thema-pearl)
  * [Allgemeines zum FaPra](#allgemeines-zum-fach-praktikum)
    + [Termine](#termine)
  * [Aufgaben](#aufgaben)
    + [Erste Aufgabe: Erzeuger-Verbraucher-Problem](#erste-aufgabe-erzeuger-verbraucher-problem)
    + [Zweite Aufgabe: Wassertank](#zweite-aufgabe-wassertank)


## Links zum Thema PEARL

- [PEARL Einführung](https://www.real-time.de/service/pearl.html)
- [OpenPEARL Wiki Tutorials](https://sourceforge.net/p/openpearl/wiki/Tutorial%20-%20PEARL%20by%20Examples/)
- [PEARL90 Lehrbuch L. Frevert](http://www.real-time.de/misc/PEARLFrev.pdf)
- [Differences PEARL90 / OpenPEARK](https://sourceforge.net/p/openpearl/wiki/Differences%20between%20OpenPEARL%20and%20PEARL90/)



## Allgemeines zum Fach-Praktikum
Modulbeschreibung: https://www.fernuni-hagen.de/mi/studium/module/fezs.shtml
- [Folien Einführungsveranstaltung](https://fernuni-hagen.sciebo.de/s/9etRRBEfmbKnhwZ)
- Skript ["Konzepte der Echtzeitprogrammierung"](https://fernuni-hagen.sciebo.de/s/5poMtPEqgZgqpvB)

### Termine
- Einführungsveranstaltung am 4.10.2024 von 13:00 bis ca. 15:00
- Online-Meeting am 9.11.2024 ab 15:00 (tdc)
- Abgabetermin am 19.1.2025
- Vorträge am 25.1.2025 ab 9:00

## Aufgaben ##
_Auszug aus den Folien der Einführungsveranstaltung_

- Warm-Up: Ausgabe einer Zeichenkette auf die Konsole. Ziel ist es sicherzustellen, dass die Entwicklungsumgebung funktioniert.
- 1. Aufgabe: Erzeuger-Verbraucher-Problem. Ein klassisches Problem der Informatik ist das Erzeuger-Verbraucher-Problem. Hierbei sollen die beteiligten Tasks über eine gemeinsame Datenstruktur kommunizieren.
- 2. Aufgabe: Steuerung der Befüllung eines Wassertankes. Ziel ist die Befüllung eines Wassertankes in Echtzeit zu regeln und auf etwaige Fehlerzustände fristgerecht zu reagieren.

### Erste Aufgabe: Erzeuger-Verbraucher-Problem
- Starten Sie drei gleichartige Erzeugertasks.
- Jede Task soll solange pro Sekunde je eine Nachricht in eine Nachrichten-Queue schreiben bis alle Tasks je 10 Nachrichten abgelegt haben.
- Das maximale Fassungsvermögen der Nachrichten-Queue sei auf 8 Einträge beschränkt.
- Starten Sie eine Verbrauchertasks, welche die Nachrichten alle 1.5 s abruft.
- Starten Sie eine zweite Verbrauchertasks, welche parallel Nachrichten alle 2s abruft.
- Protolieren Sie alle Schritte auf der Konsole.
- Dokumentieren Sie auch ggf. den Verlust einzelner Nachrichten aufgrund der Überfüllung der Nachrichtenwarteschlange.


### Zweite Aufgabe: Wassertank

Die Aufgabe beinhaltet
- einen Wassertank mit einem maximalem Füllvolumen
- einer drehzahlgesteuerten Pumpe
- einem Drucksensor, welcher den Wasserdruck der Pumpe misst
- einem Ventil, welches geöffnet oder geschloßen sein kann
- einem Drucksensor, welcher den Druck am Boden des Wassertankes misst
- einem Schwimmerschalter, welcher bei maximaler Tankbefüllung schaltet
- einem Verbraucher, welcher quasi zufällig eine Menge Wasser pro Zeiteinheit benötigt

Es soll eine Regelung konzipiert werden, welche folgende Anforderungen erfüllt:
- Der Wassertank soll dem Verbraucher zu jedem Zeitpunkt die benötigte Wassermenge zur Verfügung stellen.
-  Die Pumpe soll nur nach Bedarf ein- und ausgeschaltet werden.
-  Im Fehlerfall, wenn z.B. die Pumpe oder das Ventil ausfallen, soll ein Not-Halt durchgeführt werden.
-  Der Überlauf soll erkannt werden und eine angemessene Reaktion eingeleitet werden.
-  Falls der Tank leerläuft soll dieses Ereignis erkannt und eine angemessene Reaktion eingeleitet werden.

Alle Schaltvorgänge sollen protokolliert werden. 

**Wichtig:** Weiterhin ist ein Testkonzept zu erstellen.


