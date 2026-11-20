# HK Unicorn Squad – õpikeskkond (demo)

Ühefaililine veebirakendus (`unicorn-squad.html`) HK Unicorn Squadi tehnoloogiaringide jaoks: tüdrukutele vanuses 8–14. Keskkonnas on kolm rolli: **administraator**, **juhendaja** ja **õpilane**. Iga roll näeb oma vaadet: kursused ja tunnid, grupid, tööde esitamine ja tagasiside, märgid, tunnistus, kastide logistika ja suvelaager.

> **NB! See on prototüüp.** Serverit ega andmebaasi ei ole. Kõik andmed on brauseri mälus ja **kaovad lehe uuesti laadimisel**. E-kirju ei saadeta.

---

## Käivitamine

1. Ava fail `unicorn-squad.html` brauseris (topeltklõps või lohista brauseri aknasse).
2. Internetiühendust ega paigaldamist ei ole vaja: fondid ja esilehe pilt on failis sees (base64).
3. Vali esilehel roll, sisesta kood ja vajuta **Sisene**.

### Demokoodid

| Roll | Kood |
|---|---|
| Administraator | `UNI-ADM` |
| Juhendaja | `UNI-JUH` (sisened alati kui *Marika*) |
| Õpilased | `UNI-ITI1` (Iti), `UNI-MIA2` (Mia), `UNI-LAU3` (Laura), `UNI-KAI4` (Kaisa), `UNI-LII5` (Liisa) |

Koodi suurtähed ja väiketähed ei loe. Koodid on ka esilehel kirjas.

---

## Võimalused rollide kaupa

### Administraator (`Haldus`)

- **Ülevaade:** arvud (juhendajad, grupid, õpilased, tunnid, jagatud märgid, õpiväljunditeta tunnid). Juhendaja konto loomine. Juhendaja ligipääsu peatamine ja tagasiandmine. Laagrijuhi õiguse andmine.
- **Tunnid ja õpiväljundid:** kursuste ja Pro moodulite haldus (tutvustus, eesmärgid). Uue tunni lisamine. Tunni muutmine: nimi, eesmärk, programm, õpiväljundid, sammud, kursus, tüüp, kestus, kategooria, videolink, ohutusmärkus, lisaülesanne, kasti sisu ja lisaks vajalik.
- **Rotatsioon:** tunni määramine juhendajale või koolile kuupäevaga. Staatus *plaanis / toimunud / ära jäänud*. Samast vaatest saab kohe luua paki.
- **Logistika:** pakkide (tunnikastide) jälgimine. Staatus *ootel / postitatud / kohal / tagastatud*, kuupäevad, kuhu edasi saata, Omniva kood.
- **Juhendajate ülesanded:** linnukestega kontrollnimekirjad kõigile või ühele juhendajale. Edenemine on näha juhendaja kaupa.
- **Märgid:** märkide kataloog ja märgi andmine õpilasele.
- **Laager:** üldinfo, päevakava, registreerimised ja vanema nõusolekud.
- **Postkast:** juhendajate kirjad korraldajale, loetuks märkimine.

### Juhendaja

- **Ülevaade:** järgmine tund rotatsioonist ja teel olevad pakid. Teate saatmine grupile koos aegumiskuupäevaga.
- **Grupid:** grupi loomine, õpilaste valimine (õpilane saab olla ainult ühes grupis), uue õpilase lisamine koos automaatse sisenemiskoodiga. Edenemine, fotoloa olek, kinnitamist ootavad tööd, grupiülesanded.
- **Õpilase leht:** läbitud tundide märkimine, tööde kinnitamine või tagasilükkamine, isiklik tagasiside, märkide andmine ja eemaldamine, omandatud oskused, privaatne märkus.
- **Tunnistus:** antakse välja, kui õpilane on läbinud vähemalt **80%** tundidest. Prinditav A4-le või salvestatav PDF-ina.
- **Tunnid:** tunniplaan ja tunni ettevalmistus: ohutusmärkus, videojuhis, „Kastis on“, „Lisaks on vaja“, kasti tagastamise kontrollnimekiri, märge „ettevalmistatud“. Lisaks esitatud tööd grupi kaupa.
- **Logistika:** oma pakid, ülesannete linnukesed, kiri korraldajale.
- **Foorum:** üldteema või tunnipõhine arutelu koos vastustega.
- **Laager:** päevakava ja ruumide jaotus. Laagrijuht näeb ka registreerimisi ja saab ruume lisada.
- **Abi:** lühijuhend juhendajale.

### Õpilane

- **Minu kursus:** teated, grupi tunniplaan, ülesanded, tundide otsing ja lemmikud (★).
- **Tunni leht:** õpiväljundid, sammud, mida saab tehtuks märkida (edenemisriba), lisaülesanne. Töö lisamine koos pildi ja kolme enesetagasiside küsimusega. Pilt vähendatakse brauseris kuni 1000 px laiuseks.
- **Grupi tööd:** kaaslaste kinnitatud tööd, südamed ja kommentaarid lausealgusega („Mulle meeldis…“). Kui kaaslasel pole fotoluba, siis tema pilti ei näidata.
- **Minu mapp:** edenemine, omandatud oskused, saadud ja saamata märgid, oma tööd ja juhendaja tagasiside.
- **Laager:** päevakava, oma rühm ja ruum, prinditav kaelapilet.
- **Abi:** lühijuhend õpilasele.

Külgribal on kõigil (peale administraatori) kursuste menüü (1.–6. kursus ja Pro moodulid 1–4).

---

## Sisu

Demoandmetes on **2. kursuse 9 tundi**, igaühel kasti sisu, sammud ja õpiväljundid:

1. Elekter. Hollandi kuningas
2. Füüsika. Õhukahur
3. Robootika. Suur võidusõit (WeDo)
4. Füüsika ja elektroonika. Ventilaator
5. Programmeerimine. Kerarobotid (Sphero BOLT)
6. Programmeerimine. Dubai droonitakso (Tello EDU)
7. Lennukid
8. Playtronica
9. Greenscreen (Veescope Live)

Kategooriad: Elekter/elektroonika, Füüsika, Droonid/robootika/programmeerimine, Keskkond, Audio/visual.

---

## Tehniline ülesehitus

- **Üks fail**, ilma raamistiketa: HTML, CSS ja puhas JavaScript.
- **Kujundus:** CSS-muutujad (`--p`, `--pd`, `--pl`, `--t`, `--k` jne) plokis `:root`. Tume režiim lülitub automaatselt (`prefers-color-scheme`). Mobiilisõbralik (iPhone'i *safe area* arvestatud).
- **Font:** *Lil Grotesk* (400 ja 700), base64-na failis sees (read 10–11).
- **Esilehe pilt:** konstant `HERO` (base64 JPEG, rida 59).
- **Andmed:** objekt `D` (read 67–97):

| Võti | Sisu |
|---|---|
| `ins` | juhendajad |
| `B` | märgid |
| `L` | tunnid |
| `S` | õpilased (kood, fotoluba, läbitud tunnid, märgid, lemmikud) |
| `G` | grupid |
| `GT` | grupiülesanded |
| `BX` | pakid / logistika |
| `T` | juhendajate ülesanded |
| `M` | postkast |
| `P` | foorumi postitused |
| `C` | kursused ja Pro moodulid |
| `R` | rotatsioon / tunniplaan |
| `CAMP` | laager (päevakava, ruumid, registreerimised) |
| `N` | teated |
| `W` | õpilaste tööd (luuakse käivitusel läbitud tundide põhjal) |

- **Olek:** objekt `S` (kasutaja, aktiivne sakk, avatud tund jne). Iga muudatus kutsub välja `render()`, mis joonistab vaate `#app` sisse uuesti.
- **Põhifunktsioonid:** `home()` esileht, `adm()` administraator, `ins()` juhendaja, `stu()` õpilane, `lesson()` tunni leht, `stuPage()` õpilase leht juhendajale, `cert()` tunnistus.
- **Turvalisus:** kasutaja sisestatud tekst läbib enne kuvamist funktsiooni `esc()` (HTML-i escape).
- **Printimine:** `@media print` näitab ainult elementi `#cert` (tunnistus või kaelapilet).

---

## Kohandamine

- **Logo:** asenda faili alguses olev kohatäite-SVG (`<symbol id="lm">`) päris Unicorn Squadi logoga (koht on märgitud kommentaariga).
- **Värvid:** muuda CSS-muutujaid `:root` plokis.
- **Juhendaja nimi:** konstant `const ME='Marika'`. Praegu siseneb iga juhendaja selle nimega.
- **Tunnid ja kursused:** muuda massiive `D.L` ja `D.C` või lisa tunde administraatori vaates (muudatused ei salvestu).
- **Tunnistuse lävend:** funktsioon `elig` (`pct(s)>=80`).

---

## Teadaolevad piirangud (enne päris kasutust)

- **Andmed ei salvestu:** värskendamine taastab demoandmed. Päris kasutuseks on vaja serverit/andmebaasi (või vähemalt `localStorage`'it).
- **Sisselogimine on näidis:** koodid on lähtekoodis ja esilehel nähtavad. Kõigil juhendajatel on üks kood. Juhendajakonto „ajutist parooli“ ei salvestata ega kasutata.
- **E-kirju, Omniva teavitusi ja registreerimiskinnitusi ei saadeta:** need on ainult teated ekraanil.
- **Isikuandmed:** päris laste nimede, fotode ja vanemate nõusolekute hoidmiseks on vaja turvalist taristut ja andmekaitse (GDPR) lahendust.
- **Videojuhiste lingid** on tundides veel tühjad.
- **Fondi litsents:** enne avalikku kasutust kontrolli, et *Lil Grotesk*'i võib veebis manustatuna kasutada.

---

## Kontakt

Unicorn Squadi info: <https://unicornsquad.ee>ärgi kohandada.
