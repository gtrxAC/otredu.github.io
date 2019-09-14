## Harjoitukset 2: Fanikauppa

### Yleistä

Tehtävänä on suunnitella prototyyppi fanikaupalle. Fanikauppa on ReactJS:llä toteutettava Single Page Application. Voit valita kaupan aiheen vapaasti. Kaupassa voidaan myydä esimerkiksi jonkin urheiluseuran tms. tuotteita.

### Toiminnot

1. Tuotteiden selailu

Käyttäjä voi selailla myynnissä olevia tuotteita. Tuotteista näytetään kuva, lyhyt nimi sekä kappalehinta (euroissa). Sivuston tilaaja haluaisi, että kerrallaan näytettäisiin vain yksi tuote. Voit itse valita millä tavoin tuotteiden selailu tapahtuisi, pyri kiinnittämään huomiota sovelluksesi käytettävyyteen. Prototyypissä tulisi olla vähintään kolme tuotetta.
Tuotteita voisivat olla...

- Muki
- Lippis
- T-paita
- Juliste

2. Tuotteiden lisääminen ostoskoriin

Kun käyttäjä haluaa lisätä tietyn tuotteen ostoskoriin täytyy häneltä varmistaa myös kappalemäärä. Ostoskoriin lisätään haluttu määrä tuotetta ja kasvatetaan ostoskorin kokonaishintaa vastaavasti.

- Ostoskori voi olla samalla sivulla, näytä sisältö mikäli tuotteita on lisätty ostoskoriin.
- Tässä harjoituksessa keskeinen asia on tilamuuttujien käsittely (*useState*).

3. Ostoskorin tyhjentäminen

Käyttäjä voi tyhjentää ostoskorin sisällön eli tyhjentää kaikkien lisättyjen tuotteiden määrät. Tällöin myös tilauksen kokonaishinta tyhjennetään.

4. Tilauksen vahvistaminen

Käyttäjä voi painaa nappia "Vahvista tilaus". Käyttäjältä pyydetään tällöin yhteystiedot tilauksen lähettämistä varten. Vaaditut tiedot ovat sähköpostiosoite (email), nimi, lähiosoite, postiosoite sekä postitoimipaikka. Mikäli kaikki tiedot on syötetty käyttäjälle annetaan viesti "Paketti lähetetty!" ja kaikki henkilön sekä ostoskorin tiedot tyhjennetään.

### Edistyneet toiminnot

5. Alennus

Tuotteiden tilauksesta saa alennuksen kokonaissummasta seuraavan taulukon mukaan:
- Kokonaissumma 100 €, alennus 2.5%
- Kokonaissumma 250 €, alennus 4%
- Kokonaissumma 500 €, alennus 10%

6. Ostoskorin hallinta

Käyttäjä voisi hallita ostoskorin tuotteita siten, että voidaan poistaa jokin tietty tuote kokonaan tai muuttaa tietyn tuotteen kappalemäärää.

7. Kirjautuminen

Kun käyttäjä tulee ensimmäistä kertaa sivulle hänelle näytetään kirjautumissivu, jossa pyydetään käyttäjätunnus sekä salasana. Prototyypin tunnukset ovat "proto" ja salasana "proto". Mikäli tunnukset syötetään oikein näytetään käyttäjälle fanikaupan etusivu ja tuotteiden selailu.