Dies ist ein Template von und für DHBW-Studenten nach den aktuellen Anforderungen für wissenschaftliche Arbeiten. Es handelt sich dabei um kein offizielles Dokument der DHBW!

Bei Fragen oder Problemen dürft ihr gern ein Issue öffnen.
_____________________________
# Betrieb mit angezeigter .pdf in VS Code
1. Installation der Extension "Perl" (Language Server and Debugger for Perl)

2. Installation der LaTeX-Extension "LaTeX Workshop" (Doku: https://github.com/James-Yu/LaTeX-Workshop/wiki)

3. LaTeX-recipe in settings.json (~/home/.config/Code - OSS/User/settings.json) anpassen: 

``` 
{
    "latex-workshop.latex.recipes": [
        {
          "name": "latexmk",
          "tools": [
            "latexmk"
          ]
        },
        {
          "name": "pdflatex -> bibtex -> pdflatex * 2",
          "tools": [
            "pdflatex",
            "bibtex",
            "pdflatex",
            "pdflatex"
          ]
        }
      ]
}
``` 

4. Ändern des Compilers zu "LaTeX Workshop" (VS Code interne Konsole - Dropdown oben rechts)

5. dokumentation.pdf kann in der seitlichen Vorschau angezeigt werden. Änderungen übernehmen mit dem grünen Dreieck (build).
_______________________
# DHBW_LaTeX_template

**Ordner lang muss i. d. R. nicht bearbeitet werden.**
Je nach verwendeter Textverarbeitungsumgebung muss ggf. die source-Datei manuell eingestellt werden, da sonst kein build erfolgen kann. 
Die source-Datei ist: **dokumentation.tex**
_______________________
## Verwendung des Templates - Grundeinstellungen

### einstellungen.tex:
- Sprachauswahl *de*utsch oder *en*glisch
- Eintragen sämtlicher persönlicher sowie projektbezogener Daten (zum automatisierten Einpflegen an alle relevanten Stellen wie bspw. Deckblatt, Selbstständigkeitserklärung, ...)
- Auswahl zu enthaltener Seiten mit true und false (\selbsterkltrue oder \selbsterklfalse, \formelverztrue oder \formelverzfalse, ...) oder alternativ Auskommentieren entsprechender Zeilen
- grüner / gelber / roter Punkt (je nach Vertraulichkeit bzw. Sperrvermerk)

### deckblatt.tex:
Einfügen des Logos des Partnerunternehmens für das Deckblatt (2x) [Bilddatei in Ordner "images" ablegen!]

### header.tex:
Einfügen des Logos des Partnerunternehmens in den Kopfzeilen von Verzeichnissen, content-Seiten sowie Anhängen (je 2x -> 6x insgesamt) [Bilddatei in Ordner "images" ablegen!]

### Einfügen von Kapiteln / Inhalten:
- neue .tex im Ordner content erstellen
- Namenskonvention zwingend einhalten: zweistellige Nummer muss fortlaufend hochgezählt werden, Bsp. 03kapitel.tex 
- neues Kapitel: \chapter{}
- neues Unterkapitel (1.1): \section{}
- neues Unterkapitel vom Unterkapitel (1.1.1): \subsection{}
Achtung: Bei DHBW-Arbeiten nicht tiefer als subsection gehen!
  
### acronyms.tex:
- beinhaltet Abkürzungen für das Abkürzungsverzeichnis -> Erklärung in Datei

### bibliography.bib:
Quellenverzeichnis: Bestenfalls kann ein separates Literaturverwaltungsprogramm wie Zotero oder jabref verwendet werden --> von dort kann eine bibliography.bib exportiert und ins Projekt eingefügt werden, erleichtert den Umgang mit Quellen. <br>
Offizielle Dokumentation von [BibLaTeX](https://mirror.informatik.hs-fulda.de/tex-archive/info/translations/biblatex/de/biblatex-de-Benutzerhandbuch.pdf#9)

### abstract.tex
Je nach Sprachauswahl wird die deutsche Kurzfassung oder der englische abstract ausgegeben.

### Allgemeines

Texte für Deckblatt, Sperrvermerk und Selbstständigkeitserklärung werden automatisch erstellt und mit den in einstellungen.tex hinterlegten Daten gefüllt.

Sämtliche Verzeichnisse (auch Inhaltsverzeichnis) werden ebenfalls ohne manuelles Zutun erstellt und interaktiv (klickbar) gemacht.

-------------------------------------
## Erläuterungen Ordnerstruktur / Dateien
### ads ("additionals")
Hier befinden sich alle standardmäßig zu enthaltenen Seiten und Verzeichnisse.

#### abstract.tex
Kurzfassung bzw. abstract

#### acronyms.tex
Abkürzungsverzeichnis

#### appendix.tex
Anhang

#### deckblatt.tex
Deckblatt

#### einstellungen_liste.tex
Nicht anfassen! Hier werden Bezeichnungen einzelner Einstellungen definiert, auf die im gesamten Dokument referenziert wird.

#### header.tex
Hier werden die Kopf- und Fußzeilen unterteilt für die einzelnen Abschnitte (Deckblatt, Content, Anhang) definiert. An dieser Stelle können auch Firmenlogos hinzugefügt werden.

#### selbststaendigkeitserkl.tex
Selbstständigkeitserklärung

### content
Hier werden die einzelnen Inhaltsseiten nach der Namenskonvention "xxkapitel" hinzugefügt. Die Nummern müssen fortlaufend vergeben werden und werden entsprechend sortiert.

### images
Ablage sämtlicher im Dokument verwendeter Bilder. Dazu gehören sowohl Logos (DHBW, Firma) als auch in der Arbeit verwendete Grafiken.

### lang
Nicht anfassen! Hier werden die einzelnen Strings, welche sich auf deutsch und englisch unterscheiden, festgelegt und ggf. übersetzt.

### dokumentation.tex
Dies ist die Source-Datei für die .pdf-Ausgabe. Hier muss i. d. R. nichts verändert werden.

### cleand.cmd / clean.sh
Diese Datei löscht bei Ausführung alle bei .pdf-Erstellung automatisch generierten, nicht benötigten files wie bspw. dokumentation.aux .

### main
#### einstellungen.tex
Hier werden sämtliche Einstellungen zu Form und Inhalt der Arbeit getroffen. Es werden Eigenschaften wie Sprachen oder anzuzeigende Verzeichnisse definiert als auch Eintragungen wie Name, Matrikelnummer, Titel der Arbeit etc. vorgenommen.

