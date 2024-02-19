# Die marginalisierte SVP in Zürich?

Analyse von Vorstössen im Zürcher Gemeinderat von 1. Januar 2014 bis 1. Januar 2024


## 1 Checkliste
These: Die SVP ist im Zürcher Stadtparlament ziemlich isoliert und hat Mühe
These checken: Die Probleme der SVP in den Städten ist ein Trend. Über die sinkende Wähleranteile wurde einiges geschrieben. Eine detaillierte Analyse zum Zürcher Gemeinderat ist mir nicht bekannt. Der Aufwand war etwas grösser als gedacht. Die Arbeit lässt sich aber zweitverwerten für eine Datenanalyse vor den nächsten Wahlen.
Knackpunkt bestimmen. Es könnte sein, dass zu wenig klare Unterschiede zu anderen Parteien resultieren. Das war aber nicht der Fall
Briefing Person konsultieren: Aufbau des Artikels mit Kollegen im Ressort diskutiert, für die Visualisierung mit unserem Visuals-Team gesprochen.
Daten beschaffen/reinigen/analysieren/visualisieren: Daten Beschaffung war Anfangs aufwendig, weil ich noch nie mit XML-Daten gearbeitet habe. Habe schliesslich Workaround gemacht und zu JSON umgewandelt. Zudem war die Datenstruktur sehr verschachtelt auf der API des Gemeinderats und einige Resultate waren nur auf separaten PFD zu finden.
Ergänzen durch klassische Recherche: Gespräche mit drei wichtigen Exponenten der Zürcher SVP (Experten, Politiker etc.)
Dokumentieren Code: Ist in den Notebooks zu finden
Link auf Publikation: Kommt nach, Artikel soll am 19. Februar online gehen
Aufwandslogbuch: siehe unten

## 2 Datenquelle
Für meine Analyse habe ich alle Vorstösse der SVP der letzten zehn Jahre bzw. vom 1. Januar 14 bis 1. Januar 24 von der API des Gemeinderats heruntergeladen mit den wichtigsten Angaben dazu: Titel des Vorstosses, Zeitpunkt der Einreichung, Geschäftsart, Mitunterzeichnung von anderen Parteien, Erfolg von Motionen und Postulaten im Parlament. Letzteres hat sich als kompliziert erwiesen, die genauen Resultate sind separat in PDF hinterlegt. Das Problem liess sich weitgehend einfach lösen, da zwar nicht das genaue Abstimmungsresultat aber zumindest der Fakt, ob es überwiesen wurde oder nicht, in der API verzeichnet ist. Nur für Motionen, die zu Postulaten umgewandelt wurden, fanden sich in der API keine Resultate. Da dies selten vorkommt, habe ich dies von Hand in den PDFs nachgeschaut und in den Daten ergänzt.
Probleme hatte ich auch mit dem XML-Format. Ich versuchte es einen Tag lang mit BeautifulSoup. Das brachte mich aber in immer neue Schwierigkeiten. Die Umwandlung von XML in JSON erleichterte die Arbeit dann deutlich. Auch dann ist die Datenstruktur aber recht unübersichtlich auf der API des Gemeinderats.

## 3 Analyse der Daten
Ich habe die Daten nach verschiedenen Kriterien analysiert. Interessant waren vor allem folgende Ergebnisse: Es zeigte sich, dass die SVP in der neuen Legislatur (seit Mai 2022) viele Vorstösse einreicht. Dabei handelt es sich insbesondere um Postulate und Motionen, also gewichtige Vorstösse bzw. solche, die im Gegensatz zu den Anfragen auch wirklich etwas bewirken. Ich habe zudem berechnet, wie erfolgreich die SVP mit ihren Postulaten und Motionen in den letzten Jahren war und dies mit SP, GLP und FDP vergleichen (jeweils die grösste Partei links, in der Mitte und rechts). Die anderen Parteien sind deutlich erfolgreicher, das gilt auch für die FDP, die mit der SVP ja meist in der bürgerlichen Minderheit im Rat ist. Eine Erklärung dafür findet sich in der Isolation der SVP. Ich habe geschaut, wie oft die SVP und die anderen drei Parteien Vorstösse gemeinsam mit anderen Parteien einreichen. SP, GLP und FDP arbeiten häufig mit anderen zusammen, die SVP macht das sehr viel seltener
Die Daten belegen also die Erfolglosigkeit und die Isolation der SVP im Gemeinderat. Sie deuten aber auch darauf hin, dass die SVP eine neue Strategie hat: mit einer hohen Anzahl von Postulaten und Motionen Druck im Parlament zu machen. Dies bestätigte sich dann auch im Gespräch mit dem Fraktionschef der SVP.

## 4 Artikel
https://www.nzz.ch/zuerich/niedergang-der-svp-in-zuerich-neue-strategie-soll-krise-beenden-ld.1807233

## 5 Aufwandlogbuch

- Daten besorgen: 16 Std. 
- Datenreinigung: 5 Std.
- Datenauswertung: 6 St
- Visualisierung: 2 Std.
- Gespräche und Schreiben: 16 Std.
- TOTAL: 45 Std.

