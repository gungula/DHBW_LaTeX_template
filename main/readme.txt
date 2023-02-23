Ordner additionalPackages, beside und lang müssen i. d. R. nicht bearbeitet werden.
_______________________
Verwendung des Templates - Grundeinstellungen

einstellungen.tex:
- Sprache de oder en
- Eintragen sämtlicher persönlicher sowie projektbezogener Daten
- Auswahl zu enthaltener Seiten (bspw. Sperrvermerk ja / nein)
- grüner / gelber / roter Punkt (je nach Vertraulichkeit)

deckblatt.tex:
- Einfügen des Logos des Partnerunternehmens für das Deckblatt (2x) [Bilddatei in Ordner "images" ablegen!]

header.tex:
- Einfügen des Logos des Partnerunternehmens in den Kopfzeilen von Verzeichnissen, content-Seiten sowie Anhängen (je 2x -> 6x insgesamt) [Bilddatei in Ordner "images" ablegen!]

Einfügen von Kapiteln / Inhalten:
- neue .tex im Ordner content erstellen
- Namenskonvention zwingend einhalten: zweistellige Nummer muss fortlaufend hochgezählt werden, Bsp. 01kapitel.tex 
- neues Kapitel: \chapter{}
- neues Unterkapitel (1.1): \section{}
- neues Unterkapitel vom Unterkapitel (1.1.1): \subsection{}
Achtung: Bei DHBW-Arbeiten nicht tiefer als subsection gehen!
  
acronyms.tex:
- beinhaltet Abkürzungen für das Abkürzungsverzeichnis -> Erklärung in Datei

bibliography.bib:
- Quellenverzeichnis: Bestenfalls kann ein separates Literaturverwaltungsprogramm wie Zotero oder jabref verwendet werden --> von dort kann eine bibliography.bib exportiert und ins Projekt eingefügt werden, erleichtert den Umgang mit Quellen


Texte für Deckblatt, Sperrrvermerk und Selbstständigkeitserklärung werden automatisch erstellt und mit den in einstellungen.tex hinterlegten Daten gefüllt.

Sämtliche Verzeichnisse (auch Inhaltsverzeichnis) werden ebenfalls ohne manuelles Zutun erstellt und klickbar gemacht.

abstract.tex:
- Je nach Sprachauswahl wird die deutsche Kurzfassung oder der englische abstract ausgegeben.




