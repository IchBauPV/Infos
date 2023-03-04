Hier gibt es allgemeine Infos zu meinem Projekt für eine DIY PV Anlage mit Nulleinspeisung via IR Schnittstelle vom Einheitenzähler.  
Ihr könnt mehr über das Projekt auf [Youtube](https://www.youtube.com/@ichbaupv8402) erfahren:   
Am besten [vorne](https://www.youtube.com/watch?v=iOFwGEbs9Tw) starten.  

An dieser Stelle findet Ihr Infos wie Verdrahtungsplan, Anleitungen, Tipps, etc.  

Die Hardware kann stückweise erweitert werden. Für den ersten Test reicht der Controller + Fototransistor / IR-Lesekopf an PIN16/RX2.

## KURZANLEITUNG INSTALLATION: ##
1. Binary aus [Repositiory](https://github.com/IchBauPV/2.ESP32-PV-Controller-Binaries)  laden  
3. Mit [Flashtool](https://www.espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=13) flashen: ESP32 auswählen, Binary-Datei auwählen, 0x10000 als Adresse eingeben, Haken setzen, den richtigen COM Port einstellen - und START drücken.
4. Nach dem Start baut der ESP einen WLAN-Accesspunkt für ca. eine Minute auf. Einwählen, Heimnetz eintragen. Dann startet er neu und meldet sich im Heimnetz an.  
5. Im Router ESP eintragen als: esp32-pv-anlage  (zunächst nicht zwingend notwendig, aber da man eh nach der IP-Adresse schauen muss, ist das aber ein Abwasch)  
6. Um die IR-Verbindung zum Einheitenzähler zu prüfen, ist ein Serieller Monitor sehr nützlich (z.B Coolterm oder HTerm) 115200 Baud 8N1. Hier werden auch Debug Informationen und der komplette SML Datensatz des Zählers ausgeben sowie der ggf gefundene Gesamtverbrauch und die Wirkleistung.  
7. Browser öffnen und http://esp32-pv-anlage eintragen. Nun kann man die Webseite mit den Werte sehen (sofern welche vorhanden)
8. Das [Exceltool](https://github.com/IchBauPV/3.Zusatzsoftware) für die Visualisierung funktioniert nun ebenfalls, da es esp32-pv-anlage aufruft und die Daten abholt.  Es müssen die Makros aktiviert werden: Im Datei Explorer Datei rechts-klicken => Eigenschaften => Sicherheit => Zulassen Haken setzen, übernehmen
9. Thats all. Have fun!!!
