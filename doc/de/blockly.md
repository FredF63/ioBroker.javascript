---
title:       "ioBroker Blockly"
lastChanged: "13.06.2019"
---

>! Achtung Seite ist im Aufbau

# Inhaltsverzeichnis

* [Beschreibung](#beschreibung)
* [Editorfenster](#editorfenster)
* [Blöcke im einzelnen](#blöcke-im-einzelnen)
	* [System](#system)

        [![Debug output](img/01system/110debug.PNG)](#debug)

		[![Comment](img/01system/120kommentar.PNG)](#kommentar)

		[![Steuere Zustand](img/01system/130steuern.PNG)](#steuere-zustand)

		[![Zustand umschalten](img/01system/140umschalten.PNG)](#zustand-umschalten)

		[![Zustand aktualisieren](img/01system/150aktualisieren.PNG)](#aktualisiere-zustand)

		[![Binde zwei Zustände](img/01system/160binden.PNG)](#binde-zwei-zustände)

		[![Schreibe Zustand](img/01system/170schreiben.PNG)](#schreibe-zustand)

		[![Datenpunkt erzeugen](img/01system/180datenpunkterzeugen.PNG)](#datenpunkt-erzeugen)

		[![Wert eines Datenpunktes](img/01system/190werterzeugen.PNG)](#wert-eines-datenpunktes-1)

		[![Wert](img/01system/200werterzeugen.PNG)](#wert-eines-datenpunktes-2)

		[![Wert](img/01system/210wert.PNG)](#wert-eines-datenpunktes-3)

		[![Objekt ID auswählen](img/01system/220objekt.PNG)](#objekt-id)

		[![Attribut](img/01system/230attribut.PNG)](#attribut)

	* [Aktionen](#aktionen)

		[![Systembefehl ausführen](img/02aktionen/210.PNG)](#exec-kommando)

		[![URL abfragen](img/02aktionen/220.PNG)](#request-url)

	* [SendTo](#sendto)

		[![An telegram senden](img/.PNG)](#an-telegram-etwas-senden)

		[![An SayIt senden](img/.PNG)](#send-to-sayit)

		[![An pushover senden](img/.PNG)](#send-to-pushover)

		[![email versenden](img/.PNG)](#send-email)

		[![Einem Adapter etwas senden](img/.PNG)](#custom-sendto-block)

	* [Datum und Zeit](#datum-und-zeit)

		[![Zeit vergleichen](img/.PNG)](#time-comparision)

		[![Aktuelle Zeit vergleichen](img/.PNG)](#actual-time-comparision)

		[![Aktuelle Zeit im gewünschten Format erhalten](img/.PNG)](#get-actual-time-im-specific-format)

		[![Aktuelle Zeit eines Astro Ereignisses erhalten](img/.PNG)](#get-time-of-astro-events-for-today)

	* [Konvertierung](#konvertierung)

		[![Nach Zahl konvertieren](convert-to-number)

		[![Nach Logikwert konvertieren](convert-to-boolean)

		[![Nach String konvertieren]

		[![Get type of variable]

		[![Nach Datum/Zeit konvertieren](convert-to-datetime-object)

		[![Datum/Zeit Objekt nach String konvertieren](convert-datetime-object-to-string)

		[![JSON nach Objekt konvertieren](convert-json-to-object)

		[![Objekt nach JSON konvertieren](convert-object-to-json)

	* [Trigger](#trigger)

		[![Trigger bei mehreren Zustandswechsel](img/.PNG)](#trigger-on-states-change)

		[![Trigger bei einem Zustandswechsel](img/.PNG)](#trigger-on-state-change)

		[![Trigger info](img/.PNG)](#trigger-info)

		[![Zeitplan](img/.PNG)](#schedule)

		[![Trigger für Astro-Ereignis](img/.PNG)](#trigger-on-astro-event)

		[![Benannter Zeitplan](img/.PNG)](#named-schedule)

		[![Lösche benannten Zeitplan](img/.PNG)](#clear-schedule)

		[![CRON mit Dialogfenster](img/.PNG)](#cron-dialog)

		[![CRON Regeln](img/.PNG)](#cron-rule)

	* [Timeouts](#timeouts)

		[![Ausführung Verzögern](img/.PNG)](#delayed-execution)

		[![verzögerte Ausführung beenden](img/.PNG)](#clear-delayed-execution)

		[![Interval ausführen](img/.PNG)](#execution-by-interval)

		[![ausgeführtes Interval beenden](img/.PNG)](#stop-execution-by-interval)

	* [Logik](#logik)

		[![Falls mache](img/.PNG)](#if-else-block)

		[![Vergleichen](img/.PNG)](#comparision-block)

		[![Und/Oder](img/.PNG)](#logical-and-or-block)

		[![Negieren](img/.PNG)](#negation-block)

		[![Wahr/Falsch](img/.PNG)](#logical-value-true-false)

		[![Null](img/.PNG)](#null-block)

		[![Logik prüfen](img/.PNG)](#test-block)

	* [Schleifen](#schleifen)

		[![Wiederhole n-mal](img/.PNG)](#repeat-n-times)

		[![Wiederhole solange/bis](img/.PNG)](#repeat-while)

		[![Zähle](img/.PNG)](#count)

		[![For each]

		[![Schleife abbrechen](img/.PNG)](#break-out-of-loop)

	* [Mathematik](#mathematik)

		[![Zahlenwert](img/.PNG)](#number-value)

		[![Rechnen mit zwei Zahlen](img/.PNG)](#arithmetical-operations)

		[![Wurzel, Betrag](img/.PNG)](#square-root-abs---ln-log10-e-10)

		[![Trigonometrie](img/.PNG)](#sin-cos-tan-asin-acos-atan)

		[![Konstanten: pi, e, phi, sqrt(2), sqrt(1/2), infinity](img/.PNG)](#math)

		[![Zahl prüfen](img/.PNG)](#is-even-odd-)

		[![Variable Wert verändern](img/.PNG)](#modify-variably-by-value-plus-or-minus)

		[![Runden](img/.PNG)](#round-floor-ceil-value)

		[![Runden mit angabe der Nachkommastelle]

		[![Wert aus Liste berechnen]

		[![Rest nach Division (Modulus)]

		[![Zahl mit min und max begrenzen](img/.PNG)](#limit-some-value-by-min-and-max)

		[![ganzzahlige Zufallszahl](img/.PNG)](#random-value-between-min-and-max)

		[![Zufallszahl zwischen 0 und 1](img/.PNG)](#random-value-from-0-to-1)

	* [Text](#text)

		[![Zeichenfolge](img/.PNG)](#string-value)

		[![Zeilenumbruch](img/.PNG)](#zeilenumbruch)

		[![Zeichenfolgen verketten](img/.PNG)](#concatenate-strings)

		[![Zeichenfolge an Variable anhängen](img/.PNG)](#append-string-to-variable)

		[![Länge einer Zeichenfolge](img/.PNG)](#length-of-string)

		[![Ist Zeichenfolge leer](img/.PNG)](#is-string-empty)

		[![Suche Position einer Zeichenfolge](img/.PNG)](#find-position-in-string)

		[![Erhalte das Symbol in einer Zeichenfolge an bestimmter Position](img/.PNG)](#get-symbol-string-specific-position)

		[![Erhalte Abschnitt einer Zeichenfolge](img/.PNG)](#get-substring)

		[![In Groß- oder Kleinbuchstabe konvertieren](img/.PNG)](#Convert-to-upper-case-or-to-lower-case)

		[![Leerzeichen entfernen](img/.PNG)](#trim-string)

	*  [Listen](#listen)

		[![Erzeuge leere Liste](img/.PNG)](#create-empty-list)

		[![Erzeuge Liste mit Werten](img/.PNG)](#create-list-with-values)

		[![Erzeuge Liste mit gleichem Wert n-mal](img/.PNG)](#create-list-with-same-value-n-times)

		[![Elementanzahl einer Liste ausgeben](img/.PNG)](#get-length-of-list)

		[![Ist Liste Leer](img/.PNG)](#is-list-empty)

		[![Suche Position eines Elements in Liste](img/.PNG)](#Find-position-of-item-in-list)

		[![Erhalte Element einer Position](img/.PNG)](#get-item-in-list)

        [![Setze Element einer Position](img/.PNG)](#set-item-in-list)

		[![Erhalte Teilliste einer Liste](img/.PNG)](#get-sublist-of-list)

		[![Text in Liste und umgekehrt konvertieren](img/.PNG)](#convert-text-to-list-and-vice-versa)

		[![Liste sortieren]

	* [Farbe](#farbe)

		[![Farbe](img/.PNG)](#colour-value)

		[![Zufällige Farbe](img/.PNG)](#random-colour)

		[![Farbe nach RGB](img/.PNG)](#rgb-colour)

		[![Farben mischen](img/.PNG)](#mix-colours)

	* [Variablen](#variablen)

		[![Setze Wert einer Variablen](img/.PNG)](#set-variables-value)

		[![Erhalte Wert einer Variablen](img/.PNG)](#get-variables-value)

		[![Addiere zur Variablen](img/.PNG)](#addiere-zur-variablen)

	* [Funktionen](#funktionen)

		[![Erzeuge Funktion *ohne* Rückgabewert](img/.PNG)](#create-function-from-blocks-with-no-return-value)

		[![Erzeuge Funktion *mit* Rückgabewert](img/.PNG)](#create-function-from-blocks-with-return-value)

		[![Return value in function ](img/.PNG)](#return-value-in-function)

		[![Erzeuge javascript Funktion *ohne* Rückgabewert](img/.PNG)](#create-custom-function-with-no-return-value)

		[![Erzeuge javascript Funktion *mit* Rückgabewert](img/.PNG)](#create-custom-function-with-return-value)

		[![Funktion aufrufen](img/.PNG)](#call-function)

* [Beispiele](#beispiele)

	* [1.](#beispiel-1)
	* [2.](#beispiel-2)
	* [3.](#beispiel-3)


# Beschreibung
Blockly ist eine JavaScript-Bibliothek, die einen visuellen Code-Editor anbietet.
Auch ohne Kenntnis einer Programmiersprache ist die Bedienung der grafischen
Blöcke einfach zu erlernen.
Der Blockly-Editor im ioBroker JavaScript-Adapter erlaubt es, Skripte durch
zusammenfügen von grafisch Blöcken per Drag & Drop zu erstellen.


## Editorfenster
Aufruf des Editors erfolgt bei installiertem JavaScript-Adapter im Admin Fenster
Links unter Skripte.

> Falls Skripte nicht sichtbar ist und der JavaScript-Adapter aber installiert
ist, muss über das Dreieck oben links im Admin Fenster der Haken bei
Skripte gesetzt werden.

Beim ersten Start sind die Ordner *global* und *common* bereits angelegt.

> Der Ordner *global* ist nur für Skripte aus reinem JavaScript vorgesehen.
Mit Blockly erstellte Skripte dürfen dort auf __keinen__ Fall abgespeichert
und gestartet werden.

> __Vorsicht:__
Skripte im Ordner _global_ werden zu ___jedem___ Skript als Kopie hinzugefügt
und somit immer mit ausgeführt.

> Der Ordner *global* ist nur bei eingeschalteten Expertenmodus sichtbar.

Die Ordnerstruktur kann nach eigenem Wunsch angelegt werden. Der Speicher-
ort hat keine Auswirkungen auf die Funktionalität eines Skriptes.

Ein Suchfeld erleichtert das Wiederfinden von Skripten.

Damit ein Skript läuft, muss es links in der Ordnerstruktur durch klick auf den
roten Play-Knopf aktiviert werden. Zum Stoppen auf den grünen Pause-Knopf
drücken.
Für jedes Skript wird ein neues Objekt angelegt. Es trägt den Skriptnamen mit
dem Zusatz `_enabled` und liegt im Ordner `javascript.0.ScriptEnabled`.
Das Objekt zeigt mit `true/false` an, ob das Skript läuft. Der Zustand kann auch
gesetzt werden, um ein Skript ein-/auszuschalten.
Im Fenster links ist die Symbolleiste und die Ordner- und Dateileiste zu finden.
Rechts das Editor Fenster mit Block-Sidebar und Arbeitsfläche und unten das
Log-Fenster.

![Editor](img/Start1.png)

Gewünschte Blöcke werden über die verschiedenen [Kategorien](#verfügbare-blöcke) ausgewählt und
per Drag and Drop auf der Arbeitsfläche abgelegt.

Werte oder Inhalte der Blöcke werden über Dropdown Menü oder über Maus
Linksklick geändert.

Mit Maus Rechtsklick über einem Block im Entwurfsfenster werden zusätzliche
Befehle verfügbar:



- _Kopieren:_
Kopiert einen Block und mit ihm verbundene Blöcke und fügt ihn direkt ein.

- _Kommentar hinzufügen:_
Für jeden Block ist es möglich einen Kommentar zu hinterlegen um dessen Funktion
zu beschreiben.

- _interne Eingänge:_
Ändert Ansicht eines Blocks für eine bessere Übersicht.

- _Baustein zusammenfalten:_
um eine bessere Übersicht zu erhalten können Bausteine,zusammengefaltet werden.

- _Baustein deaktivieren:_
Deaktiviert einzelne Blöcke.

- _x Bausteine löschen:_
Löscht einen Block bzw. alle verbundenen Blöcke.

- _Hilfe:_
Ruft die dem Block zugeordnete ioBroker Dokumentation auf. (in Arbeit)



## Blöcke im einzelnen

Blöcke sind im JavaScript-Adapter in Kategorien in folgender Reihenfolge angeordnet:

* [System](#system)
* [Aktionen](#aktionen)
* [Sendto](#sendto)
* [Datum und Zeit](#datum-und-zeit)
* [Konvertrierung](#konvertierung)
* [Trigger](#trigger)
* [Timeouts](#timeouts)
* [Logik](#logik)
* [Schleifen](#schleifen)
* [Mathematik](#mathematik)
* [Text](#text)
* [Listen](#listen)
* [Farbe](#farbe)
* [Variablen](#variablen)
* [Funktionen](#funktionen)



## System



### Debug


![Debug output](img/01system/110debug.PNG)

Schreibt den frei wählbaren Text, hier `test` ins log und dient zum debuggen
eines Scripts wie dies:

![Debug output](img/01system/111debug.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/111code.txt)

Man kann 4 verschiedene Level für die Nachrichten definieren:

* debug
 	*dazu muss der debug-Level der JavaScript Instanz aktiviert sein.*

* info
	*default, zumindest der info log level muss in der JavaScript Instanz aktiviert
    sein.*

* warning
	*fehlt*

* error
	*wird immer angezeigt. Die anderen Level können ignoriert werden, wenn
	es entsprechend in  der JavaScript Instanz eingestellt ist.*


### Kommentar
![Comment](img/01system/120kommentar.PNG)

Ohne weitere Funktion dient dieser Block ausschließlich dazu einen Kommentar für
Erklärungen einzelner Funktionen o.ä. zum Skript hinzuzufügen.

> Pro Kommentar sind max. 48 Zeichen einzeilig sichtbar. Für längere Texte mehrere
> Kommentar Blöcke verwenden und Text aufteilen



### Steuere Zustand
![Steuere Zustand](img/01system/130steuern.PNG)

Steuert den Zustand eines Objektes mit dem gewünschten Status

Typische Anwendung dieses Blocks:

![Steuere Zustand](img/01system/131steuern.PNG)

Die Object ID wird durch Klick ausgewählt. Abhängig vom Typ des Datenpunkts kann
der Wert vom Typ [string](#string-value), [number](#number-value) oder [boolean](#ogical-value-trueflase) sein.

Weitere Erklärungen sind [hier](https://github.com/ioBroker/ioBroker/wiki/Adapter-Development-Documentation#commands-and-statuses) in Englisch zu finden.

Dieser Block schreibt den Befehl in den Datenpunkt mit (ack=false). Zusätzlich
kann eine Verzögerung angegeben werden. Wenn die Verzögerung ungleich 0
ist, wird der Zustand nicht sofort, sondern erst nach dem angegebenen Wert in
Millisekunden, Sekunden oder Minuten gesetzt.

Man kann weitere eventuell vorhandene Verzögerungen für diesen Datenpunkt
löschen, indem man die Checkbox `löschen falls läuft` anklickt.

Im folgenden Beispiel wird der Datenpunkt `Licht` nur einmal nach 2 Sekunden
geschaltet:

![Steuere Zustand](img/01system/132steuern.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/132code.txt)

Hier wird der Zustand von `Licht` zwei mal nach 1 Sekunde __und__ nach 2 Sekunden
geschaltet:

![Steuere Zustand](img/01system/133steuern.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/133code.txt)



### Zustand umschalten
![Zustand umschalten](img/01system/140umschalten.PNG)

Dieser Block schaltet zwischen den Werten um, von true nach false und umgekehrt.



### Aktualisiere Zustand
![Zustand aktualisieren](img/01system/150aktualisieren.PNG)

Dieser Block aktualisiert einen Wert. Es wird kein Befehl zum steuern von Hardware
gesendet.

Typische Anwendung dieses Blocks:
![Zustand aktualisieren](img/01system/151aktualisieren.PNG)



### Binde zwei Zustände
![Binde zwei Zustände](img/01system/160binden.PNG)
Dieser Block bindet zwei Zustände miteinander. Über `nur Änderungen` kann ausgewählt
werden, ob der Wert nur weitergeleitet wird, wenn sich die Quelle ändert, oder
mit jeder Aktualisierung.

Diese Blöcke:

![Binde zwei Zustände](img/01system/161binden.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/161code.txt)

entsprechend mit dem Binde Block:
![Binde zwei Zustände](img/01system/162binden.PNG)



### Schreibe Zustand
![Schreibe Zustand](img/01system/170schreiben.PNG)

Block, der [Aktualisiere Zustand](#aktualisiere-zustand) und [Steuere Zustand](#steuere-zustand) zusammen ausführt.
Object ID und Verzögerung mit anderen Bausteinen kann aber definiert werden.



### Datenpunkt erzeugen
![Datenpunkt erzeugen](img/01system/180datenpunkterzeugen.PNG)

Zwei Arten von Variablen können in Skripten erzeugt werden:

- locale [variablen](#set-variables-value)
- globale variablen oder Zustände (states).

Global Zustände sind in allen Skripten sichtbar, Lokale hingegen nur im
aktuellen Skript.

Global Zustände können in vis und allen anderen Visualisierungsmodulen
genutzt werden und können in eine DB geloggt werden.

Dieser Block erzeugt globale Zustände und wenn dieser bereits existiert wird der
Befehl ignoriert. Daher kann dieser Block ohne Risiko zu jedem Skriptstart
verwendet werden.


Typische Anwendung dieses Blocks:

![Datenpunkt erzeugen](img/01system/181.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/181code.txt)

Man kann den neu erzeugten State bereits in dem Block selber nutzen.

Bei der ersten Ausführung dieses Blocklys wird ein Fehler ausgegeben, da der
Datenpunkt erst nach der Ausführung zu finden ist.
Bei der zweiten Ausführung wird kein Fehler mehr ausgegeben, weil der Datenpunkt
jetzt existiert.



### Wert eines Datenpunktes 1
![Wert eines Datenpunktes](img/01system/190werterzeugen.PNG)

Dieser Block dient dazu den Wert eines Datenpunktes auszulesen. Folgende Attribute
des Datenpunktes können ausgelesen werden:

- Wert
	true, false oder Wert des Datenpunktes

- Anerkannt
    Befehl = falsch oder update = wahr

- Zeitstempel
	in ms seit dem 01.01.1970 (Typ "Datumsobjekt")

- Letzte Änderung
	des Wertes in ms seit dem 01.01.1970 (Typ "Datumsobjekt")

- Qualität
	???

- Quelle
	Name der Instanz, die den letzten Wert geschrieben hat, wie z.B. "system.adapter.javascript.0"

Beispiel um die Zeit der letzten Änderung des Wertes auszugeben:

![Wert eines Datenpunktes](img/01system/191.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/191code.txt)



### Wert eines Datenpunktes 2

![Wert](img/01system/200werterzeugen.PNG)

Beschreibung fehlt noch!



### Wert eines Datenpunktes 3

![Wert](img/01system/210wert.PNG)

Beschreibung fehlt noch!



### Objekt ID

![Objekt ID auswählen](img/01system/220objekt.PNG)

Dieses ist ein einfacher Hilfsblock um komfortabel die Objekt ID zum triggern des Blocks auszuwählen.
Der ID Auswahldialog wird durch Anklicken von "Objekt ID" geöffnet.

Typische Anwendung dieses Blocks:

![Objekt ID auswählen](img/01system/221.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/221code.txt)



### Attribut

![Attribut](img/01system/230attribut.PNG)

Gibt ein Attribut des Objekts zurück. Der Pfad zum Attribut kann wie im Beispiel
verschachtelt sein.

Wenn das erste Attribut string ist, versucht die Funktion, den String als JSON-
String zu analysieren.



## Aktionen

### Exec-Kommando
![Exec - execute](img/02aktionen/210.PNG)

Dieser Block führt das eingegebene Kommando im System aus, so als ob man es in
der SSH Konsole eingegeben hätte.
Der Befehl wird mit den rechten des Users ausgeführt unter dem ioBroker gestartet
wurde.

Ohne Ausgabe eines Ergebnisses:

![Exec - execute](img/02aktionen/211.PNG)

Wenn eine Ausgabe erfolgen soll, den Haken bei `mit Ergebnissen` setzen:

![Exec - execute](img/02aktionen/212.PNG)

Dieses Beispiel zum importieren: ![code](img/02aktionen/212code.txt)


Zur Anlayse der Ausgabe werden 3 besondere Variablen erzeugt:

* _Ergebnis_
enthält die reguläre Ausgabe auf die Konsole (z.B für den Befehl "ls /opt/"
lautet die Ausgabe "iobroker nodejs")

* _Fehlerobjekt_
wenn der Befehl vom JavaScript Modul nicht ausgeführt werden konnte

* _stderr_
die Fehlerausgabe des ausgeführten Programms


Zusätzlich wird die selbe Ausgabe auch im log erscheinen, wenn der loglevel
nicht auf 'none' steht.



### request URL
![request URL](img/02aktionen/220.PNG)

Ruft eine URL auf und gibt das Ergebnis zurück.

Beispiel:

![request URL](img/02aktionen/221.PNG)

Zur Anlayse der Ausgabe werden 3 besondere Variable erzeugt:


* _Ergebnis_
enthält den body der angeforderten Seite

* _Fehler_
enthält eine Fehlerbeschreibung

* _Antwort_
(nur für Fortgeschrittene), Spezialobjekt vom Typ [http.IncomingMessage](https://nodejs.org/api/http.html#http_class_http_incomingmessage)

Wenn keine Ausgabe gewünscht ist, kann diese unterdrückt werden. Dazu die Option
"mit Ergebnis" abhaken.



## SendTo
>Die SendTo Blöcke für telegram, Sayit, pushover und email erscheinen erst nachdem
der entsprechende Adapter installiert und konfiguriert wurde.


### An telegram etwas senden
![Send to telegram](de/img/03sendto/0350.png)

Dieser Block dient dazu eine Nachricht über telegram mit Hilfe des telegram-
Adapters zu senden.

Über Dropdown kann ausgewählt werden ob die Nachricht entweder über alle
verfügbargen Instanzen oder über eine Instanz (üblicherweise telegram.0) gesendet
werden soll.

Das Feld `Meldung`beinhaltet den zu sendenen Text und ist zwingen Notwendig.

> Texte können auch aus Textblöcken erstellt werden

Empfänger Angabe  ist optional. Dies ist die ID von [telegram](https://core.telegram.org/bots/api#user) (Eindeutige Kennung für
user oder bot).

Wenn der Loglevel ungleich `keins` ist, wird dieselbe Nachricht auch im Log Fenster
ausgegeben.



### Über SayIt Text aussprechen
![Send to SayIt](de/img/03sendto/0340.png)

Dieser Block wird verwendet, um Text an eine SayIt-Instanz zu senden, um diesen
Text auszusprechen.

Über Dropdown kann ausgewählt werden ob die Nachricht entweder über alle
verfügbargen Instanzen oder über eine Instanz (üblicherweise sayit.0) gesendet
werden soll.

Das Feld `Meldung`beinhaltet den zu sendenen Text und ist zwingen Notwendig.

Die Spracheinstellungen der text2speech egine müssen geprüft werden.

Die Angabe der Lautstärke in Werten von 0 bis 100 ist optional.

Wenn der Loglevel ungleich `keins` ist, wird dieselbe Nachricht auch im Log Fenster
ausgegeben.



### An pushover etwas senden

![Send to pushover](de/img/03sendto/0330.png)

This block is used to send text to pushover client. You can read about pushover driver [here](https://github.com/ioBroker/ioBroker.pushover).



To send message to some specific instance, you should select the installed adapter instance (Normally pushover.0), elsewise message will be sent to all existing instances.

Property *message* is mandatory and exactly this text will be sent to client.

All other properties are optional and you can read bout them [here](https://pushover.net/api):

- *device ID* - your user's device name to send the message directly to that device, rather than all of the user's devices (multiple devices may be separated by a comma)
- *title* - your message's title, otherwise your app's name is used
- *URL* - a supplementary URL to show with your message
- *URL title* - a title for your supplementary URL, otherwise just the URL is shown
- *priority* - send as -2 to generate no notification/alert, -1 to always send as a quiet notification, 1 to display as high-priority and bypass the user's quiet hours, or 2 to also require confirmation from the user
- *time in ms* - a Unix timestamp of your message's date and time to display to the user, rather than the time your message is received by our API
- *sound* - the name of one of the sounds supported by device clients to override the user's default sound choice

Wenn der Loglevel ungleich `keins` ist, wird dieselbe Nachricht auch im Log Fenster
ausgegeben.



### Send email
![Send to email](de/img/03sendto/0360.png)

This block is used to send text as email.

Of course the email adapter must be installed, configured and tested.

To send message to some specific instance, you should select the installed adapter instance (Normally email.0), elsewise message will be sent to all existing instances.

Property *text* is mandatory and exactly this text will be sent to client.

Of course the destination (*to*) must be filled with valid email address.

You can attach up to files (normally images) to email. To use images in the text, you must change format to HTML (check "Send as HTML" option) and text could look like:

```html
<p>Embedded image 1: <img src='cid:file1'/></p>
<p>Embedded image 2: <img src='cid:file2'/></p>
```

You can refer to files as ```<img src='cid:file1'/>```. "file1" and "file2" are reserved IDs and cannot be changed.

"file name" must consist full path to image on disk.

[Send to email](de/img/03sendto/_email_1_en.png)

Additionally if the log level is not "none", the same message will be sent to log.



### Custom sendTo block
[Custom sendTo block](de/img/03sendto/_custom_en.png)

This is just a help block to send internal system message (sendTo) to any adapter. 

Of course you can use custom function block to do anything crazy, and to send messages too.

You can define your own parameters for sendTo command:

[Custom sendTo block](de/img/03sendto/_custom_1_en.png)

Read more [here](https://github.com/ioBroker/ioBroker.javascript#sendto) about "sendTo".

Example how to send SQL query to sql adapter:

[Custom sendTo block](de/img/03sendto/_custom_2_en.png)


If you will use only one parameter with empty name, so no structure will created, like here:

```javascript
var obj, result;

/**
 * Describe this function...
 */
function JSON_stringify(obj) {
    return JSON.stringify(obj);
}


// Send query to SQL adapter
sendTo("sql.0", "query", 'SELECT * FROM datapoints', function (result) {
    console.log((JSON_stringify(result)));
  });
console.log("sql.0: " + "");
```

Or how to request history from SQL adapter:

[Custom sendTo block](de/img/03sendto/_custom_3_en.png)



Generated JavaScript code:
```javascript
var obj, end, result;

/**
 * JSON.stringify object
 */
function JSON_stringify(obj) {
    return JSON.stringify(obj);
}


// Get history from SQL adapter
end = (new Date().getTime());
sendTo("sql.0", "getHistory", {
   "id": 'system.adapter.admin.0.memRss',
   "options": {start: end - 3600000, end: end, aggregate: "minmax"}
}, function (result) {
    console.log((JSON_stringify(result)));
  });
```

If you will start value with "{" it will be interpreted as JSON string. Use double quotes in string.


### Etwas an IFTTT senden


## Datum und Zeit

### Zeiten vergleichen
![Zeitvergleich](de/img/04datumundzeit/0410.PNG)

Falls über Dropdown `zwischen` oder `nicht zwischen` ausgewählt wird, ändert sich der
Block folgendermaßen:

![Zeitvergleich](de/img/04datumundzeit/0411.png)

Folgende Vergleiche möglich:

- aktuelle Zeit ist kleiner als eingegebene Zeit
- aktuelle Zeit ist gleich oder kleiner als eingegebene Zeit
- aktuelle Zeit ist größer als eingegebene Zeit
- aktuelle Zeit ist gleich oder größer als eingegebene Zeit
- aktuelle Zeit ist gleich mit eingegebener Zeit
- aktuelle Zeit ist zwischen eingegebenen Zeiten
Es wird geprüft ob die aktuelle Zeit größer oder gleich als die erst genannte Zeit
(Startzeit) ist _und_ kleiner als die zweit genannte Zeit (Endzeit) ist.

- aktuelle Zeit ist nicht zwischen eingegebenen Zeiten
Es wird geprüft ob die aktuelle Zeit kleiner als die erst genannt Zeit (Startzeit) ist
  _und_ größer oder gleich als die zweit genannte Zeit (Endzeit) ist.

Durch abwählen des Hakens ist es möglich auch andere Zeitformate mit Datumsobjekten
zu vergleichen:

![Zeitvergleich](de/img/04datumundzeit/0412.png)

Folgende Zeitformate sind gültig:

- JJJJ-MM-TT SS:MM:ss
- JJJJ-MM-TT SS:MM
- SS:MM:ss
- SS:MM


### Vergleich mit aktueller Uhrzeit
![Vergleich mit aktueller Uhrzeit](de/img/04datumundzeit/0420.png)

Auch dieser Block wird verwendet, um die Tageszeit mit der aktuellen Zeit zu vergleichen.
Die Logik entspricht [Zeiten vergleichen](#time-comparision), es können aber keine Datumsobjekte eingefügt
werden und der Vergleich ist immer mit der aktuellen Zeit.


### Aktuelle Uhrzeit in einem bestimmten Format abrufen
![Aktuelle Uhrzeit in einem bestimmten Format abrufen](de/img/04datumundzeit/0430.png)

Folgende Formate sind möglich auszugeben:

- Datum-Objekt - Epoch Zeit in Millisekunden bezogen auf GMT
(1970.1.1 00:00:00.000Z GMT).
- Millisekunden - der aktuellen Sekunde von 0 bis 999,
- Sekunden - der aktuellen Minute von 0 bis 59,
- Sekunden seit Tagesanfang - Anzahl der Sekunden seit Tagesbeginn (0 bis 24 * 3600 - 1),
- Minuten - der aktuellen Stunde von 0 bis 59 aus,
- Minuten seit Tagesanfang - Anzahl der Minuten seit Tagesbeginn (0 bis 24 * 60 - 1),
- Stunden - des aktuellen Tages von 0 bis 23,
- Monatsdatum - Tag des Monats von 1 bis 31,
- Monat als Nummer - aktueller Monat als Zahl von 1 bis 12 ,
- Monat als Text - aktueller Monat als Text mit Sprachauswahl.
- Monat als Kurztext - aktuellen Monat als Kurztext mit Sprachauswahl:
Jan, Feb,  Mar,  Apr, Mai, Juni, Juli, Aug, Sept, Okt, Nov, Dez.
- Jahr, kurz - aktuelles Jahr von 0 bis 99, z.B.: 2018 ergibt 18.
- Jahr, voll - aktuelles Jahr
- Wochentag als Text - der aktuelle Wochentag in Textform mit Sprachauswahl.
- Wochentag als Kurztext - der aktuelle Wochentag in Kurzform mit Sprachauswahl:
So, Mo, Di, Mi, Do, Fr, Sa.
- Wochentag als Nummer - der aktuelle Wochentag von 1 (Montag) bis 7 (Sonntag).
- anwenderformatiert - Eigene Formate verwenden
- JJJJ.MM.TT - 2016.09.14
- JJJJ/MM/TT - 2016/09/14
- JJ.MM.TT - 16.09.14
- JJ/MM/TT - 16/09/14
- TT.MM.JJJJ - 14.09.2016
- TT/MM/JJJJ - 14/09/2016
- TT.MM.JJ - 14.09.16
- TT/MM/JJ - 14/09/16
- MM/TT/JJJJ - 09/14/2016
- MM/TT/JJ - 09/14/16
- TT.MM. - 14.09.
- TT/MM - 14/09
- MM.TT - 09.14
- MM/TT - 09/14
- SS:mm - 12:00
- SS:mm:ss - 12:00:00
- SS:mm:ss.sss - 12:00:00.000


### Die Zeit für aktuelle Astro-Events abrufen
![Die Zeit für aktuelle Astro-Events abrufen](de/img/04datumundzeit/0440.png)

Das Offset Attribut kann auch negativ eingegeben werden um Zeiten vor dem Astro-
Event zu bestimmen.

Folgende Werte können als Attribut in der Astrofunktion verwendet werden:

- Sonnenaufgang: Der obere Rand der Sonne erscheint am Horizont
- Sonnenaufgang-Ende: Der untere Rand der Sonne berührt den Horizont
- "Golden Hour" Ende: ende weiches licht (beste zeit für Fotografie)
- Sonnenmittag: Sonne ist in der höchsten Position
- "Golden Hour": Die goldene Stunde beginnt
- Sonnenuntergang-Anfang: Der untere Rand der Sonne berührt den Horizont
- Sonnenuntergang: Die Sonne verschwindet unter dem Horizont, abends beginnt
die zivile Dämmerung
- Abenddämmerung: Abends beginnt die nautische Dämmerung
- Nautische Abenddämmerung: Abends beginnt die astronomische Dämmerung
- Nacht: dunkel genug für astronomische Beobachtungen
- Nachtsende: Morgen beginnt die astronomische Dämmerung
- Nautische Morgendämmerung: Morgen Nautische Dämmerung beginnt
- Morgendämmerung: Die morgendliche Nautische Dämmerung endet, die morgendliche
zivile Dämmerung beginnt
- Nadir: dunkelster Moment der Nacht, Sonne ist in der tiefsten Position

Der Rückgabewert hat den Typ "Datum-Objekt", also die Anzahl der Millisekunden seit
01.01.1970.

>**Hinweis:** in den Einstellungen der JavaScript-Adapter Instanz muss die Astro-
Einstellung definiert sein.


## Konvertierung
Um einen Datentyp in einen anderen umzuwandeln, stehen folgende Konvertierungsblöcke
zur Verfügung:

### In Zahl umwandeln
![In Zahl umwandeln](de/img/05konvertierung/0510.png)

Wandelt einen Wert in eine Fließkommazahl mit Dezimalpunkt um.

### In Logikwert umwandeln
![In Logikwert umwandeln](de/img/05konvertierung/0520.png)

Wandelt einen Wert in booleschen Wert (true oder false) um.

### In String umwandeln
![In String umwandeln](de/img/05konvertierung/0530.png)

Wandelt einen Wert in einen String/Zeichenkette um.

### Variablentyp abrufen
![Variablentyp abrufen](de/img/05konvertierung/0540.png)

Variablentyp kann boolean, number, string oder object sein.

### In Datum/Zeit Objekt umwandeln
![In Datum/Zeit Objekt umwandeln](de/img/05konvertierung/0550.png)

Wandelt einen Wert in ein Datum-Objekt um. [Hier](#get-actual-time-im-specific-format) sind die Datum Objekte beschrieben.

### Datum/Zeit in String umwandeln
![Datum/Zeit in String umwandeln](de/img/05konvertierung/0560.png)

Die Format Optionen sind wie [hier](#get-actual-time-im-specific-format) beschrieben.

### JSON in Objekt umwandeln
![JSON in Objekt umwandeln](de/img/05konvertierung/0570.png)

Wandelt JSON String in JavaScript Objekt. Bei Fehler wird das leere Objekt zurückgegeben.
(Nur für Experten)

### Objekt in JSON umwandeln
![Objekt in JSON umwandeln](de/img/05konvertierung/0580.png)

Wandelt JavaScript Objekt in JSON String.
Bei aktivierter Option formatieren sieht der String so aus:

```json
{
  "a": 1,
  "b": 2
}
```

Bei nicht aktivierter Option formatieren so:

```
{"a": 1, "b": 2}
```


## Trigger

Trigger (Auslöser) werden prinzipiell benötigt um Aufgaben wiederholt durchzuführen.
Gewünschte Aufgaben müssen innerhalb der offenen Klammer platziert werden.

> Trigger in einem Triggerbaustein sind nicht möglich!
> ![Trigger in Trigger](de/img/06trigger/0611.PNG)


### Auslöser auf mehrere Status Änderungen
![Trigger on states change](de/img/06trigger/0610.png)

Wenn sich der Status eins oder mehrerer Objekte ändert oder aktualisiert wird Dieser Block führt eine Aktion aus, hat. Dies ist der Hauptblock zum Aufbau von Interaktionen zwischen
verschiedenen Zuständen und entsprechenden Systemen.

Über das Zahnrad können beliebig viele Objekt ID's per Drag and Drop
hinzugefügt werden:

![Trigger on states change](de/img/06trigger/0613.png)

Es kann gewählt werden ob das abgefragte Objekt
wurde geändert
wurde aktualisiert
ist größer als letztes
ist gleich dier größer als letztes
ist kleiner als letztes
ist gleich ider kleiner als letztes
ist wahr
ist unwahr


Das ist das Ack-Flag (bestätigt) des Zustandes (state) eines Datenpunktes, welches anzeigt, ob ein Befehl (ack == false) an den Adapter (z.B. von Vis) durch die Gegenseite bestätigt wurde (Update: ack == true). Bei "egal" wird Ack nicht ausgewertet.

Befehl heißt, dass der Zustand innerhalb ioBroker geändert wurde, aber noch nicht zwangsläufig den aktuellen/wahren Zustand des Geräts darstellt. Der jeweilige Adapter steuert daraufhin das jeweilige Gerät.

Update heißt, dass das Gerät oder der Ziel-Adapter die Änderung bestätigt, d.h. du kannst davon ausgehen, dass es sich um den tatsächlichen und aktuellen Zustand des Geräts handelt.

Typisches Beispiel:

![Trigger on states change](de/img/06trigger/0611.png)

Dieses Beispiel zum importieren: ![code](de/img/01system/0612code.txt)


### Auslöser auf eine Status Änderung
![Trigger on state change](de/img/06trigger/0620.png)

Dies ist derselbe Block wie der zuvor genannte Auslöser auf mehrere Status
Änderungen, jedoch ohne die Möglichkeit, mehrere Objekt-IDs zum Triggern zu
verwenden.


### Trigger info
![Trigger info](de/img/06trigger/0630.png)

Abrufen von Informationen des Status der den Trigger ausgelöst hat.

>Trigger Info kann nur innerhalb der Blöcke ["Auslöser auf mehrere Status Änderungen"](#auslöser-auf-mehrere-status- änderungen)
oder ["Auslöser auf eine Status Änderung"](#auslöser-auf-eine-status-änderung) verwendet werden.

Folgende Informationen können abgerufen werden:

- Objekt ID
ID des States, der den Trigger ausgelöst hat

- Name
Name des Status aus common.name

- Beschreibung
Beschreibung des Status aus common.desc

- Kanal ID
ID des Kanals, zu dem der Status gehört. Wenn dort kein Kanal vorhanden ist, ist er null

- Kanalname
Name des Kanals, zu dem der Status gehört. Wenn dort kein Kanal vorhanden ist, ist er null

- Geräte ID
ID des Geräts, zu dem der Status gehört. Wenn dort kein Kanal vorhanden ist, ist er null

- Gerätename
Name des Geräts, zu dem der Status gehört. Wenn dort kein Kanal vorhanden ist, ist er null

- Wert
Aktueller Wert des Status

- Zeitstempel
aktueller Zeitstempel als Datumsobjekt

- Qualität
aktueller Qualitätscode des Status

- Ursprung
Name der Instanz, die die Änderung verursacht

- Befehl oder Aktualisierung
Ist es ein Befehl(ack=false) oder Update (ack=true)

- letzte Änderung
Zeitstempel der letzten Änderung dieses Wertes

- vorheriger Wert
vorheriger Wert des Status

- vorheriger Zeitstempel
Vorheriger Zeitstempel dieses Status, bevor der Trigger ausgelöst wurde

- vorherige Qualität
vorherige Qualität dieses Zustands, bevor der Trigger ausgelöst wurde

- vorherige Ursprung
Vorheriger Ursprung dieses Zustands, bevor der Auslöser ausgelöst wurde

- vorherige Bestätigung
vorheriger Typ dieses Wertes, bevor der Trigger ausgelöst wurde

- vorherige letzte Änderung
Vorheriger "zuletzt geänderter Wert" dieses Status, bevor der Trigger ausgelöst wurde


Typisches Beispiel:

![Trigger on states change](de/img/06trigger/0614.png)

Dieses Beispiel zum importieren: ![code](de/img/01system/0614code.txt)



### Schedule
![Schedule](de/img/06trigger/0640.png)

This is second main block for automation after ["Trigger on states change"](#trigger-on-states-change). This block lets execute some actions periodically.

The definition of schedule rule will be done in very well documented CRON [format](https://en.wikipedia.org/wiki/Cron). With extension, that seconds can be defined too.
If seconds should be used they must be defined as very first parameter of CRON rule and rule will have 6 parts.

Generally CRON rule consist of 5 or 6 parts:
- seconds rules (optional)
- minutes rules
- hours rules
- day of month rules
- month's rules
- and day of week rules.

For every part following formats are allowed:
- \* - fire every (second, minute, hour, ...)
- X (e.g. 5) - fire only in this second, minute, hour...
- from-to (e.g 1-9) - fire only in this interval
- \*/X (e.g. \*/5) - fire every X seconds, minutes... In case of "\*/5" for hours the trigger will fire on 0, 5, 10, 15 and on 20 hours.
- numbers and intervals can be combined by comma (e.g 1,3,4-6). Do not make spaces between numbers, because space is delimiter for rule's parts.

\*/10 \* \* \* 6,7 - fire every 10 minutes on saturday and sunday.

\*/30 \* \* \* \* \* - fire every 30 seconds.

```
 ┌───────────── min (0 - 59)
 │ ┌────────────── hour (0 - 23)
 │ │ ┌─────────────── day of month (1 - 31)
 │ │ │ ┌──────────────── month (1 - 12)
 │ │ │ │ ┌───────────────── day of week (0 - 6) (0 to 6 are Sunday to Saturday; 7 is also Sunday)
 │ │ │ │ │
 │ │ │ │ │
 │ │ │ │ │
 * * * * *  schedule
```

or if seconds used:

```
 ┌───────────── seconds (0 - 59)
 │ ┌───────────── min (0 - 59)
 │ │ ┌────────────── hour (0 - 23)
 │ │ │ ┌─────────────── day of month (1 - 31)
 │ │ │ │ ┌──────────────── month (1 - 12)
 │ │ │ │ │ ┌───────────────── day of week (0 - 6) (0 to 6 are Sunday to Saturday; 7 is also Sunday)
 │ │ │ │ │ │
 │ │ │ │ │ │
 │ │ │ │ │ │
 * * * * * *  schedule
```

But there is a good help for you to build such a rules. By clicking on rule the CRON dialog will be opened and you can specify by mouse your rule.

[Schedule](de/img/06trigger/trigger_schedule_1_en.png)




### Trigger on astro event
![Schedule](de/img/06trigger/0650.png)

Execute some action on astrological event. Following events are possible:

- sunrise: sunrise (top edge of the sun appears on the horizon)
- sunriseEnd: sunrise ends (bottom edge of the sun touches the horizon)
- goldenHourEnd: morning golden hour (soft light, best time for photography) ends
- solarNoon: solar noon (sun is in the highest position)
- goldenHour: evening golden hour starts
- sunsetStart: sunset starts (bottom edge of the sun touches the horizon)
- sunset: sunset (sun disappears below the horizon, evening civil twilight starts)
- dusk: dusk (evening nautical twilight starts)
- nauticalDusk: nautical dusk (evening astronomical twilight starts)
- night: night starts (dark enough for astronomical observations)
- nightEnd: night ends (morning astronomical twilight starts)
- nauticalDawn: nautical dawn (morning nautical twilight starts)
- dawn: dawn (morning nautical twilight ends, morning civil twilight starts)
- nadir: nadir (darkest moment of the night, sun is in the lowest position)

**Note:** to use "astro"-function the "latitude" and "longitude" must be defined in JavaScript adapter settings.

Additionally you can set the offset in minutes to astrological event, e.g. to fire the trigger 1 hour before down: 

[Schedule](de/img/06trigger/trigger_astro_1_en.png)

As you can see the offset can be negative too to specify time before astrological events.




### Named schedule
![Schedule](de/img/06trigger/0660.png)

This block is the same as [Schedule](#schedule), but with possibility to set CRON rule by string and with possibility to stop the schedule.

You can specify unique name of this schedule block and then later to clear it with [Clear schedule](#clear-schedule). 

Here is an example of configurable alarm clock:
 
[Schedule](de/img/06trigger/trigger_schedule_ex_1_en.png)

```xml 

```




### Clear schedule
![Schedule](de/img/06trigger/0670.png)

With this function block you can clear named schedule. If you define named one more time without clearing it, the old one will still active.

See an example in [Named schedule](#named-schedule)




### CRON dialog
![Schedule](de/img/06trigger/0680.png)

Create CRON rule from dialog. This block can be connected with [Named schedule](#named-schedule).

[Schedule](de/img/06trigger/trigger_cron_input_1_en.png)

```xml 
<xml xmlns="http://www.w3.org/1999/xhtml">
  <block type="comment" id="]aB;GhQJvYrr~:H4Ft9l" x="63" y="38">
    <field name="COMMENT">Every 0th minute every hour</field>
    <next>
      <block type="schedule_create" id="?}upFtiA@CE_Gd)SmDo|">
        <field name="NAME">schedule</field>
        <value name="SCHEDULE">
          <shadow type="field_cron" id="1Ag|noK^~u]GFEW/(lb)">
            <field name="CRON">* * * * *</field>
          </shadow>
          <block type="field_cron" id="phjg#B~@BJTO9i[HmZ4O">
            <field name="CRON">0 * * * *</field>
          </block>
        </value>
        <statement name="STATEMENT">
          <block type="debug" id="Lv[a}BtvBDO-2Lt,s+z4">
            <field name="Severity">log</field>
            <value name="TEXT">
              <shadow type="text" id="evxnn0R1(AC^Y_U`oT_a">
                <field name="TEXT">It is exactly</field>
              </shadow>
              <block type="text_join" id="62uB_db8.g}63I{^e}#">
                <mutation items="3"></mutation>
                <value name="ADD0">
                  <block type="text" id="HH((bCdxr?A5)8Svuo6(">
                    <field name="TEXT">It is exactly </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="time_get" id="7{BBfF0jmKD[qX,y6voK">
                    <mutation format="false" language="false"></mutation>
                    <field name="OPTION">h</field>
                  </block>
                </value>
                <value name="ADD2">
                  <block type="text" id="edML0zJ2V9kN}5/DLdS5">
                    <field name="TEXT"> o'clock</field>
                  </block>
                </value>
              </block>
            </value>
          </block>
        </statement>
      </block>
    </next>
  </block>
</xml>
```




### CRON rule
![Schedule](de/img/06trigger/0690.png)

Combine CRON rule from different parts.

You can display rule as block or as line:

[Schedule](de/img/06trigger/trigger_cron_rule_1_en.png)

With additional parameter "with seconds" you can specify seconds for CRON rule too

[Schedule](de/img/06trigger/trigger_cron_rule_2_en.png)

This block can be used (like [CRON dialog](#cron-dialog)) only with [Named schedule](#named-schedule) block.







## Timeouts

### Ausführung verzögern

![Ausführung verzögern](de/img/07timeouts/0710.png)

Mit diesem Block können andere Blöcke Zeit verzögert ausgeführt werden. Die
Zeit ist wählbar in Millisekunden, Sekunden oder Minuten.
Entspricht der JavaScript Funktion `setTimeout`.

Der Name der Verzögerung kann frei gewählt werden.

Es gibt in Blockly keine Pause Funktion, kann aber mit diesem Block simuliert
werden.

Beispiel:

![Ausführung verzögern](de/img/07timeouts/0711.png)


```xml
<xml xmlns="http://www.w3.org/1999/xhtml">
  <block type="debug" id=":6GZE*FHy@vPKKl{`hV" x="487" y="163">
    <field name="Severity">log</field>
    <value name="TEXT">
      <shadow type="text" id="LV-dx[I(8bAu(_kcG.U">
        <field name="TEXT">Make a pause 5 seconds</field>
      </shadow>
    </value>
    <next>
      <block type="timeouts_settimeout" id="~?BW3eBK_t:TzNk}x9l3">
        <field name="NAME">timeout</field>
        <field name="DELAY">5000</field>
        <statement name="STATEMENT">
          <block type="debug" id="glbs:mQxsDfEieLaru0">
            <field name="Severity">log</field>
            <value name="TEXT">
              <shadow type="text" id="_7T9e{FEJTWcpLl*BltU">
                <field name="TEXT">After pause</field>
              </shadow>
            </value>
          </block>
        </statement>
      </block>
    </next>
  </block>
</xml>
```




### Ausführungsverzögerung anhalten
![Ausführungsverzögerung anhalten](de/img/07timeouts/0720.png)

Dieser Block beendet die benannte Verzögerung.

Beispiel:
Simulation eines Bewegungserkennungsszenarios, wo bei der ersten Bewegung
das Licht angehen und nach der letzten Bewegung und nach 30 Sekunden das
Licht ausgehen soll.

![Ausführungsverzögerung anhalten](de/img/07timeouts/0721.png)

```xml
<xml xmlns="http://www.w3.org/1999/xhtml">
  <block type="on_ext" id="+nZ`H6mh/;g(e3u,t;wJ" x="163" y="12">
    <mutation items="1"></mutation>
    <field name="CONDITION">ne</field>
    <field name="ACK_CONDITION"></field>
    <value name="OID0">
      <shadow type="field_oid" id="{mRcPH:k^_5q-hwg1q%">
        <field name="oid">node-red.0.javascript.0.Motion</field>
      </shadow>
    </value>
    <statement name="STATEMENT">
      <block type="controls_if" id="]lX4.m?HnwXigM.6wY/D">
        <value name="IF0">
          <block type="logic_compare" id="s0DHFun9e*,c3AawmP_~">
            <field name="OP">EQ</field>
            <value name="A">
              <block type="variables_get" id="g}IH`Bx0T(mkht8~{Ul0">
                <field name="VAR">value</field>
              </block>
            </value>
            <value name="B">
              <block type="logic_boolean" id="Meek9{gS-NOR?|(fgbVg">
                <field name="BOOL">TRUE</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="debug" id=":6GZE*FHy@vPKKl{`hV">
            <field name="Severity">log</field>
            <value name="TEXT">
              <shadow type="text" id="LV-dx[I(8bAu(_kcG.U">
                <field name="TEXT">Motion detected</field>
              </shadow>
            </value>
            <next>
              <block type="comment" id="6_T-s#wApgZhu0+4uEk}">
                <field name="COMMENT">Switch light ON</field>
                <next>
                  <block type="control" id="fxgT@s0r?[`LJIsqR~M_">
                    <mutation delay_input="false"></mutation>
                    <field name="OID">javascript.0.Light</field>
                    <field name="WITH_DELAY">FALSE</field>
                    <value name="VALUE">
                      <block type="logic_boolean" id="0mgo#`N%Zm{MTELxw%~0">
                        <field name="BOOL">TRUE</field>
                      </block>
                    </value>
                    <next>
                      <block type="comment" id="rZ^o06`}^uFftKj2oYvE">
                        <field name="COMMENT">Stop timer, even if it not running</field>
                        <next>
                          <block type="timeouts_cleartimeout" id="#H#~HxipC8_-/{%,2R1P">
                            <field name="NAME">lightOff</field>
                            <next>
                              <block type="timeouts_settimeout" id="~?BW3eBK_t:TzNk}x9l3">
                                <field name="NAME">lightOff</field>
                                <field name="DELAY">5000</field>
                                <statement name="STATEMENT">
                                  <block type="debug" id="glbs:mQxsDfEieLaru0">
                                    <field name="Severity">log</field>
                                    <value name="TEXT">
                                      <shadow type="text" id="_7T9e{FEJTWcpLl*BltU">
                                        <field name="TEXT">Light OFF</field>
                                      </shadow>
                                    </value>
                                    <next>
                                      <block type="control" id="McdOD=k4)MlO42RVgB~r">
                                        <mutation delay_input="false"></mutation>
                                        <field name="OID">javascript.0.Light</field>
                                        <field name="WITH_DELAY">FALSE</field>
                                        <value name="VALUE">
                                          <block type="logic_boolean" id="XLHrXB)/|dqGlh,nXl^[">
                                            <field name="BOOL">FALSE</field>
                                          </block>
                                        </value>
                                      </block>
                                    </next>
                                  </block>
                                </statement>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </statement>
      </block>
    </statement>
  </block>
</xml>
```




### Zyklische Ausführung
![Zyklische Ausführung](de/img/07timeouts/0730.png)

Dieser Block wiederholt Aktionen regelmäßig. Das kann zwar auch mit dem   
CRON Block erfolgen, der kürzest mögliche Intervall ist dort aber 1 Sekunde.   
Hier können wiederholte Aktionen in Millisekunden ausgeführt werden. 

If you set the interval too small (under 100ms) it can be, that intervals will be bigger.

Similar to timeout block you can set unique interval name too.

An aTTitional feature is to set the interval by using a variable, just replace the "ms" with an predefined variable:

![Zyklische Ausführung](de/img/07timeouts/Timer_variable_en.PN)


### Stop execution by interval
![Stop execution by interval](de/img/07timeouts/0740.png)

With the help of this block you can cancel periodically execution of interval block by its name.







## Logik

### If else block

Um den "falls ... sonst falls ..." Block zu erstellen klickt man auf das Zahnrad und fügt die zusätzlich benötigten Elemente dem "falls" Block hinzu.

![Getting started 3](de/img/08logik/0810.PNG)

### Comparision block

### Logical AND/OR block

### Negation block

### Logical value TRUE/FALSE

### null block

### Test block







## Schleifen



### Repeat N times

![Schleifen](de/img/09schleifen/091.PNG)

### Repeat while

![Schleifen](de/img/09schleifen/092.PNG)

### Count

![Schleifen](de/img/09schleifen/093.PNG)

### For each

![Schleifen](de/img/09schleifen/094.PNG)

### Break out of loop

![Schleifen](de/img/09schleifen/095.PNG)






## Mathematik

### Number value

![Mathe](de/img/10mathematik/1010.PNG)

### Arithmetical operations +-*/^

### Square root, Abs, -, ln, log10, e^, 10^

### sin, cos, tan, asin, acos, atan

### Math constants: pi, e, phi, sqrt(2), sqrt(1/2), infinity

### Is even, odd, prime, whole, positive, negative, divisibly by

### Modify variably by value (plus or minus)

### Round, floor, ceil value

### Operations on the list of values: sum, min, max, average, median, modes, deviation, random item

### Modulus

### Limit some value by min and max

### Random value from 0 to 1

### Random value between min and max



## Text

### String value

![Text](de/img/11text/1110.PNG)

### Concatenate strings

### Append string to variable

### Length of string

### Is string empty

### Find position in string

### Get symbol in string on specific position

### Get substring

### Convert to upper case or to lower case

### Trim string



## Listen

### Create empty list

![Listen](de/img/12listen/1210.PNG)

### Create list with values

### Create list with same value N times

### Get length of list

### Is list empty

### Find position of item in list

### Get item in list

### Set item in list

### Get sublist of list

### Convert text to list and vice versa




## Farbe

### Erzeugt eine Farbe aus der Farbpalette
![Farbe](de/img/13farbe/1310.png)

### Erzeugt eine zufällige Farbe
![Farbe](de/img/13farbe/1320.png)

### Erzeugt eine Farbe mit selbst gewählten RGB Werten zwischen 0 und 100
![Farbe](de/img/13farbe/1330.png)

### Mischt 2 Farben mit einstellbarem Farbverhältnis zwischen 0.0 und 1.0
![Farbe](de/img/13farbe/1340.png)






## Variablen

Bei Verwendung von Variablen, sollten grundlegende Programmierregeln wie
Variablen zu nutzen sind, vorhanden sein.

### Wert einer variablen setzen
![Wert einer variablen setzen](de/img/14variablen/1410.png)

Mit diesem Block kann eine globale (in jedem Skript sichtbare) Variable
geschrieben werden und diese zum Speichern von Werten verwenden. Wenn
die Variable nicht existiert, wird sie automatisch deklariert.

Es kann eine neue Variable erstellt werden oder eine vorhandene verwendet
werden.

![Wert einer variablen setzen](de/img/14variablen/1411.png)

Dieser Block:

![Wert einer variablen setzen](de/img/14variablen/1412.png)

```xml
<block xmlns="http://www.w3.org/1999/xhtml" type="variables_set" id="ch{H@omhfzI(QA{syxAG" x="212.99999999999977" y="37.99999999999994">
  <field name="VAR">item</field>
  <value name="VALUE">
    <block type="math_number" id="SbmD7,uR:hMW(P%IZRc">
      <field name="NUM">0</field>
    </block>
  </value>
</block>
```

macht dies:
```javascript
var item;
item = 0;
```




### Wert einer variablen zurück geben
![Wert einer variablen zurück geben](de/img/14variablen/1420.png)

Es können Variablen erstellt oder umbenannt werden.

![Wert einer variablen zurück geben](de/img/14variablen/1421.png)

There is one exception with trigger blocks [Trigger on states change](#trigger-on-states-change) and [Trigger on state change](#trigger-on-state-change).
Inside these blocks variable "value" yet exist, but anyway to read their values you must rename variable into value and then use it.

[Get variable's value](de/img/14variablen/variables_get_2_en.png)




## Funktionen

Mit diesen Blöcken können sich wiederholende Sequenzen als Funktion erstellt
werden und dann überall im aktuellen Skript verwendet werden.


### Funktion ohne Rückgabewert erstellen

![Funktion ohne Rückgabewert](de/img/15funktionen/1510.PNG)

Beispiel: _Schreibe die aktuelle Zeit ins Log:_

![Funktion ohne Rückgabewert Beispiel](de/img/15funktionen/1512.PNG)

```
1512code.txt
```

Nachdem die Funktion erzeugt wurde, kann sie z.B: so weiter verwendet werden:

![Funktion ohne Rückgabewert Beispiel1](de/img/15funktionen/1513.PNG)

```
1513code.txt
```

Die neue Funktion erscheint in der Block-Sidebar:

![Funktion ohne Rückgabewert Sidebar](de/img/15funktionen/1514.PNg)

Zusätzlich kann über das Zahnrad Argumente hinzugefügt und bearbeitet werden:

![Funktion ohne Rückgabewert Zahnrad](de/img/15funktionen/1515.PNg)

Beispiel: _Gebe die Summe des ersten und des zweiten Arguments aus_:

![Funktion ohne Rückgabewert Argument](de/img/15funktionen/1516.PNg)

```
1516code.txt
```
Die angelegen Variablen sind dann unter Variablen zu finden:

![Funktion ohne Rückgabewert Variable](de/img/15funktionen/1517.PNg)

Die Funktion kann z.B: so genutzt werden:

![Funktion ohne Rückgabewert VariableBSP](de/img/15funktionen/1518.PNg)

```
1518code.txt
```

### Funktion mit Rückgabewert erstellen

![Funktion mit Rückgabewert](de/img/15funktionen/1520.PNg)

Dieser Block gibt zusätzlich ein Ergebnis einer Funktion aus, um es in anderen
Blöcken zu verwenden.

![Funktion mit RückgabewertBsp](de/img/15funktionen/1521.png)

```
1521code.txt
```
Spezielles Rückgabe Element aktivieren:

![Funktion mit RückgabewertBsp](de/img/15funktionen/1522.png)

Beispiel:

![Funktion mit RückgabewertBsp1](de/img/15funktionen/1523.png)

```
1523code.txt
```


### Wert in Funktion zurückgeben

![Wert in Funktion](de/img/15funktionen/1530.png)

Dies kann nur hier [Funktion mit Rückgabewert erzeugen] verwendet werden
und liefert den zurückzugebenden Wert in der Mitte der Funkion.

### Benutzerdefinierte Funktionen ohne Rückgabewert erstellen

![Eigene Funktion ohne](de/img/15funktionen/1540.png)

Manchmal sind vorhandene Blöcke ungeeignet, um ein bestiMMtes Problem zu
lösen. Mit diesem Block ist es möglich einen eigenen Block als Funktion zu
erstellen, der Parameter akzeptiert und Aktionen ausführt.

>Eine solche Funktion muss in JavaScript erstellt werden. Es können alle
Funktionen für reines Skripting verwendet werden.

Um den Code zu schreiben, auf das '...' am Block klicken und der Editor-Dialog
wird geöffnet.

![Eigene Funktion ohne1](de/img/15funktionen/1542.png)

Ansonsten ist die Nutzung dieses Blocks ähnlich wie [Funktion mit Rückgabewert
erzeugen] oder [Funktion ohne Rückgabewert erzeugen].

### Benutzerdefinierte Funktionen mit Rückgabewert erstellen

![Eigene Funktion mit](de/img/15funktionen/1550.png)

Genau wie ohne Rückgabewert sind benutzerdefinierte Funktionen auch mit 
Rückgabewert möglich. Rückgabewert im Editor-Dialog:

```return 'das Ergebnis'```

Beispiel:

![Eigene Funktion mit](de/img/15funktionen/1552.png)

```
1552code.txt
```

### Call Funktion
Für jede erstellte Funktion erscheint ein zugehöriger Block mit dem Namen der  
Funktion in der Block-Sidebar unter Funktionen und kann so einfach wieder  
verwendet werden.
Auch in den den Funktionen erstellte Variablen erscheinen in der Block-Sidebar,  
aber unter Variablen.




# Beispiele

## Beispiel 1
**Zustand eines Datenpunkts bei Änderung eines anderen Datenpunkts ändern**

![Beispiel1](de/img/16beispiele/beispiel1.1.PNG)

Dies ist das klassische Beispiel bei Änderung eines Datenpunktes etwas anderes zu schalten.

>Das Licht wird an/ausgeschaltet wenn Bewegung/keine Bewegung erkannt wird.

Zuerst den Block "Triggers=>Falls Objekt" einfügen. Die Objekt ID auswählen um den Zustand des Objekts als Trigger für dieses Skript zu benutzen.

Einen anderen Block - "System=>Steuere" hinzufügen und im Dialog den anderen Zustand der durch den Trigger geändert werden soll auswählen.

In diesen Steuerungsblock einen Block "System=>Wert von Objekt ID" einfügen und im Dialog das Objekt "Bewegung" auswählen, um dessen Zustand in "Licht": zu schreiben.

Dieses Beispiel zum importieren: ![code](de/img/16beispiele/beispiel1code.txt)

**Es gibt bei den Trigger Blöcken eine spezielle Variable "Wert". Diese wird immer hier definiert und kann für verschiedene Zwecke verwendet werden. Sie enthält den aktuellen Wert des triggernden Objekts und man kann daher einfacherer Skripte erzeugen indem man den Block "Variable=>Objekt ID" benutzt und ihn in "Wert" umbenennt.**

![Beispiel1](de/img/16beispiele/beispiel1.2.PNG)



Dieses Beispiel zum importieren: ![code](de/img/16beispiele/beispiel1code2.txt)




## Beispiel 2
**Licht bei Bewegung anschalten und ausschalten wenn 10 Minuten keine Bewegung.**

![Beispiel2](de/img/16beispiele/Beispiel2.PNG)

Wenn der Zustand "Bewegung" mit dem Wert "wahr" aktualisiert :
1. mache "Licht" an und
2. starte eine Verzögerung von 10 Minuten um "Licht" auszuschalten und lösche
alle bisherigen Verzögerungen für diesen Datenpunkt.

Der Flag "löschen falls läuft" wird durch den letzten Befehl gesetzt. Dadurch
werden alle laufenden Timer für diesen Datenpunkt beendet und der Timer startet
neu.


Dieses Beispiel zum importieren: ![code](de/img/16beispiele/beispiel2code.txt)




## Beispiel 3
**Verschicke eine eMail wenn die Außentemperatur höher als 25 Grad Celsius ist.**

![Getting started 3](de/img/16beispiele/beispiel3.PNG)

Erklärung:

Zuerst müssen wir eine Variable definieren um zu speichern, dass die eMail für den aktuellen Temperaturalarm bereits gesendet wurde und diese Variable auf "falsch" setzen.
Dann beobachten wir die Veränderungen der Temperatur. Wir könnten dieses Skript auch periodisch ausführen, aber das ist nicht so effektiv.

Wenn sich die Temperatur ändert vergleichen wir den aktuellen Wert mit 25 und prüfen ob die eMail bereits verschickt wurde oder nicht.
Wenn die eMail noch nicht versendet war, speichern wir dass wir sie jetzt senden und senden sie auch. Natürlich muss der eMail-Adapter vorher installiert und konfiguriert worden sein.

Wenn die Temperatur unter 23 Grad fällt setzen wir die Variable "emailSent" zurück, damit beim nächsten Temperaturalarm wieder eine eMail gesendet wird.
Dazu wird die aktuelle Temperatur mit 23 verglichen und es werden keine eMails geschickt, solange die Temperatur um 25 Grad schwankt.


Dieses Beispiel zum importieren: ![code](de/img/16beispiele/beispiel3code.txt)


