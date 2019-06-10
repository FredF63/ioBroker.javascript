# Inhalt

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
Blockly ist ein Editor im javascript-Adapter, der es erlaubt, Skripte durch
zusammenfügen von grafisch verzahnten Blöcken zu erstellen.
Die grafische Darstellung ermöglicht auch Nutzern mit wenig Kenntnis einer
Programmiersprache entsprechende Skripte einfach zu erstellen.



## Editorfenster
Aufruf des Editors erfolgt im Admin Fenster Links unter Skripte.
> Falls Skripte nicht sichtbar ist und der javascript-Adapter aber installiert
ist, muss über das Dreieck oben links im Admin Fenster der Haken bei
Skripte gesetzt werden.

Beim ersten Start sind die Ordner *global* und *common* bereits angelegt.

> Der Ordner *global* ist nur für Scripte aus reinem Javascript vorgesehen.
Mit Blockly erstellte Scripte dürfen dort auf __keinen__ Fall abgespeichert
und gestartet werden.

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

![Rechtsklick](img/00einleitung/blockrechtemaustaste.png)

Baustein zusammenfalten: um eine bessere Übersicht zu erhalten können Bausteine,
zusammengefaltet werden.

![Zusammenfalten](img/16beispiele/)



## Blöcke im einzelnen
Blöcke sind in folgenden Kategorien unterteilt:
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

![{Debug output}](img/01system/110debug.PNG)

Schreibt den frei wählbaren Text, hier `test` ins log und dient zum debuggen
eines Scripts wie dies:

![Debug output](img/01system/111debug.PNG)

Dieses Beispiel zum importieren: ![code](img/01system/111code.txt)

Man kann 4 verschiedene Level für die Nachrichten definieren:

* debug - dazu muss der debug-Level der Javascript Instanz aktiviert sein.
* info - default, zumindest der info log level muss in der Javascript Instanz
	aktiviert sein.
* warning
* error - wird immer angezeigt. Die anderen Level können ignoriert werden, wenn
	es entsprechend in  der Javascript Instanz eingestellt ist.



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

Dieser Block schaltet zwischen den Werten um, non true nach false und umgekehrt.



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

Bei der ersten Ausführung dieses Blocklys wird ein Fehler ausgegeben, da der Datenpunkt erst nach der Ausführung zu finden ist.
Bei der zweiten Ausführung wird kein Fehler mehr ausgegeben, weil der Datenpunkt jetzt existiert.



### Wert eines Datenpunktes 1
![Wert eines Datenpunktes](img/01system/190werterzeugen.PNG)

Dieser Block dient dazu den Wert eines Datenpunktes auszulesen. Folgende Attribute des Datenpunktes können ausgelesen werden:
- Wert
- Acknowledge - Befehl = falsch oder update = wahr
- Timestamp in ms seit dem 01.01.1970 (Hat den Typ "Datumsobjekt")
- Letzte Änderung des Wertes in ms seit dem 01.01.1970 (Hat den Typ "Datumsobjekt")
- Qualität
- Quelle - Name der Instanz, die den letzten Wert geschrieben hat, wie z.B. "system.adapter.javascript.0"

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

Beschreibung fehlt noch!



## Aktionen

### Exec-Kommando
![Exec - execute](img/02aktionen/210.PNG)

Dieser Block führt das eingegebene Kommando im System aus, so als ob man es in
der SSH Konsole eingegeben hätte.
Der Befehl wird mit den rechten des Users ausgeführt unter dem ioBroker gestartet
wurde.

Wenn keine Ausgabe gewünscht ist, kann diese unterdrückt werden:

![Exec - execute](img/02aktionen/211.PNG)

Wenn eine Ausgabe erfolgen soll:

![Exec - execute](img/02aktionen/212.PNG)

Dieses Beispiel zum importieren: ![code](img/02aktionen/212code.txt)


Zur Anlayse der Ausgabe werden 3 besondere Variablen erzeugt:

* Ergebnis, enthält die reguläre Ausgabe auf die Konsole (z.B für den Befehl
    "ls /opt" lautet die Ausgabe "iobroker nodejs")
* Fehlerobjekt, wenn der Befehl vom JavaScript Modul nicht ausgeführt werden konnte
* stderr, die Fehlerausgabe des ausgeführten Programms

Zusätzlich wird die selbe Ausgabe auch im log erscheinen, wenn der loglevel
nicht auf 'none' steht.



### request URL
![request URL](img/02aktionen/220.PNG)

Ruft eine URL auf und gibt das Ergebnis zurück.

Beispiel:

![request URL](img/02aktionen/221.PNG)

Zur Anlayse der Ausgabe werden 3 besondere Variable erzeugt:

* Ergebnis, enthält den body der angeforderten Seite
* Fehler, enthält eine Fehlerbeschreibung
* Antwort (nur für Fortgeschrittene), Spezialobjekt vom Typ [http.IncomingMessage](https://nodejs.org/api/http.html#http_class_http_incomingmessage)

Wenn keine Ausgabe gewünscht ist, kann diese unterdrückt werden. Dazu die Option
"mit Ergebnis" abhaken.

to be continued...


