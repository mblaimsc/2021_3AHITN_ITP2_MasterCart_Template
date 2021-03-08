# Einkaufslisten App "MasterCart":

Zu Programmieren ist eine Einkaufslisten - App.

## Erklärung
Hierfür ist zuerst ein Backend zu programmieren, welches die entsprechenden Befehle empfängt, verarbeitet und eine Antwort zurückschickt.
Das Backend wird über einen HTTP - Server abgebildet, welcher selbst in JAVA Programmiert wird.
Das Frontend wird als Angularanwendung programmiert.

Der Server liefert die Daten über eine REST - API (REST ... Representational State Transfer) im JSON - Format an die Angular Anwendung.

###  Wie funktioniert REST-API?
>Die „Representational State Transfer - Application Programming Interface“ (REST-API) ist eine Programmier-Schnittstelle, die den Austausch von Daten auf verteilten Systemen - insbesondere für Web-Services - ermöglicht.
> Die Programmierschnittstelle REST-API nutzt HTTP-Anfragen, um per PUT, GET, POST und DELETE auf Informationen zuzugreifen. Da REST das Verbinden mit Cloud-Diensten erlaubt und eine Interaktion ermöglicht, ist sie meist die erste Wahl. So sind REST-APIs zum Beispiel für Twitter, Amazon und Google im ständigen Einsatz. Und AWS, VMware, Azure und andere Cloud-Anbieter setzen fast ausschließlich auf REST. <br/> Mehr dazu: https://www.datacenter-insider.de/was-ist-rest-api-a-714434

### Wie funktioniert HTTP?
> Die Kommunikation findet nach dem Client-Server-Prinzip statt. Der HTTP-Client (Browser) sendet seine Anfrage (HTTP-Request) an den HTTP-Server (Webserver/Web-Server). Dieser bearbeitet die Anfrage und schickt seine Antwort (HTTP-Response) zurück. Nach der Antwort durch den Server ist diese Verbindung beendet. Typischerweise finden gleichzeitig mehrere HTTP-Verbindungen statt.<br />
Mehr dazu: https://www.elektronik-kompendium.de/sites/net/0902231.htm

Eine einfache Umsetzung eines HTTP Servers kann hier gefunden werden: https://ssaurel.medium.com/create-a-simple-http-web-server-in-java-3fc12b29d5fd

## Schnittstellen
Hierfür werden folgende CRUD (Create, Read, Update, Delete) - Schnittstellen am Server vorgesehen:
- Hinzufügen eines neuen Items zur Einkaufsliste 	... POST Request an http(s)://<serveradresse>:<port>/create
- Laden eines speziellen Items von der Einkaufsliste 	... GET Request an http(s)://<serveradresse>:<port>/read/<id des Items>
- Bearbeiten eines bestehenden Items 			... POST Request an http(s)://<serveradresse>:<port>/update/<id des Items>
- Löschen eines bestehenden Items von der Einkaufsliste ... DELETE Request an http(s)://<serveradresse>:<port>/delete/<id des Items>
- Laden der aller Items in der Einkaufsliste 		... GET Request an http(s)://<serveradresse>:<port>/read/all

Wenn eine nicht vorhandene URL aufgerufen wird, oder eine falsche HTTP Methode verwendet wird (z.B. POST anstelle von DELETE), so soll ein Fehler mit dem Fehlercode 404 bzw. 405 vom Server geliefert werden. 

## Zeitplan
- Woche 1 (08.03.2021 - 14.03.2021): Grundsätzliches Entwickeln eines Java HTTP Servers
- Woche 2 (05.03.2021 - 21.03.2021): Implementieren der jeweiligen REST - Schnittstellen am HTTP Server
- Woche 3 (22.03.2021 - 28.03.2021): Implementieren der jeweiligen REST - Schnittstellen am HTTP Server
- Woche 4 (05.04.2021 - 11.04.2021): Grundsätzlicher Entwurf einer Angular Anwendung
- Woche 5 (12.04.2021 - 18.04.2021): Implementieren der jeweiligen REST - Schnittstellen in der Angular Anwendung
- Woche 6 (19.04.2021 - 21.04.2021): Überarbeitung, Abgabe am Ende der Stunde (21.04.2021)

## Dokumentation
Die Dokumentation des Projekts (Zusammenfassung der Tätigkeiten in den einzelnen Unterrichtseinheiten, Beschreibung des Backends, Beschreibung des Frontends, ...) wird im Markdown Format in Form einer README[]().md im Github Repository im jeweiligen Ordner geführt.

## Abgabe
Die Abgabe erfolgt über Github. Erzeugen Sie hierfür ein neues Repository (Owner HTL-Steyr). Als Vorlage wählen Sie folgendes Template: 2021_3AHITN_ITP2_MasterCart_Template.
Der Name des Repositories lautet wie folgt: 2021_3AHITN_ITP2_<Ihr HTL Steyr Benutzername>_MasterCart


Im Template sind zwei Ordner enthalten: 
- Frontend: Hier wird das Frontend (= Angular Anwendung) hochgeladen. Das Verzeichnis beinhaltet bereits eine .gitignore Datei, welche für Angular - Anwendungen optimiert ist: https://www.toptal.com/developers/gitignore/api/angular
- Backend: Hier wird das Backend (= Java Server) hochgeladen. Das Verzeichnis beinhaltet bereits eine .gitignore Datei, welche für Java Anwendungen mit IntelliJ optimiert ist: https://www.toptal.com/developers/gitignore/api/intellij
