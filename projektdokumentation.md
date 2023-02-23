# Projekt-Dokumentation

Pantic

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|   11.01.2023    | 0.0.1   |Erste Version der Doku, Punkte 0 bis und mit 3 behandelt.  |
|   26.01.2023    | 0.0.2   |UserStories zur Projektidee formuliert, ersten "Prototypen" erstellt.                                                              |
|   21.02.2023    | 0.0.3   |UserStories fertiggestellt, Mockup erstellt, login implementiert.                                                              |
|       | 0.0.4   |                                                              |
|       | 0.0.5   |                                                              |
|       | 0.0.6   |                                                              |
|       | 1.0.0   |                                                              |

# 0 Ihr Projekt

Ich habe mir vorgestellt ein "Bibliotheksverwaltungssystem" zu entwickeln, welches Benutzern Bücher herausgeben kann und dem Benutzer generelle Informationen über das Werk liefert (Titel, Autor, Erscheinungsdatum, Sprache, Seitenzahl, Verlag etc.).Ich möchte probieren dieses Projekt in Form einer ASP.Net MVC Webapplikation zu realisieren.

# 1 Analyse

✍️ Beschreiben Sie, auf welchem Tier Sie die dynamischen Elemente der Anwendung unterbringen möchten:

* Tier 1 (Presentation): User interface
* Tier 2 (Webserver):              
* Tier 3 (Application Server): Logik
* Tier 4 (Dataserver): Datenbank

# 2 Technologie
* Presentaion Tier: ASP.Net WebForms, Bootstrap
* Business Tier: C# Klassen
* Persistenz Tier: MySql MVC items

# 3 Datenbank
✍️ Wie steuern Sie Ihre Datenbank an? Wie ist das Interface aufgebaut? 

# 4.1 User Stories

✍️ Formulieren Sie klare Anforderungen in der Form von User Stories (*„als … möchte ich … damit …“*) und zu jeder Anforderung mindestens einen dazugehörigen Testfall (in Kapitel 4.2). 

✍️ Formulieren Sie weitere, eigene Anforderungen und Testfälle, wie Sie Ihre Applikation erweitern möchten. Geben Sie diesen statt einer Nummer einen Buchstaben (`A`, `B`, etc.)

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |    Muss             | Funktional     | Als Kunde möchte ich ein Benutzerkonto erstellen können, um Zugriff auf die Plattform zu erhalten.  |
| 2    |    Muss             | Funktional     |  Als Kunde möchte ich mich mit einem bereits bestehenden Benutzerkonto anmelden können, um Zugriff auf die Plattform zu                                                  erhalten.
| 3    |    Muss             | Funktional     | Als Kunde möchte ich ein Buch anklicken können , damit ich weitere Informationen (Autor, Erscheinungsjahr, Genre,                                                       Verlag und Sprache) über das Werk erhalten kann.  |
| 4    |    Muss             | Funktional     |  Als Bibliothekar möchte ich mich mit einem "Administrator" Konto anmelden können, damit ich Bücher hinzufügen und                                                      entfernen kann. |
| 5    |    Muss             | Funktional     | Als Kunde möchte ich ein Buch ausleihen können, damit ich dieses über einen bestimmten Zeitraum hinweg lesen kann.   |
| 6    |    Kann             | Funktional     | Als Kunde möchte ich eine Bestätigungsemail nach dem Ausleihen auf die Email Adresse meines Benutzerkontos erhalten. |
| 7    |    Muss             | Funktional     | Als Bibliothekar möchte möchte ich sehen können wann, welche Werke, von welchen Kunden ausgeliehen worden sind und wann                                                 diese zurückgebracht werden müssen, damit ich sehe, ob noch welche Bücher überfällig sind.    |
| 8    |    Muss             | Funktional     | Als Kunde möchte ich eine Liste der von mir ausgeliehnen Bücher einsehen können, damit ich sehen kann welche Werke ich                                                 ausgeliehen habe und weiss wann ich diese wieder zurückbringen muss. |
| 9    |    Kann             | Funktional     | Als Kunde möchte ich mein Profil einsehen können, damit ich auf Wunsch meine Zugangsdaten (Passwort und Email) ändern                                                   kann. |
| 10    |   Kann             | Qualität     |  Als Kunde möchte ich einen "Dark-mode" in der Applikation aktivieren können, um meine Augen etwas zu schonen.|
| 11    |    Muss             | Qualität     |Als Kunde möchte ich das die Applikation stabil in der Ausführung läuft.  |
| 12    |    Kann             | Funktional     |Als Kunde möchte ich eine "Errinerungsemail" erhalten, welche mich etwas 2-3 Tage vorher an meine Deadline erinnert. |
| 13    |    Muss             | Funktional     |Als Kunde möchte ich eine Suchleiste benutzen können, damit ich nach meinem gewünschten Werk suchen kann.  |
| 14    |    Kann             | Funktional     |Als Kunde möchte ich verschiedene Filter anwenden können, damit ich ein passendes Buch, welches meinen Vorlieben                                                       entspricht finden kann (Genre, Seitenzahl, Autor, Verlag)  |
| 15    |    Muss             | Funktional     |Als Kunde möchte ich meine ausgeliehenen Bücher verlängern können, falls ich sie nicht rechtzeitig zurückbringen kann.  |
| 16    |    Muss             | Funktional     |Als Kunde möchte ich die Verfügbarkeit eines Buches überprüfen können, damit ich dafür nicht extra zur Bibliothek                                                       laufen muss. |
| 17    |    Kann             | Funktional     |Als Kunde möchte ich die Möglichketi haben nach Büchern auf Englisch suchen zu können, damit ich meine Sprachkenntnisse                                                 verbessern kann.  |
| 18    |    Kann             | Funktional     |Als Kunde möchte ich die Möglichkeit haben mir meine ausgeliehnen Werke per Post nachhauseschicken zu können, damit ich                                                 nicht extra zur Bibliothek muss, um dieses abzuholen.  |
| 19    |    Muss             | Funktional     |Als Kunde möchte ich die Möglichkeit haben eine Rezenssion zu einem Werk zu hinterlassen, um zukünftigen Lesern einen                                                   Ratschlag hinterlassen zu können. |
| 20    |    Muss             | Rand            | Als Kunde möchte ich die Applikation ab dem 2. März 2023 benutzen können, damit ich nichtmehr am Schalter schlange                                                      stehen muss.  |

✍️ Jede User Story hat eine ganzzahlige Nummer (1, 2, 3 etc. oder Zahl), eine Verbindlichkeit (Muss oder Kann?), und einen Typ (Funktional, Qualität, Rand). 

# 4.2 Testfälle

| TC-№ | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  |              |         |                   |
| ...  |              |         |                   |

✍️ Die Nummer hat das Format `N.m`, wobei `N` die Nummer der User Story ist, die der Testfall abdeckt, und `m` von `1` an nach oben gezählt. Beispiel: Der dritte Testfall, der die zweite User Story abdeckt, hat also die Nummer `2.3`.

# 5 Prototyp

✍️ Erstellen Sie Prototypen für das GUI (Admin-Interface und Quiz-Seite).



# 6 Implementation

✍️ Halten Sie fest, wann Sie welche User Story bearbeitet haben

| User Story | Datum | Beschreibung |
| ---------- | ----- | ------------ |
| ...        |       |              |

# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1    | ja / nein |                                           |
| ...  |           |                                           |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

# 9 `README.md`

✍️ Beschreiben Sie ausführlich in einer README.md, wie Ihre Applikation gestartet und ausgeführt wird. Legen Sie eine geeignete Möglichkeit (Skript, Export, …) bei, Ihre Datenbank wiederherzustellen.

# 10 Allgemeines

- [ ] Ich habe die Rechtschreibung überprüft
- [ ] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [ ] Ich habe alle mit ✍️ markierten Teile ersetzt
