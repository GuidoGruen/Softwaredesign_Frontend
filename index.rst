Demo Launcher
==============

Mit unserer Anwendung wollen wir Mitarbeitern des Instituts für 
Intelligente Interaktive Ubiquitäre Systeme die Planung und Inszenierung 
von Vorstellungen und Demonstrationen der Geräte im Labor erleichtern. 
Die Anwendung soll die Effizienz bei der Planung und Durchführung von 
Vorstellungen und Demonstrationen erhöhen, indem sie den manuellen 
Arbeitsaufwand minimiert und Mitarbeitern mit weniger spezifischem 
Fachwissen eine sichere Durchführung ermöglicht.

Dieses Projekt entsteht im Rahmen der Veranstaltung Softwaredesign bei 
Prof. Dr. Thomas Schlegel an der Fakultät Digitale Medien der
`Hochschule Furtwangen <https://www.hs-furtwangen.de/>`_.

Das Projekt auf `GitHub <https://github.com/GuidoGruen/Softwaredesign_Frontend.git>`_

.. note::

   Dieses Projekt befindet sich noch in Entwicklung.


Nutzerhandbuch
==============

Allgemeine Informationen
---------------
Unsere Anwendung ermöglicht das Erstellen, Bearbeiten und Abspielen von Szenarien, 
die aus einer oder mehreren Phasen bestehen. Zu jeder Phase können beliebig viele 
Geräte hinzugefügt werden, die wiederum verschiedene Demomaterialien besitzen können.

Szenarien
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Das Herzstück der Anwendung bilden **Szenarien**. Diese können automatisch **Geräte** starten 
und bei bedarf Szenarien oder Medien (**Demomaterial**) auf diesen laden. Außerdem ermöglichen sie eine 
Steuerung dieser Medien.
Szenarien werden passend zu einem bestimmten Zweck erstellt und sind immer dann nützlich, 
wenn mehr als ein Gerät genutzt werden soll oder Medien auf einem Gerät gesteuert werden 
sollen.
Beispiel Demonstration VR-Brille: Es soll zur Demonstration eine Szene in einer VR-Brille 
gezeigt werden. Damit aber auch Außenstehende davon profitieren können, sollen zusätzliche 
Informationen auf einem nebenstehenden Bildschirm gezeigt werden. Bei einer manuellen 
Steuerung müssen also zunächst die VR-Brille sowie der Bildschirm gestartet werden. Nach dieser 
Startphase setzt jemand die VR-Brille auf, um dort die gewünschte Szene zu laden. Außerdem muss 
die PDF-Datei mit Zusatzinformationen auf dem Bildschirm geladen und geöffnet werden. Erst dann kann die 
eigentliche Demonstration der Szene beginnen - doch was passiert, wenn ein Fehler auftritt und die 
Szene neu geladen werden muss? Der zuständige Labormitarbeiter muss die Demonstration unterbrechen, 
um die Szene manuell neu zu laden.
Szenarien vereinfachen diesen gesamten Ablauf: Die beiden gewünschten Geräte, die VR-Brille und der 
Bildschirm, werden zu einem Szenario hinzugefügt. Anschließend wird das gewünschte Demomaterial für 
beide Geräte festgelegt - die Szene für die VR-Brille und die PDF-Datei für den Bildschirm. Anschließend 
wird das Szenario gespeichert und kann nun gestartet werden. Beim Start werden die beiden benötigten 
Geräte automatisch angeschaltet und sobald dieser Vorgang abgeschlossen ist, wird das entsprechende 
Demomaterial geladen. Die Demonstration ist also nun ohne manuelle Eingriffe bereit. Und falls es zu 
Problemen kommt und die Szene neugeladen werden muss, kann das einfach über einen Klick in unserer 
Anwendung geschehen. Ebenso kann innerhalb der PDF-Datei auf die nächste oder vorherige Seite geschaltet 
werden.

Bei komplexeren Szenarien mit mehr Geräten können außerdem verschiedene **Phasen** angelegt werden, um den 
Ablauf der Demonstration zu vereinfachen.


Phasen
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Ein Szenario hat immer mindestens eine **Phase**. Dies ist ausreichend für simple Szenarien mit wenigen Geräten 
oder Demomaterial. Sind jedoch mehr Geräte vorhanden oder möchte man innerhalb einer Demonstration mehrere 
Geräte oder Demomaterialien gleichzeitig starten, kann man dies über Phasen vereinfachen. Möchte man also 
zuerst eine Szene auf einer VR-Brille zeigen und anschließend Informationen darüber auf zwei verschiedenen 
Bildschirmen enzeigen, kann man dafür zwei Phasen erstellen: Die erste startet die VR-Brille und öffnet die 
entsprechende Szene, die zweite startet die beiden Bildschirme und öffnet darauf die gewünschten Dateien.
Der Nutzer kann dabei entscheiden, wann er in die nächste Phase wechseln möchte. In einer Phase nicht 
benötigte Geräte werden außerdem automatisch abgeschaltet - in diesem Fall ist also in Phase eins nur die 
VR-Brille aktiv, in Phase zwei wird sie abgeschaltet und stattdessen die beiden Bildschirme eingeschaltet.

Geräte
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
**Geräte** bilden den wesentlichen Bestandteil von Szenarien. Sie müssen zunächst zur Anwendung hinzugefügt werden, 
um später innerhalb eines Szenarios angesteuert werden zu können. Nach dem Hinzufügen können dann innerhalb 
eines Szenarios die gewünschten Geräte ausgewählt werden.

Unterstützte Gerätetypen:
- VR-Brillen
- Bildschirme

Demomaterial
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Optional kann innerhalb eines Szenarios auch **Demomaterial** zu bestimmten Geräten hinzugefügt werden. Dies wird 
beim Start des Szenarios automatisch geladen und abgespielt und kann zudem - je nach Art des Demomaterials - 
über die Anwendung gesteuert werden. Ein Gerät kann auch mehr als ein Demomaterial besitzen. Der Nutzer kann 
dann während der Demonstration zwischen den hinzugefügten Demomaterialien wechseln.

Untersützte Dateitypen:
- .PDF
- .mp4

.. note::

   Achtung: Nicht jedes Gerät unterstützt jeden Dateityp. Kompatible Geräte für jeden Dateityp werden in der 
   Anwendung dargestellt.

