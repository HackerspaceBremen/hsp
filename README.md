hsp 0.1 - OpenStatus for Hackspaces with SpaceAPI

 Copyright (C) 2014 Daniel Wendt-Fröhlich
 ( daniel.w-froehlich at aetherfoton.de )
 
 This program is free software: you can redistribute it and/or modify
 it under the terms of the GNU General Public License as published by
 the Free Software Foundation, either version 3 of the License, or
 (at your option) any later version.
 
 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License
 along with this program.  If not, see <http://www.gnu.org/licenses/>.

----------------------------------------------------------------------------------------------------------------

hsp 0.1
Hackspace-Statusmelder für (beinahe) alle Hackspaces nach http://spaceapi.net/

Kann den Status des "Hackerspace Bremen e.V." ändern

Abhängigkeiten: bash curl sed

----------------------------------------------------------------------------------------------------------------

Installation:

     git clone https://github.com/hackerspacebremen/hsp/
     cd git
     chmod a+x hsp  
     sudo cp hsp /usr/bin/

----------------------------------------------------------------------------------------------------------------

Erstaufruf (Beispiel "Hackerspace Bremen e.V."):

     hsp -u https://hackerspacehb.appspot.com/v2/status -n USERNAME
Die URL und der Username werden in ~/.hsp gespeichert, damit sie nicht immer wieder eingegeben werden müssen.

Status abrufen:

     hsp

Space öffnen (mit nachträglicher Passworteingabe):

     hsp -o
oder

     hsp -o -t "THEMA"

Space schließen (mit nachträglicher Passworteingabe):

     hsp -c
oder

     hsp -c -t "THEMA"

Für weitere Möglichkeiten: 

     hsp -h

----------------------------------------------------------------------------------------------------------------

Geschrieben wurde das Script als "mobiles Unterwegs-Projekt" mit SailfishOS.
Ziel dieses Scripts ist es, einen CLI-Spacemelder in möglichst vielen Linux-Umgebungen bereit zu stellen. 
Daher wurde auf Werkzeuge zurückgegriffen, die in fast jeder Umgebung vorhanden sein sollten.
So läuft dieser Code sowohl unter Ubuntu, wie auch unter SailfishOS, Cyanogenmod und raspbian.
Die Konvertierung der Status-Ausgabe von JSON in eine Variablenliste ist ohne python, ruby, perl o.ä. eher
ungenau, erfüllt hier aber seinen Zweck und war bei 90% aller unter spaceapi.net gelisteten URLs erfolgreich. 
Funktion oder Sicherheit können nicht garantiert werden, vor allem auch weil dieses Script von einem Anfänger 
erstellt wurde. 
 
TODO: 
* englische Kommentare
* Bessere Hilfeübersicht
* lesbarer machen


