Git-Schulungsmaterialien
========================

Die Schulungsmaterialien sind auf eine zweitägige Schulung ausgelegt;
per Default werden bei einem Aufruf von `make` vier Dateien,
`session_1.pdf` bis `session_4.pdf`, erzeugt; jedes Foliendeck ist für
einen halben Tag gedacht. Zusätzlich liegt unter `workshop.wiki` ein
Beispiel für einen kürzeren Workshop, wird per `make workshop` gebaut.

Die Materialien sind komplett zweisprachig deutsch/englisch.
Durch `mv deckblatt-en.wiki deckblatt.wiki && make` wird die englische Version
produziert.

Die Folien wurden mit dem GPL lizensierten
[wiki2beamer](http://wiki2beamer.sourceforge.net/) realisiert. Das Programm ist
als Abhängigkeit unter `folien/wiki2beamer` inkludiert.

Diverse Teile der Schulung sind per Default nicht eingebunden (z.B.
Gerrit, Gitolite). Am schnellsten findet man diese per
`./find-unused.sh` im Verzeichnis `folien/`; eine entsprechende
Include-Zeile in einer der Session-Datein aktiviert sie.

Hinweise zur Kompilierung
=========================

Auf dem Rechner muss folgendes installiert sein:
1. LaTeX (auf Ubuntu: `sudo apt install texlive-latex-base`)
2. Python
3. Die Style-Klassen `pgf` und `beamer`

Auf Ubuntu hat dazu folgendes geklappt:
`sudo apt install texlive-science` installiert die Klasse `beamer`

Die Klasse `pgf` muss manuel installiert werden. 
1. Die Datei `pgf_3.0.1.tds.zip`von `https://sourceforge.net/projects/pgf/files/pgf/version%203.0.1/pgf_3.0.1.tds.zip/download` herunterladen.
2. Im Homeverzeichnis den Ordner `texmf` anlegen
3. Die Datei `pgf_3.0.1.tds.zip`dort entpacken

Nun kann man wie oben beschrieben mit `make` den Foliensatz erzeugen.


Lizenz
======

Lizensiert unter der [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).
