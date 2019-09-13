# LaTeX Briefvorlage

Im Jahr 2009 habe ich einen Blog-Post veröffentlicht mit einer LaTeX-Briefvorlage: https://gehrcke.de/2009/12/latex-briefvorlage/

Über die Jahre habe ich dazu sehr viel positives Feedback bekommen (Danke!) und 2013 ein größeres Update vorgenommen.

Auch in den letzten 6 Jahren (2013 bis 2019) habe ich die Briefvorlage für mich selbst sehr viel benutzt und leicht weiterentwickelt (eine wesentliche technische Änderung im Vergleich zur Version von 2009 und 2013 ist der Umstieg von `pdflatex` nach `lualatex` für die Kompilierung in ein PDF-Dokument).
In diesem Code-Repository findet Ihr nun die aktuelle Variante.
Ihr könnt die Vorlage gerne für alles erdenkliche benutzen.
Und bitte gebt mir gerne weiterhin Feedback!


## Quickstart

1. Passe `brief-absender.lco` mit Deinen persönlichen Details an.
2. Passe `brief.tex` an.
3. Generiere Deinen Brief als PDF-Datei mit `lualatex`:

```
$ lualatex brief.tex
This is LuaTeX, Version 1.07.0 (TeX Live 2018)
 restricted system commands enabled.
(./brief.tex
LaTeX2e <2018-04-01> patch level 5

[...]

(./brief-absender.lco

[...]

Output written on brief.pdf (1 page, 28471 bytes).
Transcript written on brief.log.
```

4. Betrachte `brief.pdf` in einem PDF-Viewer.


## Kompatibilität

Ich habe `brief.tex` zuletzt mit `lualatex` in [TeX Live](https://www.tug.org/texlive/) 2018 getestet.
TeX Live ist meine favorisierte LaTeX-Distribution (ich habe in den letzten 10 Jahren nichts anderes benutzt; ich installiere immer die vollständige Distribution).
Es funktionieren höchstwahrscheinlich auch ältere Versionen von `lualatex` sowie zukünftige.

## Hinweise:

- Speichere `brief.tex` und `brief-absender.lco` mit dem UTF-8 codec (ohne BOM, wenn Du die Wahl hast).
- Du kannst `brief.tex` beliebig umbenennen. Wenn Du `brief-absender.lco` umbenennst musst Du die Datei-Endung `.lco` unbedingt beibehalten und in `brief.tex` die Referenz `\LoadLetterOption{brief-absender}` entsprechend anpassen.
- Führe `lualatex brief.tex` zweimal aus wenn du die Quelldateien geändert hast.
- `brief-absender.lco` beinhaltet einige Stil-Definitionen die Geschmackssache sind, wie z. B.  `\setkomafont{fromaddress}{\small\mdseries\slshape\color{black}}`. Das kann alles angepasst werden (eine Internet-Recherche hilft).


## Referenzen

- https://de.wikibooks.org/wiki/LaTeX-Kompendium:_Sonderzeichen
- https://practicaltypography.com/first-line-indents.html
- https://www.tug.org/texlive/windows.html
- https://de.wikipedia.org/wiki/LaTeX
- https://de.wikibooks.org/wiki/LaTeX-Kompendium
- https://de.wikibooks.org/wiki/LaTeX-Kompendium:_Schnellkurs:_Das_erste_Dokument