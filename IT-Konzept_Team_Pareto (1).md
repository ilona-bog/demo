# IT Konzept
## Teamname  
Team Pareto

## Projektname
ParetoTrack

## Version
0.2

### Dokumenthistorie 

| Datum | Autor | Version |
|---|---|---|
| 16.10.2022 | Hendrik Schlange | 0.2 |
| 15.10.2022 | Michael Wischniewski | 0.1 |



## Kurzbeschreibung
Logistikunternehmen im Bereich Seefracht stehen vor der Herausforderung, dass sie den aktuellen Status ihrer Sendungen verfolgen müssen. Dies erfolgt in der Regel über die Webinterfaces der Reedereien.
Die Software ParetoTrack ermöglicht Logistikunternehmen die Nachverfolgung von Containern anhand der Containernummer über ein zentrales Webinterfaces oder über eine einzige API.
Die Integration in bestehende Logistik-Software und die Möglichkeit Container verschiedener Reedereien in einer einzigen Suche zu berücksichtigen, tragen wesentlich zur Zeit- und Kostenersparnis bei.

Die Entwicklung der Software erfogt in drei Phasen:
In der erstem Phase wird eine Benutzereschnittstelle entwickelt, welche das Container-Tracking über per Webinterface ermöglicht. Das Release zur Anwendung in Webbrowsern ist für das 2. Quartal 2023 geplant.

Nach erfolgreicher Evaluierung zur Nutzung per Webbrowser wird eine API entwickelt, mit der Softwareanbieter und Unternehmen ihre Systeme an ParetoTrack anbinden können, sodass das Tracking vollautomatisch erfolgt.

Im Anschluss werden Mehrwertdienste wie bspw. die Normalisierung von Tracking-Events, Push-Nachrichten bei Problemen oder ETA-Vorhersagen mit Machine Learning implementiert.

## Stakeholder
- Logistikunternehmen
- Reedereien
- Versender
- Empfänger
- Auftraggeber

### 1. Projektziel
Projektziel ist die Entwicklung eines Prototypen für das Tracking von Seefrachtcontainern.
Technische Grundlage für die Entwicklung bilden die Programmiersprache Python mit den Frameworks [Flask](https://flask.palletsprojects.com/en/2.2.x/) und [Bootstrap](https://getbootstrap.com). Der Datenbanksupport wird mit Hilfe des Object-relational Mappers [SQLAlchemy](https://www.sqlalchemy.org) realisiert.

### 2. Basis
Methodisch erfolgt die Entwicklung von Scrum. Dabei arbeiten zwei Teams gleichzeitig an der Umsetzung des Projektes. Der Projektfortschritt wird in wöchentlichen Meetings in Protokollen, sowie anhand des Ticket-Backlogs festgehalten (bspw. anhand von Burn-Down-Charts).
Die Sprintlänge während der Umsetzung beträgt jeweils zwei Wochen. Am Ende eines Sprints werden über eine Retrospektive der Fortschritt und die Methodik während des vorhergegangenen Sprints ausgewertet. Alle Team-Mitglieder sollen in der Sprint Retrospective ihr Feedback geben. Das Feedback dient der Verbesserung der Zusammenarbeit im nächsten Sprint und sollte beschreiben, was in der bisherigen Zusammenarbeit gut war und was verbesset werden kann.

Das Ticket Backlog wird in Jira verwaltet. Das Repository für die Applikation wird bei GitHub gehostet.

Releases werden dynamisch bei Erreichung eines funktionalen Meilensteines erstellt. Builds werden mit Hilfe einer CI/CD Pipeline erzeugt. Dabei werden sowohl Unittests als auch die Code Qualität (Linting) geprüft.
 
### 2.1. Systemarchitektur
Die folgend genannten Systemkomponenten beziehen sich auf die erste Komponente zur Standortsuche über Webbrowser.

#### 2.1.1 Systemkomponenten

##### 2.1.1.1. Hardware 
###### Server-Hardware:
- Server mit
- WSGI Server
- Datenbank-Server

###### Client-Hardware:
- PC oder mobiles Endgerät mit Webbrowser

#### 2.1.1.2. Software
Software auf dem Server
- VM via AWS
- Apache TomCat Webserver in aktuellster Version
- Java RTE
- MySQL-Server

Software auf dem Client
- Webbrowser „Google Chrome“ oder „Microsoft Edge“ oder „Mozilla Firefox“ oder „Apple Safari“ bzw. Webbrowser mit der aktuellesten Version der Blink-Engine oder Chromium-Engine oder Edge-HTML oder WebKit-Enging oder Mozilla-Engine

### 2.2. Voaussetzungen
Die folgend genannten Systemvoraussetzungen beziehen sich auf die erste Komponente zur Standortsuche über Webbrowser.

#### 2.2.1. Systemvoraussetzungen

##### 2.2.1.1 Systemvoraussetzungen auf dem Server
Linux-Betriebssystem, welches die im Punkt "Software" genannte Software unterstützt.

##### 2.2.1.1  Systemvoraussetzungen auf dem Client
auf mobilen Endgeräten (Smartphone, Tablets)
Betriebssystem: Android oder IOs 
Webbrowser
| Browser           | Version     | Engine            |
|---|---|---|
| Firefox           | 65+         | Mozilla 64+       |
| Chrome            | 72.0.3626 + | Blink 72+         |
| Edge              | 44.1836+    | EdgeHTML 18.18362 |
| Safari            | 12.1+       | WebKit  607.140+  |
| Opera             | 58+         | Chromium 71+      |

auf PC 
| Browser           | Version     | Engine            |
|---|---|---|
| Firefox           | 65+         | Mozilla 64+       |
| Chrome            | 72.0.3626 + | Blink 72+         |
| Edge              | 44.1836+    | EdgeHTML 18.18362 |
| Safari            | 12.1+       | WebKit  607.140+  |
| Opera             | 58+         | Chromium 71+      |

#### 2.2.2. Betriebssysteme
Betriebssystem auf dem Server
Linux Red Hat Enterprise Linux oder ein beliebiges anderes Linux-System, welches die unter dem Punkt "Software" genannte Server-Software bereitstellt.

Betriebssystem auf dem Client
- Mobilgeräte: Android, IOs
- PCs: Windows10, ein beliebiges anderes Linux-System, welches die unter dem Punkt "Software" genannte Client-Software unterstützt.

### 2.2.3. Netzwerk

#### 2.2.3.1. Bandbreite (Carrier, QoS) 
50 mbit
QoS nicht notwendig, da zu übertragende Datenmenge gering. Der Datenaustausch muss für diese Anwendung nicht priorisiert werden.

##### 2.2.3.2. IP-Adressen/ Ports /Firewallfreischaltung/QoS
##### Cloud-Bedarf 
- 2 virtuelle Server (Mirror)
- 2 virtuelle Datenbanken (Mirror)

### 2.2.4. Betriebskonzept 
- 

###  2.2.5 Ausgangsschnittstellen 

### 2.2.6. Updateverfahren (Securitypatches,..) 
Securitypatches auf dem Server
Mit dem Provider wird ein SLA vereinbart, der die Installation der aktuellen Security Patches für das Betriebssystem beinhaltet.
Die Anwendungen und Plugins werden durch unser Team aktualisiert

Securitypatches auf dem Server
- Updates der Betriebssysteme über das Systemupdate
- Updates der Browser und der Java RTE wird durch die Anwender installiert

#### 2.2.7. Datensicherung / Logs 
- Erstellung eines Backups alle 15 Minuten
- Erstellung von Logs und Sicherung für 3 Monate
- Auswertung der Logs manuell per Splunk


### 2.2.8. Notfallkonzeption 

#### 2.2.8.1. Notfallkonzept auf dem Server
Die Anwendungen (Web-Server, MySQL-DB, Java RTE) werden auf dem Server in einer VM ausgeführt.
Über RAID5 wird die Server-VM auf 2 Server gespiegelt.
Bei Ausfall eines Servers wird automatisch auf die VM des 2. Servers umgeschaltet.
24/7 Support durch den Provider via SLA gewährleistet.

### 2.2.9. Support 
Benutzer-Anfragen werden via Telefon oder E-Mail oder Chatbots zu den Geschäftszeiten beantwortet. 

#### 2.2.9.1. Entry Point für Incidents 
Incident-/Ticket-System "ZenDesk"

#### 2.2.9.2. Geschäftszeit 
08:00-18:00 Uhr

#### 2.2.9.3. Reaktionszeit // Wiederherstellungszeit
| Servicelevel | response time | resolution time |
|---|---|---|
| L1           | 1 Stunde      | -               |
| L2           | 12 Stunden    | 1 business day  |

#### 2.2.9.4. Wartungszugang
Supportanfragen werden ausschließlich via Telefon oder E-Mail oder Chatbots  beantwortet.
Ein Wartungszugang auf das Endsystem des Clients ist daher nicht erforderlich.

### 2.2.10. Bedienoberflächen
HTML5-Seite für das UI zur Anwendung

### 2.2.11. Hardware – Wartungsbedarf
kein Wartungsbedarf
Die Web-Server werden via AWS gemietet.

#### 2.2.12. Quellsysteme 

### 2.3. Zielsetzung
In der Implementierung haben die Wahrung der Datenintegrität und der Datenschutze oberste Priorität.
Die Validierung der Eingaben erfolgt durch Prüfmethoden und dem Abfangen von Ausnahmen (Exceptions).
Für alle Webseiten wird das Anwendungs-Protokoll HTTPS erwendet.

### 2.4. Performanz
Bei 1000 parallelen Aufrufen darf die maximale Zugriffszeit 2 Sekunden nicht überschreiten und das Ergebnis zur Standortsuche innerhalb von maximal 10 Sekunden dem Anwender zur Verfügung stehen.

### 2.5. Verfügbarkeit/Ausfallsicherheit.
Für die Nutzung der Anwendung wird eine permanente Verfügbarkeit (24/7) angestrebt.
Bei einem Ausfall ist die Verfügbarkeit der Anwendung innerhalb von 4 Std. zu gewährleisten. Ausgenommen sind Ausfälle, die vom Unternehmen, welches die Anwendung bereitstellt, nicht zu beeinflussen sind (z. B. Stromausfall, Ausfall der Systeme beim Provider).

### 2.6. Ansprechpartner

- Ilona Bogdasarova
- Leon Hitzer
- Michael Meineke
- Hendrik Schlange
- Manuel Stahl
- Michael Wischniewski

### 3. Daten
Genannte Bedingungen und Informationen beziehen sich auf die erste Komponente zur Standortsuche über Webbrowser.

#### 3.1 Überblick


#### 3.2. Architektur
In der Anwendungsschicht wird die Komponente zur Standortsuche über Webbrowser über die Architektur Modell-View-Controller entwickelt.  
Die Daten werden in SQL-Tabelle gehalten. In der Implementierung werden die Attribute der Entitäten und Programm-Methoden über den objekt-orientierten Ansatz in Klassen programmiert.

#### 3.3. Modellierung
Für die Modellierung kommen folgende Diagrammtypen zum Einsatz

##### 3.3.1. Use cases 
Mit Hilfe des Use-Case-Diagramms werden die Anwendungsfälle modelliert.

##### 3.3.2. Datenmodellierung/Klassendiagramm
Als Basis für die Programmierung sind vor Beginn Klassendiagramme für die geplanten Klassen zu entwerfen.

##### 3.3.3. Relationen der Entitäten
Über ER-Diagramme werden die Relationen zwischen den Entitäten visaualisiert.  
Neben den Entitäten und den Relationen werden die Attribute und Schlüsselattribute erfasst.

##### 3.3.4. Komponentendiagramm
Sämtliche für den Einsatz der Software erforderlichen Systemkopmpoponenten werden in Komponentendiagrammen dargestellt.

##### 3.3.5. Programmablauf
Ein Ablaufdiagramm visualisiert den Programmablauf für jede zu entwickelnde Komponente.

##### 3.3.6. Programmablauf
Für die Darstellung der Bereitsellung von Systemkomponenten kommt das Deployment-Diagramm zur Anwendung.

#### 3.4. Datenmodelle
Die Stamm- und Bewegungs-Daten werden in einer relationalen SQLite-Datenbank in Tabellen gespeichert.  
Daten aus Dritt-Systemen werden über APIs ausgelesen.  
Über das Komponentendiagramm wird die IT-Systemlandschaft dargestellt. ER-Diagramme veranschaulichen das Datenmodell.

#### 3.5. Datenplausibilität
Alle Eingaben der Containernummer werden auf Plasubilität geprüft.

### 4. Steuerung 

### 5. Verarbeitung

#### 5.1. Bedingungen zur Verarbeitung

### 6. Protokollierung

### 7. Qualitätssicherung 

#### 7.1. Programmierrichtlinien

#### 7.2. Tests

### 8. Implementierungskonzept

#### 8.1 DevOps-Ansatz

##### 8.1.1. Build

##### 8.1.2. Test

##### 8.1.3. Relese/Paket-Repository

##### 8.1.4. Deploy

##### 8.1.5. Monitor
Auswerten und Bewerten der erfassten und verarbeiteten Daten mittels new relic oder Grafana
