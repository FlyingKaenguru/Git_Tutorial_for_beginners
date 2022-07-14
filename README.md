# Git_Tutorial_for_beginners


1. Erstelle ein "Repository" (Projekt) mit einem Git-Hosting-Tool (z. B. Github / Gitlab).
* Melde dich hierfür bei deinem Git-Hosting-Tool an und klicke auf neues Repository erstellen
* Vergebe einen Namen

2. Klonst das Repository auf dein lokales System.
* Die werden zwei Möglichkeiten zum klonen des Repos angeboten - https und ssh

*Für ssh musst du deinen Publickey im Git-Hosting-Tool hinterlegen - !unser levigo-Gitlab spricht nur ssh innerhalb des Firmengebäudes - VPN geht nicht*

3. Wechsel in den geklonten Ordner
* Hier findest du bereits einen Unterordner mit dem Namen ".git". 

*Der Ordner .git enthält alle Informationen, die für das Projekt erforderlich sind, 
sowie alle Informationen über Commits, die Adresse des entfernten Repositorys usw.*

4. Erstelle eine README.md Datei und schreibe "Hello World" rein. 
5. Schau die deine Änderungen an:
* git status
* git diff

6. Stage und Committe deinen Änderung
* git add . oder git add README.md
* git commit -m "added README.md"

7. Sende deinen neuen Commit an den Remote Server
* git push

8. Schau dir deine Änderungen in deinem Git-Hosting-Tool an. Klicke dafür auf den letzten Commit.

9. Bearbeite deine README.md Datei im Git-Hosting-Tool:
* Ändere den Inhalt ("Hallo World" in "This is a tutorial") 
* Füge noch eine zusätzliche Zeile hinzu

10. Schau dir deine Änderungen in deinem Git-Hosting-Tool an. Klicke dafür auf den letzten Commit. 
* Deine bearbeitete Zeile wird nun rot angezeigt - entfernt 
* Der neue Inhalt wird grün angezeigt

11. Führe lokal einen "Pull" durch, um die Änderungen auf dein lokales System zu übernehmen.

12. Erstelle lokal einen neuen Branch. 
* git checkout -b <branch_name>

oder 

* git branch <branch_name>
* git checkout <branch_name> 

**Warum sind Branches sinvoll?** 
* Im Team kann unabhängig voneinander gearbeitet werden
* Der Master-Branch ist der Produktiv-Branch (Kunden) der immer lauffähig sein muss (sollte) - Änderungen des lauffähigen Codes können gefahrlos auf einem Branch getestet werden

13. Nimm eine Änderung vor, führe einen Commit dafür durch und pushe die Änderung an den Server.
* ! Es können auch mehrere Commits gleichzeitig gepushed werden. Ein Push nach jedem Commit ist nicht notwendig
* git push --set-upstream origin <branch_name>

14. Vergleiche in deinem Git-Hosting-Tool die beiden Branches miteinander. Wechsel dafür zwischen den Branches hin und her und schau dir die Änderungen an.

15. Eröffne in deinem Git-Hosting-Tool ein "Pull-Request".

**Ziel eines Pull Requests ist:**
Änderungen aus einem Branch in einen anderen Branch zu übernehmen (in der Regel in den Master-Branch).
Ein Pull-Request ist nicht zwingend notwendig für das Zusammenführen zweier Branches, es ist jedoch ein Hilfreiches Tool für die Teamarbeit.
Mit einem Pull-Request kann ein Entwickler Teammitglieder über die Fertigstellung eines Features informieren. 
So wissen alle Beteiligten, dass der Code reviewt und in den Master-Branch gemergt werden muss. Jeder kann nun die Änderung begutachten und letzte Bedenken, Fehler mitteilen.
Wurden zwei Stände zusammengeführt, spricht man von einem "Merge"

**Warum sind Pull-Requests sinnvoll?**
* Teammitglieder sind immer auf dem aktuellen Stand
* Teammitglieder können frühzeitig reagieren, wenn ihre Entwicklung auf etwas aufbaut, was in dem zu mergenden Branch gelöscht/verändert wurde
* Fehler können frühzeitig gefunden werden bevor sie an den Kunden gehen

16. Führe einen "Merge" deiner Änderungen durch.
