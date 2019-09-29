## Die Verteiler und Harfe in der Hauptverteilerstation und wie ein Zug beladen wird.
Die Hauptverteilerstation besteht aus zwei Teilen:

1. Harfe
2. Verteiler

In der Harfe werden die Züge nach Farbe sortiert, es muss immer genug Platz für alle Züge einer Farbe auf einer Schiene
in der Harfe sein.

Vor der Harfe steht ein Stopper, der Stopper kann die Farbe eines Zuges erkennen und ein IR Signal mit einem
Code absetzen.

Der erste Stopper benachrichtigt über IR die Weichen in der Harfe, die dann sich entweder öffnen,
wenn der Farbcode ihrerer Farbe entspricht, oder schließen.

Außerdem wird der Verteiler über das gleiche IR Signal benachrichtigt.

Dieser hat eine Queue, in der alle Farben, die einfuhren, eingetragen sind.

Wenn nun ein Zug fertig beladen ist, wird der Verteiler einen IR Code für die Farbe,
die als nächstes in der Queue steht, aussenden, um die richtige Weiche am Ende der Harfe
zu öffnen und den Zug dieser Farbe vorfahren zu lassen.

Wenn dieser Zug unter dem Verteiler steht, wird dies von einem Stopper dort registiert und 
über einen neuen IR Code den Verteiler benachrichtigen.

Dieser beginnt nun die Beladung und löscht diese Farbe aus der Queue.

Wenn der Verteiler fertig ist, beginnt der Prozess von neuem.

Wenn die Queue leer ist, steht der Verteiler-Harfe Komplex still.
