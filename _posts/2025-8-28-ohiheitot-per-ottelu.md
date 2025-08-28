---
title:  "Ohiheitot per ottelu"
layout: post
categories: korisliiga
image: images/image_nba_ohiheitot.jpg
---

Kirk Goldsberry kertoo artikkelissaan NBA joukkueiden ottavan 3p heittoyrityksiä kiihtyvällä vauhdilla. Koska NBA:n 3p heittoprosentti (noin 36%) ei ole juuri muuttunut, niin seurauksena on enemmän ja enemmän 3p ohiheittoja per ottelu. Goldsberry ehdottaakin, että nykyinen 3p-viiva on aikansa elänyt ja siihen pitäisi tehdä muutoksia (poistaa kulmakolkki kokonaan). Itse innostuin sääntökeskustelua enemmän Goldsberryn tekemästä kaaviosta, josta näkyy tyydyttävällä tavalla, kuinka runkosarjassa 2p ja 3p ohiheittojen määrä on lähestynyt toisiaan. Jopa siinä määrin, että tällä NBA:n runkosarjakaudella 3p ohiheittoja nähtiin enemmän kuin 2p ohiheittoja!

<Image
  src="images/image_nba_ohiheitot.jpg"
  width="1015"
  height="800"
  alt="Image"
  sizes="100vw"
/>


## Entä korisliiga?

Kuinka ohiheitot jakaantuvat kotoisessa miesten korisliigassa? Onko muutos ollut yhtä tasaista, ja koliseeko täälläkin 3p heitot useammin rautoihin kuin 2p heitot? Basket.fi:n tilastohistoriasta sekä nykyisestä tilastopalvelusta saa kerättyä 2p ja 3p heittojen määrät kaudesta 1984-1985 lähtien. Toisin kuin Goldsberryllä, jolla on kaaviossaan vain NBA:n runkosarjaottelut, niin käyttämässäni korisliigatilastoissa on mukana kaikki kauden ottelut.1 “Hetken” jumpattuani ggplot2:ssa minäkin osasin tehdä Goldsberryä mukailevan kaavion.

Kaaviostani näkyy, kuinka myös korisliigassa trendi on ollut saman suuntainen. 3p ja 2p ohiheittojen määrä on lähentynyt toisiaan. Suomessa 3p ohiheittojen määrä ylittivät 2p ohiheittojen määrän jo kaudella 2020-2021. Tuo kausi oli tietenkin koronakausi, jolloin pelattiin vain 20 ottelua runkosarjaa + pleijarit, joten kausi oli poikkeuksellinen. Tuon poikkeuskauden jälkeen otettiin käyttöön ylempi- ja alempijatkosarja, ja näillä kausilla on taas normaaliin tapaan viskottu ohi enemmän 2p kuin 3p heittoja. Ero ohiheittojen määrässä ei kuitenkaan ole iso.

## 3p heittotahti eri sarjoissa

NBA:ssä ja miesten Korisliigassa heitetään enenevässä määrin 3p heittoja, mutta kuinka usein niitä 3p heittoja oikein otetaan näissä sarjoissa? Katsoessa klippejä NBA:sta tuntuu, että pelaajat heittävät jatkuvasti hätäisiä siirtymä pull up -kolmosia sekä väkinäisiä step back -kolmosia, kun taas Suomessa 3p yritykset ovat hieman harkitumpia. Pitääkö fiilis paikkansa? Heitetäänkö NBA:ssa oikeasti useammin kaaren takaa kuin Korisliigassa, ja kuinka paljon eri joukkueiden välillä on vaihtelua? Jotta eri sarjoissa pelaavien joukkueiden vertailu onnistuu, niin tarkastellaan kuinka monta 3p heittoa (3PA, 3 Point Attempt) kukin joukkue ottaa per minuutti.2 Pylvästaulusta joukkueden heittotahtia on helppo vertailla.3

NBA joukkueet heittävät keskimäärin selvästi useammin 3p heittoja (0.78 3PA/min) kuin Korisliigajoukkueet (0.68 3PA/min). Kuitenkin molempien sarjojen joukkueiden välillä on suuria eroja ja joukkueiden sijoitukset menee osin lomittain. Boston Celtics on aivan omissa lukemissa (ensimmäisen kerran ikinä NBA:ssä joku joukkue yrittää 3p heittoa useammin kuin kerran minuutissa).4 Toisaalta Denver Nuggets, NBA:n maltillisin 3p heittojen ottaja, olisi 3p heittotempossa (0.67 3PA/min) Korisliigan keskikastia. Korisliiga joukkeista puolestaan KTP on koko lista 9. eniten heittävä (0.82 3PA/min), mutta Loimaalla tempo laahaa muiden perässä (0.55 3PA/min).

Heittotahti ei tietenkään kerro vielä mitään joukkueen tasosta. Boston, joka oli selvästi NBA:n innokkain kolmosten heittäjä, oli ennakkosuosikki mestariksi, mutta finaalissa pelaavat Indiana ja Oklahoma, jotka ovat keskitasoa 3p heittotahdissa. Korisliigassa sama juttu. Tempo kertoo kyllä paljon pelitavasta – menestyksestä ei niinkään.

- Käyttämäni data sisälsi runkosarjan, ylempi- /alempijatkosarja sekä pudotusottelut. Tämä lisää pleijareissa pitkälle edenneiden joukkueiden ottelumääriä, ja tuo siten lisää vaihtelua eri kausien välille. Hyvä myös huomata, että Korisliigassa pelataan melko vähän pelejä (vrt. NBA), joten otoskoon pienuuden takia vaihteluväli on myös suuri.
- Korisliiga data on taas koripalloliiton tilastopalveluista. NBA data on realGM sivustolta.
- 3PA/min laskemiseen käytin vain joukkueen 3p yritysten kokonaismäärän ja jaoin sen otteluiden määrällä ja sen 40 tai 48:lla riippuen sarjan peliajasta. Laskussa ei siis ole otettu huomioon, että osa peleistä on mennyt jatkoajalle. NBA tilastoina käytin taas vain runkosarjatilastoja, ja korisliigan kohdalla puolestaan kaikkia otteluita. Huomaa myös, että taulukon skaalan merkkasin alkamaan 0.5:stä.
- Bostonin 3PA/min on 1.005 jos lasketaan 3PA/(82*48) eli 3955/3936. Jos otetaan mukaan jatkoajatkin eli lasketaan 3PA / kaikki runkosarjan peliminuutit (3955/3964), niin Boston 3PA/min on “vain” 0.998.
