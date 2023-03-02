# Projekt-Dokumentation

Pantic

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|   11.01.2023    | 0.0.1   |Erste Version der Doku, Punkte 0 bis und mit 3 behandelt.  |
|   26.01.2023    | 0.0.2   |UserStories zur Projektidee formuliert, ersten "Prototypen" erstellt.                                                              |
|   21.02.2023    | 0.0.3   |UserStories fertiggestellt, Mockup erstellt,                                                              |
| 23.02.2023 | 0.0.4   | Konzeptionelles Datenmodell erstellt, implementation des GUI's |
| 25.02.2023 | 0.0.5   | GUI fertig implementiert. |
| 28.02.2023 | 0.0.6   | Datenbank eingebunden und mit 6 Beispieldatensätzen gefüllt,  begonnen mit der Darstellung in die Tabellen. |
| 02.03.2023 | 1.0.0   | Programm mittels Testfällen getestet, Demovideo gemacht und abgegeben. |

# 0 Ihr Projekt

Ich habe mir vorgestellt ein "Bibliotheksverwaltungssystem" zu entwickeln, welches Benutzern Bücher herausgeben kann und dem Benutzer generelle Informationen über das Werk liefert (Titel, Autor, Erscheinungsdatum, Sprache, Seitenzahl, Verlag etc.).Ich möchte probieren dieses Projekt in Form einer ASP.Net MVC Webapplikation zu realisieren.

# 1 Analyse



* Tier 1 (Presentation): User interface
* Tier 2 (Webserver):              
* Tier 3 (Application Server): Logik
* Tier 4 (Dataserver): Datenbank

# 2 Technologie
* Presentaion Tier: ASP.Net WebForms, Bootstrap
* Business Tier: C# Klassen
* Persistenz Tier: MySql MVC items

# 3 Datenbank
Zum Erstellen und Befüllen meiner MySql Datenbank habe ich Xaamp und PHPMyAdmin verwendet, diese Datenbank habe ich dann mittels eines Connection-Strings in mein Projekt in Visual Studio eingebunden. Zum Einbinden brauchte es noch ein Nuget-Package namens MySql.Data, welches man ganz einfach mit dem Package-Manager installieren kann.



# 4.1 User Stories



| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |    Kann         | Funktional     | Als Kunde möchte ich ein Benutzerkonto erstellen können, um Zugriff auf die Plattform zu erhalten.  |
| 2    |    Kann         | Funktional     |  Als Kunde möchte ich mich mit einem bereits bestehenden Benutzerkonto anmelden können, um Zugriff auf die Plattform zu                                                  erhalten.|
| 3    |    Muss      | Funktional     | Als Kunde möchte ich ein Buch anklicken können , damit ich weitere Informationen (Autor, Erscheinungsjahr, Genre, Verlag und Sprache) über das Werk erhalten kann. |
| 4    |    Kann         | Funktional     | Als Bibliothekar möchte ich mich mit einem "Administrator" Konto anmelden können, damit ich Bücher hinzufügen und entfernen kann. |
| 5    |    Muss         | Funktional     | Als Kunde möchte ich ein Buch ausleihen können, damit ich dieses über einen bestimmten Zeitraum hinweg lesen kann.   |
| 6    |    Muss         | Funktional     | Als Kunde möchte ich eine Bestätigungsemail nach dem Ausleihen auf die Email Adresse meines Benutzerkontos erhalten. |
| 7    |    Kann        | Funktional     | Als Bibliothekar möchte möchte ich sehen können wann, welche Werke, von welchen Kunden ausgeliehen worden sind und wann                                                 diese zurückgebracht werden müssen, damit ich sehe, ob noch welche Bücher überfällig sind.    |
| 8    |    Muss             | Funktional     | Als Kunde möchte ich eine Liste der von mir ausgeliehnen Bücher einsehen können, damit ich sehen kann welche Werke ich                                                 ausgeliehen habe und weiss wann ich diese wieder zurückbringen muss. |
| 9    |    Kann             | Funktional     | Als Kunde möchte ich mein Profil einsehen können, damit ich auf Wunsch meine Zugangsdaten (Passwort und Email) ändern                                                   kann. |
| 10    |   Kann             | Qualität     |  Als Kunde möchte ich einen "Dark-mode" in der Applikation aktivieren können, um meine Augen etwas zu schonen.|
| 11    |    Muss             | Qualität     |Als Kunde möchte ich das die Applikation stabil in der Ausführung läuft.  |
| 12    |    Kann             | Funktional     |Als Kunde möchte ich eine "Errinerungsemail" erhalten, welche mich etwas 2-3 Tage vorher an meine Deadline erinnert. |
| 13    |    Muss             | Funktional     |Als Kunde möchte ich eine Suchleiste benutzen können, damit ich nach meinem gewünschten Werk suchen kann.  |
| 14    |    Kann             | Funktional     |Als Kunde möchte ich verschiedene Filter anwenden können, damit ich ein passendes Buch, welches meinen Vorlieben                                                       entspricht finden kann (Genre, Seitenzahl, Autor, Verlag)  |
| 15    |    Muss             | Funktional     |Als Kunde möchte ich meine ausgeliehenen Bücher verlängern können, falls ich sie nicht rechtzeitig zurückbringen kann.  |
| 16    |    Muss             | Funktional     |Als Kunde möchte ich die Verfügbarkeit eines Buches überprüfen können, damit ich dafür nicht extra zur Bibliothek                                                       laufen muss (ausgeliehen/verfügbar). |
| 17    |    Kann             | Funktional     |Als Kunde möchte ich die Möglichkeit haben nach Büchern auf Englisch suchen zu können, damit ich meine Sprachkenntnisse                                                 verbessern kann.  |
| 18    |    Kann             | Funktional     |Als Kunde möchte ich die Möglichkeit haben mir meine ausgeliehenen Werke per Post nachhause schicken zu können, damit ich                                                 nicht extra zur Bibliothek muss, um dieses abzuholen.  |
| 19    |    Muss             | Funktional     |Als Kunde möchte ich die Möglichkeit haben eine Rezension zu einem Werk zu hinterlassen, um zukünftigen Lesern einen                                                   Ratschlag hinterlassen zu können. |
| 20    |    Muss             | Rand            | Als Kunde möchte ich die Applikation ab dem 2. März 2023 benutzen können, damit ich nicht mehr am Schalter Schlange                                                      stehen muss. |



# 4.2 Testfälle

| TC-№ | Vorbereitung                      | Eingabe                 | Erwartete Ausgabe                                            |
| ---- | --------------------------------- | ----------------------- | ------------------------------------------------------------ |
| 3.1  | Projekt in Visual Studio geöffnet | Projekt Starten         | Hauptseite mit den verschiedenen Büchern und Informationen wird angezeigt. |
| 5.1  | Projekt in Visual Studio geöffnet | Projekt Starten         | Hauptseite min den verschiednen Büchern wird geladen und unter jedem Buch wird ein Knopf namens "Ausleihen" angezeigt. |
| 16.1 | Programm ist geöffnet             | Auf "Ausleihen" klicken | "Status" ändert sich zu "ausgeliehen"                        |



# 5 Prototyp



![Screenshot 2023-02-23 110905](https://user-images.githubusercontent.com/69889967/220878714-5cc0bd5f-36a8-4e40-9aca-8bcbd4f79ad1.png)




# 6 Implementation



| User Story | Datum      | Beschreibung                                                 |
| ---------- | ---------- | ------------------------------------------------------------ |
| 3          | 22.02.2023 | Erstellen des GUI-Mockups, Erstellen eines konzeptionellen Datenmodells, Implementation des GUI's |
| 3          | 25.02.2023 | Fertigstellen des GUI's, Erstellen der Datenbank,            |
| 3          | 28.02.2023 | Eibinden der Datenbank und Befüllung mit Beispieldatensätzen |
| 5,16       | 01.03.2023 | Erstellen des Buttons und der Funktion zur Ausleihe,  Enum für den Status des Buchs (ausgeliehen/verfügbar) implementiert. |

# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung               |
| ---- | --------- | ------------------------------------------------------- |
| 3    | nein      | Im Moment wird nur ein buch aus der Datenbank angezeigt |
| 5    | Ja        | -                                                       |
| 16   | nein      | Noch nicht implementiert                                |

# 8 Testprotokoll



| TC-№   | Datum      | Resultat | Tester      |
| ------ | ---------- | -------- | ----------- |
| 3.1.1  | 02.03.2023 | NOK      | Luka Pantic |
| 5.1.1  | 02.03.2023 | OK       | Luka Pantic |
| 16.1.1 | 02.03.2023 | NOK      | Luka Panitc |

Produkt ist noch nicht auslieferberit, da recht vieles noch nicht implementiert ist.

# 9 `README.md`



# 10 Allgemeines

- [x] Ich habe die Rechtschreibung überprüft
- [x] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [x] Ich habe alle mit ✍️ markierten Teile ersetzt
