# qual-o-mat-kiss

Dieses Repository enthält einen simplen POC (Proof of concept) eines "Wahl-*tools*". In der Standardeinstellung wird die Datenbasis von [qual-o-mat-data](https://github.com/gockelhahn/qual-o-mat-data) verwendet.

## Preview

Man kann sich [hier](https://gockelhahn.github.io/qual-o-mat-kiss/) immer die aktuelle Version anzeigen lassen.

## Setup

Da es sich bei dieser Seite um reines HTML(5) und clientseitiges JavaScript handelt, braucht man die Dateien einfach nur auf einen Webserver legen und die *index.html* im Browser aufrufen.

## Konfiguration

In der Datei *[js/common.js](js/common.js)* wird mit der Variable **data_url** die Herkunft der zu benutzenden Daten definiert.
```javascript
var data_url = 'https://raw.githubusercontent.com/gockelhahn/qual-o-mat-data/master';
```
Für selbst gehostete Daten kann man auch einen relativen Pfad setzen.

## Offline Modus

Natürlich kann man das Ganze auch ohne Webserver von einem lokalen Medium laden. Dazu einfach alle Dateien in einen Ordner legen und die oben genannte Variable auf einen relativen Pfad setzen, z.B.:
```javascript
var data_url = 'data';
```
In diesem Unterordner müssen dann die Daten, die man verwenden möchte, abgelegt werden.

**Hinweis**:
Da Chromium/Chrome XMLHttpRequest (XHR) auf "file:///" defaultmäßig verbietet, muss man den Browser für eine funktionierende Offline-Unterstützung mit dem folgenden Parameter starten:
```
--allow-file-access-from-files
```

## Lizenz

Für alle Dateien in diesem Repository gilt folgende [Lizenz](LICENSE).
