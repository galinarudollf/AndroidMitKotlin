<!--
author:   Galina Rudolf

email:    galina.rudolf@informatik.tu-freiberg.de

logo:     https://upload.wikimedia.org/wikipedia/commons/c/cb/Kotlin_vs_java.jpg

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Beispiel eines Foliensatzes mit
          Verwendung von LiaScript.

translation: Deutsch  translations/German.md
-->

# **<font color=red>Android meets Kotlin (oder Android mit Kotlin)</font>**


## Motivation


### Gibt es eine Welt ohne Smartphone?

                        {{1-2}}
*************************************************************
![Smartphone](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/Bild1.jpg?raw=true "Quelle")<!--style="width:75%"-->

[Quelle: rawpixel.com](https://www.rawpixel.com)
*************************************************************


                        {{2}}
*************************************************************
Vielleicht ein besserer Beweis:

![Smartphone-Statistik](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/anzahl-der-nutzer-von-smartphones-in-deutschland-bis-2019.png?raw=true)<!--style="width:75%"-->

[Quelle: Statista](https://de.statista.com/statistik/daten/studie/198959/umfrage/anzahl-der-smartphonenutzer-in-deutschland-seit-2010/)
*************************************************************


### Warum Android?

+ Betriebssystem für mobile Geräte wie Smartphones, Netbooks …

  > Wikipedia: Android hatte als Smartphone-Betriebssystem im dritten Quartal 2016
  > einen weltweiten Marktanteil von 87,5 Prozent (nach Verkaufszahlen).

+ und Software-Plattform, {1}{d.h. erlaubt die Entwicklung von Anwendungen}


     {{2}}
Entwicklungssprachen: Java und Kotlin

     {{3-4}}
*************************************************************
*Java und Kotlin sind beide <font color=red size=5>Inseln</font>.*

![Insel Kotlin](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/Bild2.jpg?raw=true)<!--style="width:50%" -->
*************************************************************

     {{4}}
**Java und Kotlin sind beide moderne platformübergreifende objektorientierte <font color=red size=5>Programmiersprachen</font>.**


### Warum mit Kotlin?

+ eine plattformübergreifende  Programmiersprache
+ kann in Bytecode für die Java Virtual Machine (JVM) übersetzt werden, aber
  nicht nur
+ lässt sich zur Entwicklung von Android-Apps verwenden und wird seit 2017
  offiziell von Google unterstützt, seit 2019 empfohlene Programmiersprache
+ Eine moderne Programmiersprache mit interessanten Konzepten
+ syntaktisch nicht zu Java kompatibel, kann aber mit Java-Code interoperieren
+ nutzt Java Class Library (JCL)


## Mehr über Android


### Android-Architektur

![Android-Architektur](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/Bild3.png?raw=true)<!--style="width:100%; max-width: 800px"-->

Quelle: Universität Trier, Bernhard Baltes-Götz, Einführung in die Entwicklung
von Apps für Android 8

     {{1-2}}
Anwendungsrahmen (Android Application Framework)

     {{2-3}}
Android Laufzeitumgebung

     {{3}}
Basis: Linus-Kernel

### Build-Prozess

Warum wir Java und Kotlin kombinieren können … und Bytecode ist nur der erste Schritt…

<div>

<!--
style=" width: 30%;
        float: right;"
-->
````ascii
+----------------------------+
|   .java                    |
|   .kt                      |
+-------------+--------------+
              |
              V
.----------------------------.
|   Compiler                 |
'-------------+--------------'
              |
              v
+----------------------------+
|   .class                   |
+-------------+--------------+
              |
              v
.----------------------------.
|    dx                      |
'-------------+--------------'
              |
              v
+----------------------------+
|   .dex                     |
+-------------+--------------+
              |
              v
.----------------------------.
|   apk                      |
'-------------+--------------'
              |
              v
+----------------------------+
|   .apk                     |
+----------------------------+
````
![Build-Prozess](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/Bild4.png?raw=true)<!--style="width:60%"-->

[Quelle: https://developer.android.com/studio/build](https://developer.android.com/studio/build)

</div>


### Was ist eine Komponente, welche und wie viele gibt es in einer App?

![Android-Komponenten](https://github.com/galinarudollf/AndroidMitKotlin/blob/master/images/Bild5.jpg?raw=true)<!--style="width:60%"-->

[Quelle: https://www.edumobile.org](https://www.edumobile.org)

    {{1-2}}
**Activity (Aktivität):** präsentiert eine Bildschirmseite mit Bedienelementen.  

    {{2-3}}
**Service (Dienst):** führt Aufgaben im Hintergrund aus und hat keine Bedienoberfläche. Er kann von einer anderen Anwendungskomponente gestartet oder gebunden werden

    {{3-4}}
**Broadcast Receiver (Empfangen von Nachrichten):** kann auf Nachrichten reagieren, die vom System oder von Anwendungen stammen . Er hat keine Benutzeroberfläche und ist nur kurzzeitig aktiv, kann aber Aktivitäten oder Dienste starten.

    {{4-5}}
**Content Provider:** verwaltet Daten, abstrahiert darunterliegende Schicht (z. B. eine Datenbank). Er kann über erteilte Berechtigungen die Daten anderen Anwendungen zur Verfügung stellen.

    {{5}}
und über Intents sprechen wir später

## Kotlin

### Datentypen

Nummerische Datentypen

Quelle: [https://kotlinlang.org/docs/reference/basic-types.html](https://kotlinlang.org/docs/reference/basic-types.html)

{{1-2}}
*************************************************************
Ganze Zahlen

<!-- data-type="none" -->
| Type    | Size (bits) | Min value | Max value  |
|:------- |:----------- |:--------- |:---------- |
| `Byte`  | $8$         | $-128$    | $127$      |
| `Short` | $16$        | $-32768$  | $32767$    |
| `Int`   | $32$        | $-2^{31}$ | $2^{31}-1$ |
| `Long`  | $64$        | $-2^{63}$ | $2^{63}-1$ |
 *************************************************************

    {{2}}
Fließkommazahlen


## Literatur

https://developer.android.com/guide/

https://developer.android.com/kotlin/

https://de.wikipedia.org/wiki/Kotlin_(Programmiersprache)

http://helmbold.de/artikel/kotlin/

http://helmbold.de/artikel/java-kotlin/

https://developer.android.com/kotlin/


## Ausserhalb des Tellerrandes


### Boolesche Funktion

> Eine Boolesche Funktion (auch logische Funktion) ist eine mathematische Funktion
> der Form $F : B^n → B^1$. $B$ ist dabei eine Boolesche Algebra.

#### Formen von Booleschen Funktionen

**DNF**:
$$
f(\underline x)=\bar x_0 x_1 x_2 \vee  x_0 \bar x_1 x_2 \vee  x_0 x_1 \bar x_2
$$
**ANF:**
$$
f(\underline x)=\bar x_0 x_1 x_2 \oplus  x_0 \bar x_1 x_2 \oplus  x_0 x_1 \bar x_2
$$
**KNF:**
$$
f(\underline x)=(x_0 \vee x_1 \vee x_2) \wedge  (x_0 \vee x_1 \vee \bar x_2) \wedge ( x_0 \vee \bar x_1 \vee x_2) \wedge
(\bar x_0 \vee x_1 \vee x_2) \wedge (\bar x_0 \vee  \bar x_1 \vee \bar x_2)
$$

Und das wäre eine ganz andere Formel ;-):
$$
   \sum_{i=1}^\infty\frac{1}{n^2}
        =\frac{\pi^2}{6}
$$


#### Darstellungsformen einer Booleschen Funktion

+ Ausdruck
+ Karnaugh-Diagramm

<!--style="color: red"-->Beispiel:

<div>
<!--
style=" width: 49%;
        max-width: 200px;
        float: right;"
-->
````ascii
c                   f
  +---+---+---+---+
0 | 0 | 1 | 1 | 1 |
  +---+---+---+---+
1 | 1 | 0 | 1 | 1 |
  +---+---+---+---+
    0   1   1   0   b
    0   0   1   1   a
````
<!--
style=" width: 49%;
        float: left;"
-->
$$
f_1(a,b,c)=a \vee  (b \oplus c)=a \vee \bar b c\vee b \bar c
$$
</div>

### Chemische Formeln

{|>}{was müssen wir darüber wissen?}

    --{{1}}--
Eine chemische Formel beschreibt die Zusammensetzung chemischer Verbindungen.

#### Formelschreibweisen

+ Verhältnisformel
+ Summenformel
+ Strukturformel
+ Kristallchemische Strukturformel

Beispiele:

<div>
<!--
style=" width: 49%;
        max-width: 200px;
        float: right;"
-->
````ascii
    H
    |
H - C - H
    |
    H
````
<!--
style=" width: 49%;
        float: left;"
-->
$$CH_4$$
</div>

## Was alle interessiert

Luftemperatur am 21.9.2020 in Dresden/Klotzsche

| # Messung | Temperatur |
| ---------:| ----------:|
|         0 |    14.1 C° |
|         1 |    13.4 C° |
|         2 |    12.6 C° |
|         3 |    10.9 C° |
|         4 |    10.1 C° |
|         5 |    10.1 C° |
|         6 |     9.7 C° |
|         7 |    10.3 C° |
|         8 |    12.9 C° |
|         9 |    14.5 C° |
|        10 |    17.7 C° |
|        11 |    20.3 C° |
|        12 |    21.6 C° |
|        13 |    22.3 C° |
|        14 |    23.1 C° |

Quelle: [https://meteostat.net](https://meteostat.net)

## Und zu guter Letzt

Zwei Informatiker-Witze:

+ Es gibt genau 10 Typen von Menschen. Solche, die Binärzahlen verstehen und solche, die es nicht tun.
+ PnP = Plug'n'Pray

Wer sie nicht versteht, kann sie sich im folgenden Video erklären lassen:

!?[IT- und Programmierer-Witze erklärt](https://www.youtube.com/watch?v=w2PNEBw1V_s)
