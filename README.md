Alkuperäinen opas:

[CSS Tutorial – Full Course for Beginners](https://www.youtube.com/watch?v=OXGznpKZ_sA)
[the superfast colorpalette generator](https://coolors.co/)
[WebAIM (mm. kontrastichecker)](https://webaim.org/resources/contrastchecker/)
[Flex layout CSS -peli](https://flexboxfroggy.com/#fi)
[Grid layout CSS -peli](https://cssgridgarden.com/#fi)

## Muistiinpanoja

### Kokomääritykset

Fonttikoko

Fonttikoon määrityksessä käytetään usein *rem*-mittayksikköä, jolloin käytetyt määritykset ovat 
suhteessa juurielementin fonttikokooon.

- sivujen toteuttajan ei ole syytä määrittää juurielementin fonttikokoa vaan jätetään se selaimen / käyttäjän valittavaksi.
- rem eli 'root em'
- koko siis suhteessa juurielementtiin, eikä esim. sisältävään elementtiin
- jos taas käytössä em, niin silloin kokoa suhteutetaan sisältävään elementtiin!

Tilamääritykset

- marginaaleja ja padding-asetuksia määriteltäessä kannattaa puolestaan käyttää *em*-mittayksikköä
- Kun määritetään elementin fonttikoko, elementin tilanmäärityksessä (esim. padding) käytettävä em. suhteutetaan tähän fonttikokoon.
- jos elementin fontti-kokoa ei määritetä, voidaan käyttää rem-mittoja myös marginaaleissa ja täytöissä.

Leveys

- palstan leveyttä voi määrittää ch mittayksiköllä, jolloin yksi ch vastaa käytetyn fontin & fonttikoon 0-merkin leveyttä.
- vw:n sijasta kannattaa käyttää prosentteja....

Korkeus

- mikäli haluaa, että elementin korkeus on 100vh, niin kannataa käyttää: min-height: 100vh. Tällöin kompoentti voi kasvaa, mikäli sisältö ylittää sivunkorkeuden.

### Box Model

css-reset lohkossa käytetään usein box-sizing asetusta. Tämä määrittää sen, kuinka komponentin koko lasketaan. Jos esim. elementin leveydeksi on määritetty 400px
- box-sizing: content-box => elementin sisäosan leveys on 400px
- box-sizing: border-box => elementin sisällön, reunan ja täytön yhdeislevyes on 400 px

### Linkkien muotoilu

- yhdistä linkkien pseudomuotoiluissa luokat: a:hover ja a:focus 

### Miniporojekti

- a on normaalisti inline-elementti. tällöin background kattaa vain tekstin taustan. Display ominaisuus voidaan vaihtaa block-elementiksi, jolloin a-elementti kattaa käytettävissä olevan leveyden. Kätevää kun haluaa esim. linkkilistalla käyttää hover-efektiä

### Display

- listan saa kulkemaan vaakasuunnassa, kun laittaa LI elementille ominaisuudeksi display: inline-block

### Float

- Irroittaa elementin 'normaalivirtauksesta'. Saattaa aiheuttaa esim. yllätyksiä, kun 'kellutetun' elementin sisältävä elementti kattaa vain osan alueesta. (Voidaan korjata esim. display: flow-root määrityksellä)

### Position

- absolute määritys tarvitsee emoelementin, jonka suhteen absoluuttiset arvot toteutetaan. Mikäli tällaista ei ole asetettu, arvot (left, top..) perustuvat selaimen ikkunaan
- relative liikuttaa elementtiä suhteessa sen oletuspaikkaan
- fixed pysyy paikallaa, top, left ... asemoituu absoluuttisesti suhteessa sivun sisältöön.
- sticky pysyy näytöllä niin kauan kuin sen sisältävä elementti on näytöllä


### Flex

- flex-direction, missä suunnassa täytetään. Oletuksena rivi
- justify-content: miten sijoitetaan täyttösuunnassa: alku, loppu, keskellä jne..
- align-items: miten sijoitetaan täyttösuuntaa kohtisuorassa olevan tilan puitteissa.

### Grid

- grid-template-columns määrityksessä voi käyttää yhtä aikaa kiinteitä ja fraction arvoja, esim: grid-template-columns: 100px 1fr 1fr;

### Image

- css reset osuuden: img {display: block;} muuttaa kuvat inline-elementeistä block-elementeiksi, jolloin niiden alla oleva pieni oletus marginaali häviää

### Media Queries

- Jotta media queryt toimisivat, pitää seuraava määritys löytyä HTML HEAD sectiosta: <meta name="viewport" content="width=device-width, initial-scale=1.0">
- esimerkin tapauksessa korkeuksia määritetty: sivu vähintään 100vh & main: flex käytä kaikki vapaa tila .. joten koko sivu aina täyttyy.

### Pseudo

- :target pseudo-luokalla voidaan määrittää esim. linkin kohteena olleelle kortille eri värinen tausta tms.
- nt-child(x) laskee järjestyksen sen perustella, miten elementit on lisätty sivulle. Jos elementtien järjestystä on *uusittu esim. grid-layoutin order attribuutin avulla, tämä muutos ei heijastu nth-child() -valitsimen toimintaan


Linkkejä

[CSS Validointi palvelu](https://jigsaw.w3.org/css-validator/)

