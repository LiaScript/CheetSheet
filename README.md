# LiaScript CheetSheet


## Überschriften

``` Markdown
# Überschrift 1
## Überschrift 2
### Überschrift 3
#### Überschrift 4
##### Überschrift 5
###### Überschrift 6
```

## Texthervorhebungen

``` md
_kursiv_ auch *kursig*
__fett__ auch __fett__
___kursiv___ und ***fett***

~durchgestrichen~
~~unterstrichen~~
~~~durch- & unterstrichen~~~

^hochgestellt^

`unformatierter Code`
```

## Textblock

``` md
Einfache Blöcke/Absätze werden durch
Leerzeilen voneinander getrennt.

> Blöcke mit einem vorangestellten `>`
> werden hervorgeboben dargestellt.
```

## Listen

``` md
* Ungeordnete Listen werden mit einem
  vorangestellten `*`, `+` oder `-`
  markiert

  Und können mehrere Absätze enthalten.

* Liste mit Unterpunkten:

  - Es ist egal ob `-`
  + oder `+`
  * oder `*` vorangestellten surden
```


``` md
1. Sortierte Listen werden mit einer
   vorangestellten Zahl markiert:

2. Unterpunkten können auch sortierte
   oder unsortierte Listen sein:

   + Punkt 1
   + Punkt 2
```

## Trenner

``` md
Horizontale Linien werden durch min. 3
aufeinander folgende `---` definiert:

---

Beide Linien werden gleich dargestellt.

--------------------------------------

```

## Verweise

### Links

``` md
* unformatiert: https://LiaScript.github.io

* formatiert:

  + Externe Webseiten:
    - [name](https://...)
    - [name](https://... "titel")

  + Intern im Dokument:
    - [name](#Links) <-- Markdown-Überschrift
    - [name](#Links "titel")
    - [name](#12)    <-- Slide-Nummer
    - [name](#12 "titel")
```

### Bilder

``` md
Verweis auf Externe Bilder:

![alt](https://...)
![alt](https://... "titel")

Projektinterne Bilder:

![alt](/pic/image.jpg)
![alt](/pic/image.jpg "titel")
```

### Audio

``` md
Verweis auf Externe Audio-Dateien:

?[alt](https://soundcloud...)
?[alt](https://....mp3 "titel")

Projektintern:

?[alt](/sound.mp3)
?[alt](/sound.mp3 "titel")
```

### Filme

``` md
Verweis auf Externe Filme:

!?[alt](https://youtube...)
!?[alt](https://....avi "titel")

Projektintern:

!?[alt](/movie.mp4)
!?[alt](/movie.mp4 "titel")
```

### LiaScript

``` md
[preview-lia](https://...README.md)
```

## Formeln

Hierfür wird [KaTeX](https://katex.org/docs/supported.html) verwendet.

``` md
Textinterne Formeln: $ f(a,b,c) = (a^2+b^2+c^2)^3 $

Eigenständige Blöcke:

$$
   \sum_{i=1}^\infty\frac{1}{n^2}
        =\frac{\pi^2}{6}
$$
```

## Effekte

### Animationen

#### Blöcke `{{in(-out)}}`

``` md
             {{1}}
Dieser Block erscheint als erster.

{{2-3}} Dieser Block als zweiter und
verschwindet bei drei.
```

#### Micro-Animationen `{in(-out)}{content}`

``` md
             {{1}}
beliebige Markdown-Blöck und "Makro"-Animationen
können weiter {2-3}{_Micro-Anmationen_} enthalten.
Die Reihenfolge wird nur durch die {2}{Zahlen}
definiert
```

#### Multi-Block-Animationen

``` md
             {{1}}
*********************************
Mehrere Blöcke können auch mit
Sternchen abgegrenzt werden.

Und weitere {2}{Elemente} enthalten.

...
*********************************
```

### Sprachausgabe `--{{number}}--`

``` md
          --{{1}}--
Dieser ganze Absatz wird mit der default-Stimme
bei **Animationsschritt 1** mit der vorgelesen.

    --{{2 US English Male}}--
This test will be spoken out loud in English.
```

#### Verborgene Sprachausgabe

``` md
<!-- --{{1}}--
Dieser ganze Absatz wird nur vorgelesen, taucht
aber im Textbuch-Modus nicht auf!
-->
```

#### Liste aller Sprachen

Siehe auch: https://responsivevoice.org

| Female                        | Male                        |
| ----------------------------- | --------------------------- |
| UK English Female             | UK English Male             |
| US English Female             | US English Male             |
|                               | Afrikaans Male              |
|                               | Albanian Male               |
| Arabic Female                 | Arabic Male                 |
|                               | Armenian Male               |
| Australian Female             | Australian Male             |
| Bangla Bangladesh Female      | Bangla Bangladesh Male      |
| Bangla India Female           | Bangla India Male           |
|                               | Bosnian Male                |
| Brazilian Portuguese Female   | Brazilian Portuguese Male   |
|                               | Catalan Male                |
| Chinese Female                | Chinese Male                |
| Chinese (Hong Kong) Female    | Chinese (Hong Kong) Male    |
| Chinese Taiwan Female         | Chinese Taiwan Male         |
|                               | Croatian Male               |
| Czech Female                  | Czech Male                  |
| Danish Female                 | Danish Male                 |
| Deutsch Female                | Deutsch Male                |
| Dutch Female                  | Dutch Male                  |
|                               | Esperanto Male              |
|                               | Estonian Male               |
| Filipino Female               |                             |
| Finnish Female                | Finnish Male                |
| French Canadian Female        | French Canadian Male        |
| French Female                 | French Male                 |
| Greek Female                  | Greek Male                  |
| Hindi Female                  | Hindi Male                  |
| Hungarian Female              | Hungarian Male              |
|                               | Icelandic Male              |
| Indonesian Female             | Indonesian Male             |
| Italian Female                | Italian Male                |
| Japanese Female               | Japanese Male               |
| Korean Female                 | Korean Male                 |
| Latin Female                  | Latin Male                  |
|                               | Latvian Male                |
|                               | Macedonian Male             |
| Moldavian Female              | Moldavian Male              |
|                               | Montenegrin Male            |
| Nepali                        | Nepali                      |
| Norwegian Female              | Norwegian Male              |
| Polish Female                 | Polish Male                 |
| Portuguese Female             | Portuguese Male             |
| Romanian Female               | Romanian Male               |
| Russian Female                | Russian Male                |
|                               | Serbian Male                |
|                               | Serbo-Croatian Male         |
| Sinhala                       | Sinhala                     |
| Slovak Female                 | Slovak Male                 |
| Spanish Female                | Spanish Male                |
| Spanish Latin American Female | Spanish Latin American Male |
|                               | Swahili Male                |
| Swedish Female                | Swedish Male                |
| Tamil Female                  | Tamil Male                  |
| Thai Female                   | Thai Male                   |
| Turkish Female                | Turkish Male                |
| Ukrainian Female              |                             |
| Vietnamese Female             | Vietnamese Male             |
|                               | Welsh Male                  |

### Bedingte Sprachausgabe `{{|>}}` oder `{{!>}}`

``` md
                  {{|>}}
Dieser ganze Absatz wird mit der default-Stimme
vorgelesen, wenn der Nutzer auf Play klickt.

                  {{|> Deutsch Male}}
Micro-Animationen {1}{können} den gelesenen Text
verändern sowie bedingte {|>}{*Micro-*}Ausgaben.

                  {{!> 1-3}}
Bedingte Sprachausgaben sind ebenso Animationen
und können beliebig kombiniert werden
{|> 2 UK English Male}{yeah}...
```

## Quizze

### Textquiz `[[text]]`

``` md
Wie heißt die hier vorangestellte Sprache?

[[LiaScript]]
```

### Single-Choice `[(X)]`

``` md
Anzahl und Ordnung der Optionen ist beliebig.

[( )] Diese Wahl ist falsch.
[(X)] <-- __Richtig__
[( )] Auch falsh.
```

### Multiple-Choice `[[X]]`

``` md
Alle markierten Zeilen müssen ausgewählt werden:

[[ ]] nicht ausgewählt
[[X]] <-- __Richtig__
[[ ]] auch falsh.
[[X]] __auch Richtig__
```

### Matrix

``` md
Kombination von Single- und Multiple-Choice Quizzen:

[[Head 1] [_Head 2_] [**Head 3**]]
[  [X]        [ ]         [X]    ]  Weitere
[  ( )        (X)         ( )    ]  Zeilen...
```

### Auswahl `[[...|(richtig)|..]]`

``` md
Elemente werden durch | getrennt und dir richtige Option wird durch Klammern markiert:

[[ falsche Option
|  auch *falsch*
|  ( **richtig** )
]]
```

### Weitere Optionen

#### Hilfen `[[?]]`

``` md
Hilfen können mit `[[?]]` an alle Quizze angehängt
werden:

[[LiaScript]]
[[?]] Tipp 1
[[?]] Tipp 2
[[?]] ...
```

#### Erweiterte Auflösungen `***`

``` md
[[LiaScript]]
[[?]] Tipp 1
[[?]] ...
**************************************************
Einer oder mehrere Absätze die durch min. 3 `***`
abgetrennt sind und nur dargestellt werden, wenn
das Quiz gelöst wurde.

$$
   \sum_{i=1}^\infty\frac{1}{n^2}
        =\frac{\pi^2}{6}
$$
**************************************************
```

#### Weitere Prüfung `<script>`

Ein `<script>` kann an jedes Quiz angehängt werden um die Eingabe zu formatieren und zu prüfen. Nur wenn `true` zurück gegeben wird, gilt das Quiz als gelöst.

``` md
[[LiaScript]]
<script>
  // @input wird mit der Nutzereingabe ersetzt.
  let input_string = "@input";
  "liascript" == input_string.trim().toLowerCase();
</script>
```

#### Generische Quizze `[[!]]`

Die Eingaben müssen/können selber organisiert werden:

``` md
[[!]]
<script>
  Math.random() > 0.1
</script>
```

## Styling `<!-- ... -->`

``` md
<!-- style="color:red; width: 300px" -->
Die in einem vorangestellten HTML-Kommentar enthaltenen Parameter werden auf den gesamten Block angewendet. Ein **angefügter Kommentar**<!-- style='color: green' --> nur auf das vorangestellte Element. Dies eignet sich auch zum formatieren von Bildern:

![image](url)<!--
style="width: 100%; max-width: 800px"
title="ein beliebiges Bild"
onclick="alert('It started with a click!');"
-->
```

## HTML

``` md
<h2 style="...">_HTML kombiniert mit LiaScript_</h2>

<lia-keep>
  verhindert diese Kombination:

  <h2 style="...">_..._
  ---
  </h2>
</lia-keep>
```

## ASCII-Art

### Diagramme

Die verwendeten Buchstaben/Zeichen definieren die Farbe und Form der Linien und Punkte sowie deren Größe. Können keine Linien dargestellt werden, wie bei `DOTS`, so werden nur Punkte dargestellt. Alle Beschriftungen sind optional.

```md
                                        Titel
    1.9 | DOTS
        |                 ***                   (* Gauß)
      y |               *     *                 (r obere Grenze)
      - | r r r r r r r*r r r r*r r r r r r r
      a |             *         *
      x |            *           *
      i | B B B B B * B B B B B B * B B B B B
      s |         *                 *
        | *  * *                       * *  *
     -1 +------------------------------------
        0              x-axis               1
```

### Beliebige

Beliebige ASCII-Art Diagramme können als Code-Block mit dem Hinweis `ascii` versehen werden, oder durch mindestens 10 aufeinander folgenden Back-ticks.

Siehe: https://github.com/andre-dietrich/elm-svgbob

```````````````````````````````````````````````````````````````````````````` md
``` ascii
        +-------------+       .--------------.
+------#|    Box 1    |------*|    Box 2     +-------.
 \      +-------------+       '-o------------'       |
  \                            /                     |
   ^                          /                ______|______
    \                        v                |      V      |
     +--- ein ---<--- Kreislauf ---O----------|    Box 3    |
                                              |_____________|
```

`````````````````````````````````````````````````````````````````````````
╔════════════════════════════════════[×]═╗       ╭─────╮
║ Fenstertitel                           ║       │     │     ╳
╟──────────────────────────────────────┬─╢       ╵     ╷    ╱ ╲
║ Fensterinhalt                        │▲║       ╰─────╯
║                                      │░║
║                                      │░║       ┌─┬┐  ╔═╦╗  ╓─╥╖  ╒═╤╕
║                                      │░║       │ ││  ║ ║║  ║ ║║  │ ││
║                                      │░║       ├─┼┤  ╠═╬╣  ╟─╫╢  ╞═╪╡
║                                      │█║       └─┴┘  ╚═╩╝  ╙─╨╜  ╘═╧╛
║                                      │░║
║                                      │░║       ┌───────────────────┐
║                                      │░║       │  ╔═══╗ Some Text  │▒
║                                      │░║       │  ╚═╦═╝ in the box │▒
║                                      │░║       ╞═╤══╩══╤═══════════╡▒
║                                      │░║       │ ├──┬──┤           │▒
║                                      │░║       │ └──┴──┘           │▒
║                                      │▼║       └───────────────────┘▒
╚══════════════════════════════════════╧═╝        ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
`````````````````````````````````````````````````````````````````````````
````````````````````````````````````````````````````````````````````````````

## Tabellen

### Basics

``` md
| Kopf | Linksbündig | Rechtsbündig | Zentriert |
| ---- |:----------- | ------------:|:---------:|
| I.   | _Tabellen_  |         0.10 |   Son-    |
| II.  | **sind**    |         0.12 |  stiges!  |
| ...  | ^cool^      |          ... |    ...    |
```

### Datensätze

Tabellen werden in LiaScript auch als Datensätze interpretiert und geeignet visualisert. Hier wird versucht aus der Struktur der Tabelle/Daten auf die geeignete Darstellung zu schließen. Mithilfe eines vorangestellen HTML-Kommentars können weitere Einstellungen vorgenommen werden.

#### Linien-Diagramme

``` md
|   x |  y1 |  y2 |  y3 |
| ---:| ---:| ---:| ---:|
|   1 |   1 |   1 |  15 |
|   2 |   2 |   4 |  15 |
|   3 |   3 |   9 |  15 |
|   4 |   4 |  16 |  15 |
|   5 |   5 |  25 |  15 |
```

#### Punkt-Diagramme

Wenn die X-Spalte doppelte Einträge enthält...

``` md
|   x |  y1 |  y2 |  y3 |
| ---:| ---:| ---:| ---:|
|   1 |   1 |   1 |  15 |
|   1 |   2 |   4 |  15 |
|   2 |   3 |   9 |  15 |
|   2 |   4 |  16 |  15 |
|   3 |   5 |  25 |  15 |
|   3 |   3 |   1 |   4 |
```


#### Balken-Diagramme

Falls die erste Spalte keine Zahlen enthält...

``` md
| Animal/Gruppe   | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |     0.028 kg |              2 |      95 |
| Flying squirrel |     0.085 kg |             15 |      50 |
| Brown bat       |     0.020 kg |             30 |      10 |
| Sheep           |        90 kg |             12 |      95 |
| Human           |        68 kg |             70 |      10 |
```

#### Radar

Wenn der Unterschied zwischen den Spalten zu groß ist...

``` md
| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |             02 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
```


#### Torten-Diagramme

Bei nur einer Zeile...

``` md
| Music-Style 1994 | Classic | Country | Reggae | Hip-Hop | Hard-Rock | Samba |
|:---------------- | -------:| -------:| ------:| -------:| ---------:| -----:|
| Student rating   |      50 |      50 |    100 |     200 |       350 |   250 |
```

#### Parallel-Diagramm

Bei zu vielen Kategorien und Spalten...

``` md
| Country  |   GDP growth (%) | Births per woman |  ... |  ... | ... | ... | ... |
| -------- | ----------------:| ----------------:| ----:| ----:| ---:| ---:| ---:|
| Albania  |              7.5 |            1.858 |  ... | .... | ... | ... | ... |
| Andorra  | 3.57073718591123 |            1.260 |  NaN |  NaN | NaN | NaN | ... |
| Austria  | 2.17880778069679 |            1.414 | .... |  ... | ... | ... | ... |
| Byelarus |                  |                  |      |      |     |     |     |
```


#### Karten

Die erste Spalte enthält die Objekte der GeoJson-Datei...

``` md
<!--
data-type="map"
data-src="https://code.highcharts.com/mapdata/custom/europe.geo.json"
-->
| Country | percent |
| ------- | -------:|
| Albania |    73.5 |
| Andorra |    98.9 |
| ....    |      .. |
```

#### HeatMap

``` md
<!-- data-type="heatmap" -->
| Seattle |  Jan |  Feb |  Mar |  Apr |  May |  ... |
| -------:| ----:| ----:| ----:| ----:| ----:| ----:|
|       0 | 40.7 | 41.5 | 43.6 | 46.6 | 51.4 |  ... |
|       2 |  ... |  ... |  ... |  ... |  ... |  ... |
```

#### Graph

Kopf und erste Spalte sind gleich...

Ungerichtet:

``` md
| Graph |  A  |  B  |  C  |  D  |  E  |
|:----- |:---:|:---:|:---:|:---:|:---:|
| A     |  0  |  1  |  0  |  1  |  0  |
| B     |  1  |  0  |  0  |  1  |  0  |
| C     |  0  |  0  |  0  |  0  |  0  |
| D     |  1  |  1  |  0  |  0  |  1  |
| E     |  0  |  0  |  0  |  1  |  0  |
```

Gerichtet:

``` md
| Graph |  A  |  B  |  C  |  D  |  E  |
|:----- |:---:|:---:|:---:|:---:|:---:|
| A     |  0  | 12  |  0  |  1  |  0  |
| B     | -22 |  0  |  0  | 0.4 |  0  |
| C     |  0  |  0  |  0  |  0  |  0  |
| D     |  2  | 12  |  0  |  0  |  1  |
| E     |  0  |  0  |  0  |  2  |  0  |
```

Sankey:

``` md
<!-- data-type="sankey" -->
| Sankey |  A  |  B  |  C  |  D  |  E  |
|:------ |:---:|:---:|:---:|:---:|:---:|
| A      |     |  2  |     |     |     |
| B      |  3  |     |     |     |     |
| C      |  1  |  1  |     |     |     |
| D      |     |  1  |  1  |     |     |
| E      |  2  |  1  |  1  |  1  |     |
```

#### Kobination mit Animationen

``` md
<!-- data-transpose -->
| Music-Style {0-1}{1994} {1}{2014} |      Student rating |
|:--------------------------------- | -------------------:|
| Classic                           |   {0-1}{50} {1}{20} |
| Country                           |   {0-1}{50} {1}{30} |
| Reggae                            |                 100 |
| Hip-Hop                           | {0-1}{200} {1}{220} |
| Hard-Rock                         | {0-1}{350} {1}{400} |
| Samba                             | {0-1}{250} {1}{230} |
```

#### Weitere Einstellungen

* __`data-type`__: You can use `data-type="map|boxplot|barchart|..."` to overwrite the automatically identfied representation with your desired one. The names can be taken from the previous titles, it is not relevant if you use lower or upper-case. This way it is also possible to use types that cannot be automatically infered at the moment, such as Sankey or BoxPlot.

  If you do not want to show tables as diagrams, you can also use `data-type="None"` and only the table will be visible.

* __`data-show`__: Simply add this attribute or set it to true (`data-show="true"`), if you want to visualize your data immediately, without the need to click in the switch-button. It is still possible for your users to switch to the table representation.

* __`data-transpose`__: Like in the mathematical sense, set this attribute or set it to true (`data-transpose="true"`), if you want to switch rows and columns. One benefit is, that you can for example use PieChart and let your table grow vertically instead of using a horizontal monster.

* __`data-title`__: Normaly, the first cell defines the title of your diagram, but if you want larger titles and not have to write gigantic table headers, apply this attribute `data-title="Use whatever title you want to ..."`

* __`data-xlabel`__: As above, you can also define the strings for the labels, in this case for the x label

* __`data-ylabel`__: or the y label.

* __`data-src`__: Currently this attribute is used to refere to your geojson data, if you use the `data-type="Map"` representation, but this might change in the future to load and visualize data directly, such as csv.

  If you are using geojson files from external websites such as:

  https://code.highcharts.com/mapdata/

  It can be usefull to use anycors, if the data cannot be visualized due to CORS restrictions:

  `data-src="https://cors-anywhere.herokuapp.com/https://code.highcharts.com/mapdata/custom/europe.geo.json"`


## Code

Ein Code-Block wird durch min. 3 aufeinander folgende Back-ticks vom Rest abgetrennt. Das folgende Kürzel ist ist optional und spezifiziert die Sprache und damit auch das Syntax-Highlighting.

```` md
``` js
console.log("Hallo Welt")
```
````

### Ausführbarer Code

Code kann ausführbar gemacht werden, indem ein `script` tag angefügt wird. `@input` wird wir bei den Quizzen mit dem aktuellen Code vor der Ausführung ersetzt.


```` md
``` js
console.log("Hallo Welt")
```
<script>@input</script>
````

### Projekte

Mehrere Code-Segmente können direkt zusammengefasst und mit Namen versehen werden. Das vorangestellte `+` oder `-` im Titel definiert ob die Datei bei der ersten Darstellung auf- oder eingeklappt erscheint. Auf die verschiedenen Code-Segmente wird im script durch `@input(0)` und `@input(1)` verwiesen.

```` md
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.online) {
  who + " is online"; }
else {
  who + " is NOT online"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "online"     :  true
}
```
<script>
  // insert the JSON dataset into the local variable data
  let data = @input(1);

  // eval the script that uses this dataset
  eval(`@input(0)`);
</script>
````

### Default-Ausgabe `@output`

Die erste Ausgabe kann durch ein `@output`-Script-Block angehängt werden.

```` md
``` js
for (let i=0; i<5; i++)
  console.log("Hallo Welt", i)
```
``` text  @output
Hallo Welt 0
Hallo Welt 1
Hallo Welt 2
Hallo Welt 3
Hallo Welt 4
```
<script>@input</script>
````

### Weitere Optionen

Mit vorangestellten Kommentaren können auch die Code-Segment formatiert werden:

```` md
<!-- data-showGutter="false" -->
```cpp
// some C++ code without line numbers
...
```
<!-- data-readOnly="true" -->
```hpp
// some header-file with lineNumbers,
// that cannot be edited
```
<script>
...// your execution code
</script>
````

Attributes:

* `data-firstLineNumber`: change the initial line number to any number you prefer (default: `data-firstLineNumber="0"`).

* `data-fontSize`: change the default font-size, which has to be defined with `pt` (default `data-fontSize="12pt"`).

* `data-readOnly`: whether it is an executable snippet or not, there are different default values, you can either set only data-readOnly to make it read-only or pass it a boolean value (`data-readOnly="false"`)

* `data-showGutter`: same as with `data-readOnly`

* `data-tabSize`: this takes an integer to represent the default tab-size replacement (default `data-tabSize="2"`)

* `data-theme`: your default theme as in your settings is applied, but you can change this to any of the ace-themes, eg: `Chaos`, `Eclipse`, `Soliarized Light`, ...

* `data-marker`: use this to highlight aspects of your code, you have to apply the following pattern `data-marker="y1 x1 y2 x2 color type;"`. You start with a row and column and end with a row and a column. Then you can apply one of the predefined colors, for `error`, `log`, `warn`, `debug` or `info`, or you can set your own color with the css rgba function, do not use spaces in this function!

  The type is optional, but you can choose between one of the following ace-marker types: `text`, (default `fullLine`), `screenLine`

  If you want more than one marker, then simply separate different marker definitions with a colon ...


## Macros

Macros können im Kopf eines jeden Dokuments definiert werden, es gibt single-line Makros und Block-Makros, die die Struktur erhalten. Single-line Makros beginnen mit `name:` oder `@name:` und alle dazugehörigen Element müssen eingeschoben sein.

```md
<!--
author: someone who wants to create something new

@Single.line: you can add as much content as you
  want to your single-line macro!

  The only thing that is important, is to use
     indentation.

     Not __matter__ how [much](#12) it is.
-->

# Main Title

@Single.line  <-- this will be replaced at compile-time by ...

you can add as much content as you want to your single-line macro! The only thing that is important, is to use indentation. Not __matter__ how [much](#12) it is.

@author <-- by: someone who wants to create something new
```

### Block-Macros

Block-Macros beginnen mit `name` oder `@name` und werden mit `@end` abgeschlossen. Sie erhalten die Struktur:

``` md
<!--
@smile: ;-)

@block
this type of macro preserves the structure.

<h1>
@smile and you can also use macros, that
define other macros
</h2>

| Header 1   | Header 2   | Header 3   |
| :--------- | :--------- | :--------- |
| Item 1     | Item 2     | Item 3     |

<script>alert("hello world")</script>
@end
-->

# Main Title

@block
```

### Kommentare

Zwei `@@` bei single-line und drei `@@@` bei Blöcken dient als zum Kommentieren/Auskommentieren.

``` md
<!--
@@comment: this is a single line macro
  that has been commented out

@@ if you prefer it, comment blocks can
@@ be defined like this
@@ ...

@@@block-comments

start with three @s and go until the
parser reaches ...

@end
-->
```

### Überschreiben

Makros und Einstellungen können je Abschnitt überschrieben werden:

``` md
``` markdown
<!--
...
narrator: US English Female

-->

# Main Title

....

### Some other section
<!--
author: another author for this section
...
narrator: Australian Male

-->
```

### Parameterübergabe

Makros können Parameter übergeben werden `@0` bis `@n` definiert wo Parameter ersetzt werden sollen:

``` md
<!--
@highlight: <b style="color: @0">@1</b>
-->

@highlight(red,I want this text to be read and bold)
```

Parameter werden durch Komma `,` voneinander getrennt und mit Klammern eingeschlossen. Sollte ein Parameter Kommas und/oder Klammern enthalten, so können diese auch als Markdown-Code element übergeben werden

``` md
@highlight(red; fontSize: 22px,`some text with commas,,,, and (parenthesis)`)
```

Multiline ist auch möglich...

```` md
@highlight(red,```
It works also for multi-line

elements...

@highlight(green,macros can also call other macros)
```)
````

Makros sollten so organisiert werden, dass das der komplexeste Parameter als letztes übergeben wird, dann kann auch folgende Syntax verwendet werden:

```` md
``` md @highlight(red)
It works also for multi-line

elements...

@highlight(green,macros can also call other macros)
```
````

dies eignet sich vor allem bei Parametern, die JSON, YAML oder sonstigen Code enthalten...

### Wichtige Macros

#### Import

LiaScript erlaubt das impotieren und die Nutzung von JavaScript (`script:`), CSS (`link:`), Markdown (`import:`). Bei LiaScript-Dokumenten werden nur die Makros im Kopf importiert.

``` md
<!--
script: https://javascript.js
        ...js

link:   https://style.css
        ...css

import: https://ReadME.md
        ...md
-->

# Überschrift
```

#### Informationen

``` md
<!--
version:  0.0.1

author:   Autor des Kurses

email:    Kontakt@....com

comment:  Was wird behandelt, bzw. eine Kurs(z)-Vorstellung,
          In mehreren Zeilen ...

logo:     https://logo.jpg

language: de|en|es|...

narrator: Afrikaans Male|Arabic Female|Brazilian Portuguese Female|...

mode:     Presentation|Slides|Textbook
dark:     true

date:     09/09/2020

@onload
alert("some JavaScript to be executed at the start...")
@end

attribute: Erste Danksagung ....
attribute: Zweite Danksagung mit Lizenz[MIT](https://opensource.org/licenses/MIT)

translation: Deutsch  translations/German.md
translation: Français translations/French.md
translation: Русский  translations/Russian.md
-->

# Überschrift
```

#### Weitere

``` md
@uid erzeugt eine einmalige ID.

@section wird durch die Abschnittsnummer ersetzt.
```

#### Debug

Ein vorangestelltes `@` sollte den Ersetzungs-Code zeigen:

``` markdown
<!--
@highlight: <b style="color: red">@0</b>

@red_and_green:
  @highlight(@0) <i style="color: green">@1</i>
-->

@@red_and_green(red,`simply, simply, green`)
```

#### Escape

In some cases, for example if you want to pass content to a javascript string and you need to escape the content of the LiaScript content, wich could be a multiline string for example. Then you can simply add a `'` to your macro, for example:

* `@'input` will result in an escaped version of the input string
* `@'input(1)` is the same as above
* `@'1` as a parameter will also get escaped
* similarly to any other `@'macro(with, some, params)`

