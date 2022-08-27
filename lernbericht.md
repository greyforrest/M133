# Lern-Bericht
Völlmin Melanie

## Einleitung

Wir behandeln in diesem Modul Webapplikationen mit JSF.

## Was habe ich gelernt?

Ich habe gelernt, dass man mithilfe des "PropertyActionListener" ganz einfach bei einer Aktion Daten im Hintergrund weitergeben kann.

## Beschreibung

Der PropertyActionListener wird nicht normal wie die anderen Tags benutzt, sondern sieht folgendermassen aus: <f:setPropertyActionListener/>. Er bekommt die Attribute "target" und "value". Value ist der Wert, der weitergegeben wird. Target gibt an, wohin der Wert weitergegeben wird, zum Beispiel kann er in einer Variable in einer Bean gespeichert werden. Um diesen Tag braucht es jedoch eine Aktion, zum Beispiel einen CommandLink oder einen CommandButton. Sobald dieser gedrückt wird, wird dann dieser Wert weitergeleitet.
Gebraucht haben wir den PropertyActionListener für eine kleine Charakterdesign-Webapp. Dabei ging es darum, dass man auf eines von zwei Bilder klickt und je nach Bild ein anderer Wert vermerkt wird. Hier das Beispiel, wie es auf der Website aussieht und der Code, der dahinter steckt: 
![image](https://user-images.githubusercontent.com/69569613/187029174-84a4a12c-0efd-4bc2-8f38-3384cc59d1d3.png)
```
        <!-- Das ganze muss in ein Formular -->
        <h:form>
            <!-- CommandLink, der auf eine neue Seite weiterleitet -->
            <h:commandLink action="chooseEyes.xhtml">
                
                <!-- Der Link wird als Bild angezeigt -->
                <h:graphicImage value="/9954_PokemonBilder/h.png"/>
                
                <!-- PropertyActionListener, der beim Klick auf den Link Infos weiterleitet -->
                <f:setPropertyActionListener target="#{bean.skin}" value="h"/>
            
            </h:commandLink>
            
            <!-- Dasselbe nochmals mit einem anderen Bild -->
            <h:commandLink action="chooseEyes.xhtml">
                <h:graphicImage value="/9954_PokemonBilder/d.png"/>
                <f:setPropertyActionListener target="#{bean.skin}" value="d"/>
            </h:commandLink>
        </h:form>
```

## Verifikation

Am kurzen Text zu dem PropertyActionListener kann man erkennen, dass ich verstanden habe, wie diese funktionieren und angewendet werden. 
Im Code erkennt man nochmals, dass ich den PropertyActionListener auch richtig anwenden kann. 
Das Bild bestätigt dies ebenfalls, da diese Website ja aus dem Code resultiert.

# Reflektion zum Arbeitsprozess

Ich bin mit meiner Arbeit in diesem Modul (bis jetzt) sehr zufrieden. Ich nehme den neuen Stoff schnell auf und kann ihn sofort anwenden, wie zum Beispiel eben den PropertyActionListener. Ich habe den Auftrag dazu schnell gelöst und konnte das Programm ohne Probleme starten.

Ich habe jedoch leider immernoch nicht wirklich verstanden, wie ich in einem völlig neuen Projekt xhtml mit JSF verwenden kann. Wenn man eine neue Webapplikation erstellt, entsteht ja als Basis immer eine html-Datei. Diese muss dann gelöscht und eine xhtml-Datei hinzugefügt werden, und dann fehlt noch das web.xml-File und die richtigen Links für den JSF-Teil.

**VBV**: Ich möchte mich gerne, sobald wir wieder direkten Unterricht haben, bei Herrn Colic mal darüber informieren, ob es einen einfacheren Weg gibt oder immer dieser Umweg gemacht werden muss. 
