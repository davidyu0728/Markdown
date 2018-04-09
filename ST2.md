# <font color ='black' face="微软雅黑"> Technologien und Methoden der Softwaresysteme II

## Ziele


- Softwarequalität

## 1. Konfigurationsmanagment
### 1.1 Difinition und Abgrenzung von Konfigurationsmanagment

#### Das Navigationssystem der Softwareentwicklung ist das Konfigurationsmanagement

#### Ausgangssituation

Ein Projekt

- Mehrere Mitarbeiter <font color ='red'> 2-20 Personen
</font>
- Längere Entwicklungszeit<font color ='red'> 3 Monate -3 Jahre
</font>

- Wartungsverpflichtungen<font color ='red'>1 Jahr -15 Jahre
</font>

- Unmenge von Dokumenten<font color ='red'> 50 –5000 Dokumente
</font>

- Unterschiedliche Versionen<font color ='red'> 5 -10 Versionen
</font>

- Mehrere Varianten<font color ='red'> 0 -1000 Varianten
</font>

#### Wozu braucht man Konfigurationsmanagment?

#####  Chaos und Informationsverlust
##### bei Einzeländerungen

- Abhilfe: Festhalten aller Änderungen(补救措施：关注所有改动)
	- Inhalt
 	- Grund
	- Zeitpunkt
	- Verantwortlicher

##### bei zusammengehörigen Änderungen
- Abhilfe: Änderungsmanagment
	- Verknüpfung von Änderungswünschen mit den tatsächlichen Änderungen
	- Überwachung des Ablaufs von Änderungen

##### bei der zeitlichen Verwaltung zusammengehöriger Änderungen

- Abhilfe: Konfigurationsselektion
	- Automatische Versions-und Konfigurationsselektion
	- Dokumentation des Resultats

##### bei der Beherrschung der Gesamtinformation

- Abhilfe: Rechnerunterstützung bei der Verwaltung
	- Sorgfältige, rechnerunterstützte Überwachung der Durchführung aller Arbeitsschritte

#### Was ist Konfigurationsmanagement?

Konfigurationsmanagement ist eine Menge von

- Verfahren
- Methoden
- Werkzeugen

zur Verwaltung aller Arbeitsergebnisse der Entwicklung und ihrer Änderungsgeschichte

##### Ziele:

- Auffinden und Wiederherstellen von alten Softwareversionen
- Verwaltung von Software mit vielen Versionen und Varianten
- Ableitung von Unterschieden zwischen unterschiedlichen Versionen
- Prozesstransparenz, Prozesskontrolle

#### Was wird beim Konfigurationsmanagement verwaltet?
##### Dokumente
##### Produkte
##### Sonstige Objekte

#### Aufgaben des Konfigurationsmanagements
##### Sicherstellung, dass

- Alle Entwicklungstätigkeiten auf einer gesicherten Basiserfolgen
- Nur in sich konsistente Systeme erzeugt werden
- Mehrere Varianteneiner Anwendung parallel existieren können
- Parallele Entwicklung verschiedener Systemteile möglich ist und die Ergebnisse wieder zusammengeführt werden können
- Produktions-und Entwicklungsversionen unterscheidbar sind
- Auf historische Zustände zurückgesetzt werden kann
- Änderungen nur von dafür autorisierten Personen vorgenommen werden können
- Abhängigkeitenaufgezeigt werden, die bei Änderungen zu beachten sind
- Alle wichtigen Modifikationen protokolliertwerden
- Beziehungenzwischen Änderungenund Versionenaufgezeigt werden

#### Anforderungen an ein Konfigurationsmanagement
- Definitionund Identifizierungvon logisch zusammengehörenden Bausteinen (Konfiguration)
- Kontrolle der Freigabe und der Änderungender Konfigurationsbausteine während des gesamten Lebenszyklus
- Protokollierungund Erstellung von Berichten zum Status der Konfigurationsbausteine und Änderungsforderungen
- Sicherstellung der Vollständigkeit und Korrektheit von Konfigurationsbausteinen
- Ausleihmechanismusfür verwaltete Objekte

### 1.2 Objekte des Konfigurations-managements
#### Begriffe des Konfigurationsmanagements

<font color = 'red'> 

- Konfigurationen
- Version
- Baseline
- Release
- Variante
- Verzweigte Versionierung

</font>

#### Konfiguration

- Definierte Menge von Verwaltungseinheiten (Dateien), die zusammen ein sinn-volles Ganzes ergeben
- Bei der Konfiguration werden keine Aussagen zur Version gemacht
![](https://i.loli.net/2018/04/10/5acbe59a6632b.png)

##### Komplexe Konfiguration
![](https://i.loli.net/2018/04/09/5acb39f3dd4fb.jpg)

##### Überlappende Konfigurationen
![(https://i.loli.net/2018/04/10/5acbe5c3e3f94.jpg)

#### Version
- Versionsbegriff bezieht sich auf eine atomare Verwaltungseinheit
- Version indiziert den Entwicklungsstand dieser atomaren Einheit

##### Aufgaben der Versionierung

- Protokollierung der Änderungen
- Wiederherstellung von alten Zuständen einzelner Dateien
- Archivierung der Dateien
- Koordinierung des gemeinsamen Zugriffs
- Gleichzeitige Entwicklung

#### Baseline

- Baseline beschreibt den Entwicklungsstand einer Konfiguration
- Zu einem bestimmten Zeitpunkt formell gekennzeichnete und festgeschriebene Konfiguration
![](https://i.loli.net/2018/04/10/5acbe5d8363eb.jpg)

#### Release

- Definiert das an den Kunden ausgelieferte Produkt
- Basiert auf einer Konfiguration einer Baseline und freigegebenen Änderungen

##### Beispiel: Fernwirksystem

- Ausgeliefert wird: Konfiguration Fernwirksystem
- Basiert auf Baseline vom 10.01.16
- Änderungen: Modem.H;5
![](https://i.loli.net/2018/04/10/5acbe5ed6e474.jpg)

#### Zusammenführung der Begriffe
![](https://i.loli.net/2018/04/10/5acbe5f68103d.jpg)

#### Variante

- Durch Parametrisierung oder Modifikation werden spezielle Kundenwünsche erzeugt und installiert
- Unterschiedliche Hardware mit unterschiedlicher Basissoftware
![](https://i.loli.net/2018/04/10/5acbe61b789e2.jpg)

#### Verzweigte Versionierung
Problemstellung

- Fehlerhaftes Vertriebsprodukt (basierend auf Basline vom 01.06.09)
- "Schnittstelle.H" ist zu korrigieren (am 10.01.10)
![](https://i.loli.net/2018/04/10/5acbe6c6cb4ab.jpg)

