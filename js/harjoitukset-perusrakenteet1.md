## Harjoitukset 1

**Ennen näitä harjoituksia tutustu materiaaliin [JavaScript-alkeita](../js/alkeita.html).**

Tee Visual Studio Code:lla uusi tiedosto, nimeä se *harjoitukset1.js*. Avaa VS:n terminaali ja aja koodi kirjoittamalla konsoliin: *node harjoitukset1.js*.

### Tehtävä 1: Merkkijonojen yhdistäminen

Tee funktio, joka saa parametrina merkkijonon *nimi* ja palauttaa tervehdystekstin "Hei, \< nimi \>, mitä kuuluu?". Kutsu funktiota kahdella eri nimellä ja tulosta funktion palauttamat merkkijonot konsolille.

### Tehtävä 2: Neliöön korottaminen

Tee funktio, joka saa parametrina yhden luvun ja korottaa sen potenssiin 2. Kutsu funktiota kahdella eri arvolla ja tulosta funktion palauttamat arvot konsolille.

### Tehtävä 3: Täysi-ikäisyys

Tee funktio, joka saa parametrina iän ja palauttaa merkkijonon "täysi-ikäinen" jos ikä on 18 tai yli, muussa tapauksessa palautetaan "alaikäinen". Kutsu funktiota kolmella eri arvolla ja tulosta funktion palauttamat arvot konsolille.

### Tehtävä 4. Suurempi luku

Tee funktio, joka joka saa kaksi lukua (x ja y) parametrina ja palauttaa merkkijonon "Annetuista luvuista x ja y, suurempi on ___". Kutsu funktiota kolme kertaa ja tulosta funktion palauttamat arvot konsolille.

Esimerkkitulostus:

![vertailu](./img/vertailutulostus.PNG)

### Tehtävä 5. Kolmion pinta-ala

Tee funktio, joka saa kaksi lukua parametrina (kanta ja korkeus) ja laskee ko. kolmion pinta-alan. Pyöristä pinta-ala yhden desimaalin tarkkuuteen. Kutsu funktiota kaksilla eri arvoilla ja tulosta tiedot konsolille.

Vihje 1: kanta kertaa korkeus jaettuna kahdella.
Vihje 2: pyöristäminen yhde desimaalin tarkkuuteen: kerro pyöristettävä luku kymmenellä, pyöristä saatu luku (Math.round), jaa pyöristetty luku kymmenellä.

<!-- ![pyöristys](./img/round_example.PNG) -->
<img src="img/round_example.PNG" alt="pyöristys" width="150"/>

### Tehtävä 6. Osamäärä

Tee funktio, joka saa kaksilukua (jaettava, jakaja) ja laskee näiden osamäärän. Varmista ennen jakolaskua, että jakaja ei ole nolla (jos se on nolla palauta merkkijono "nollalla ei voi jakaa"). Kutsu funktiota kaksilla eri arvoilla ja tulosta tiedot konsolille.

### Tehtävä 7. Robotin värianalyysi

Koodaa taulukon avulla funktio, joka päättelee aallonpituuden avulla mitä väriä robotti näkee. Jos funktion syöte ei osu millekään alueelle, palauta *null*. Kutsu funktiota kolmella eri arvoilla ja tulosta tiedot konsolille.

![Värikartta](./img/robocolors.png)

<iframe width="640" height="360" src="https://web.microsoftstream.com/embed/video/a679cbf9-fb1a-4d87-b08d-bb50940faf98?autoplay=false&amp;showinfo=true" allowfullscreen style="border:none;"></iframe>

### Tehtävä 8. Taksimatka

Tee funktio, jonka avulla voit laskea taksimatkan suuruuden euroissa, kun tiedetään matkustajien määrä ja kuljetut kilometrit. Tarkista myös funktion saamat arvot, että ne ovat järkeviä ja jos ne eivät ole palauta "tarkista tiedot".

Taksimatkan hinta lasketaan seuraavasti:

| Henkilöitä  |  €/km  |
| ------------- |:-------------:|
| 1-2           |     1,6    |
| 3-4           |     1,9    |
| 5-6           |     2,0    |
| yli 6         |     2,2    |

Aloitusmaksu on 5,40€

### Tehtävä 9. Pyöristys

Tee funktio, joka pyöristää desimaaliluvun lähimpään kokonaislukuun "tie-breaking"-sääntönä "pyöristä nollasta poispäin": Kun x on positiivinen, pyöristetään alaspäin (floor) lauseke: (x + 0,5) ja kun x on negatiivinen, pyöristetään ylöspäin (ceil) lauseke: (x – 0,5). Kutsu funktiota kolmella eri arvoilla ja tulosta tiedot konsolille.

<!-- ![pyöristysesimerkki](./img/floor_ceil_example.PNG) -->
<img src="img/floor_ceil_example.PNG" alt="pyöristysesimerkki" width="150"/>

### Tehtävä 10. Tuotteen hinta

Tee funktio, joka laskee tuotteen kokonaishinnan, kun sen parametrit ovat hinta ja ALV-prosentti (desimaalilukuna). Ennen ALV:in lisäämistä hinnasta vähennetään alennus seuraavien ehtojen mukaisesti:

- hinta on välillä 100 - 200€ alennus 5%
- hinta on välillä 200 - 500€ alennus 10%
- hinta on 500€ tai yli alennus 15%

Kutsu funktiota kolme kertaa eri arvoilla ja tulosta tiedot konsolille.

Vihjeet:

Alennuksen prosenttikertoimet laskeminen:
- alennus on 10% --> prosenttikerroin on 0.9
- alennus on 20% --> prosenttikerroin on 0.8
jne

Hinnan korotuksen (alv nostaa hintaa) prosenttikertoimen laskeminen:
- jos alv on 24% --> prosenttikerroin on 1.24
- jos alv on 19% --> prosenttikerroin on 1.19
jne

Lopullinen hinta lasketaan:
hinta x alennuksen prosenttikerroin x alv:in prosenttikerroin

### Lisätehtävä 1

Korjaa edellisiä funktioita niin, että ne tarkistavat kaikki saamansa syötteet ja virhetilanteessa heittävät poikkeuksen (esim. nollalla ei saa jaakaa, syötteet eivät ole lukuja, liian vähän parametreja):

```js
 throw new Error('nollalla ei voi jakaa');
```

Kun käytät tällaista funktiota, joka heittää poikkeuksen, kutsu sitä try-catch-lauseen sisältä:

```js
try {
  console.log(division(100, 0))
}
catch(err) {
  console.log(err);
}
```

<!-- ### Lisätehtävä 2

Asenna JEST-yksikkötestaus kirjasto ja kirjoita yksikkötestit em. funktioille.

Testit kirjoitetaan erilliseen tiedostoon, jonka nimen pitää olla muotoa *.test.js.

Testattava koodi on oma moduulinsa, jonka funktiot pitää *export*:ata

```js
  module.exports = { summa, ikatesti };
```

Testitiedostossa ne otetaan käyttöön *require*:n avulla:

```js
const { summa, ikatesti } = require('./harjoitukset1'); 

test('yhteenlasku kokonaisluvuilla', () => {
    const tulos = summa(2, 3);
    expect(tulos).toBe(5);
  });
```

Katso tarkemmat ohjeet JEST:in asennuksesta ja ajamisesta:

- [JEST:in asennus](../testaus/jest.html)
- [JEST alkeet](../testaus/jest-alkeet.html)
- [JEST esimerkkikoodi](../testaus/demo1.html) -->