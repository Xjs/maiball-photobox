# Maiball-Photobox

Der [https://www.maiball-heidelberg.de/](Maiball Heidelberg e. V.) hat 2018 eine Photobox gebaut, um auf dem Maiball eine stationäre Photographiermöglichkeit für Gäste anbieten zu können.

## Hinweise

* Die Photobox besteht aus Multiplex-Platten, die Tobias sich erstmal beim Baumarkt hat zuschneiden lassen. Die Maße stehem im Spreadsheet der FreeCAD-Datei.
In die Frontplatte haben wir zentral mit einer Lochfräse das Loch für die Linse geschnitten, seitlich darunter noch ein Loch für die Signal-LED. Die LED hat Tobias letztendlich mit angelöteten und verschrumpften Kabeln festgeleimt, auch wenn da sicherlich andere Lösungen denkbar sind. In die Rückplatte haben wir auf der Höhe des kleinen Faches eine Bohrung für einen 5,25mm Klinkenanschluss angebracht, der für die Taste (in unserem Fall ein Keyboardpedal) zum Einsatz kam.
* Sämtliche Platten wurden verschraubt und verleimt, wobei wir die Front- und Rückseite sowie die rechte Seite zum Aufklappen auf die volle Höhe (und Breite für v/h) genommen haben, damit es schöner aussieht.
* An der Seite haben wir oben zwei Scharniere angebracht und ein Loch reingefräst, durch das eine Metall"schiene" mit Bohrung für das Vorhängeschloss passt.
* Eine der Platten hatten wir auch noch für die Stromkabel angefräst, aber daran kann Tobias sich nicht mehr genauer erinnern.
* Die Elektronik ist bisher auf einem Breadboard mit nem kleinen Arduino aufgebaut, wichtig ist hier die galvanische Trennung des Kamera-Stromkreises mit einem Optokoppler. Hier gibt es zwei separate Schalter (Fokus und Auslöser), die kurz zeitverzögert ausgelöst werden.
* Die Kamera ist auf einen kleinen Mount angebracht, der im Inneren festgeschraubt ist.
* Zusätzlich hatten wir auf der Frontseite noch einen Ausschnitt angebracht, der einen Großteil der Fläche eines iPads zeigt, und hinter dem eine Plexiglasscheibe vor eifrigen Touchscreen-Nutzern schützt.
* Oberhalb und unterhalb des Ausschnittes haben wir zwei L-förmige Führungsschienen aus Holz (mit Filz verkleidet) untergebracht, in die das Tablet eingeführt werden kann.
* Der Funkauslöser für den Blitz war etwas zu hoch, weshalb wir die L-Schienen in der Mitte einschneiden mussten, aber ansonsten ist das etwa unsere Bauanleitung gewesen 🙂
* Die Kamera ist eine EOS 40D, der Auslöser ist mit deren Fernauslöser-Anschluß verbunden. (Kabel ist in diesem Fall so eines: https://www.amazon.de/dp/B014FVHHJ6, das kommt aber vermutlich auf den Kameratyp an.) Wir hatten einen Blitz mit einem https://www.amazon.de/gp/product/B01LYS8KNN als Trigger, weil einer aus dem Team ohnehin einen Godox-Blitz hat. Der Blitz war auf einem separaten Stativ montiert, mit (sehr rudimentär selbst gebastelter) Softbox und hat mit TTL-Belichtungssteuerung die (weiße) Decke angeblitzt. Die Batterien mußten alle 1-2 Stunden ausgetauscht werden, eine konstante Stromversorgung für den Blitz einzuplanen wäre daher sehr ratsam. Die Kamera war im E-TTL-Modus und ansonsten einfach Autofokus. Wir haben ein 50/1.4-Objektiv bei f/2.8 (glaubt Jannis) benutzt, etwas weitwinkliger bietet sich aber an (wir hatten nur spontan keines).
* Achso, wichtig: Der Schalter braucht einen Pull-Up-Widerstand (intern oder extern), sonst hört er nach einem Auslösen nicht mehr auf, zu feuern. Außerdem war das Klavierpedal ein Unterbrecherpedal, d.h. das Signal musste invertiert behandelt werden. Aber das müsste man auch im Code (Photobox_c.ino) sehen können
* Und Standardkram im Umgang mit Holz (Kanten entgraten, Bei Bedarf Oberfläche schleifen und behandeln) gilt natürlich auch in diesem Fall :)
