# Dokumentation
## Teamname  
Team Pareto
## Projektname
ParetoTrack
## Version
0.1
## Einleitung
## Einleitung
- Vorstellen der Software
- Zweck und Nutzen der SW

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


Software auf dem Client


## Methodisches Vorgehen in der SW-Entwicklung und in der Projektarbeit


### Software-Stack

#### auf dem Server
Python 3.10
MySQL-Server

#### auf dem Client
Webbrowser „Google Chrome“ oder „Microsoft Edge“ oder „Mozilla Firefox“ oder „Apple Safari“ bzw. Webbrowser mit der aktuellesten Version der Blink-Engine oder Chromium-Engine oder Edge-HTML oder WebKit-Enging oder Mozilla-Engine

## Voraussetzungen

### Hardware


## Beschreibung des DevOps

### CI/CD
- Was ist datunter zu verstehen?
- Wie wird CI/CD in unserem Projekt umgesetzt?

### Build-Prozess

### Deploy-Prozess

## Automatisiertes Testen

## Monitoring
- mittels Datadog (eine Beschreibung hierfür bekommst Du noch)

## Fazit/Ausblick
- Welcher Stand wurde erreicht? 
- Welche Funktionalitäten sind im aktuellen Stand enthalten?
- Welche Funktionalitäten müssen/sollten in zukünftigen Versionen noch implementiert werden?
- Welche Funktionalitäten werden nicht unterstützt (Abgenzung)?
