# Tanulószoba

Bíborka személyes tanulószobája — egyetlen, függőség nélküli HTML fájl.

## Négy rész

1. **Határidő napló** — a saját teendők, az iskolák és az ügyfelek határidői egy naptárban,
   **havi** és **heti** nézetben, visszaszámlálással. **Egy naptári napra kattintva kilistázza
   az aznapi összes teendőt** — ott pipálható, szerkeszthető, törölhető, és új is vehető fel.
   Itt van a **gyorsjegyzet** is.
2. **Iskolák** — több képzés párhuzamosan, saját színnel; tárgyanként tanár,
   elérhetőség, jegyek és átlag, ZH-k / beadandók, saját naptár és kézírásos jegyzetfüzet.
3. **Munka → Ügyfelek** — kapcsolat, teendők határidővel, szabad szöveges jegyzet.
4. **Journaling** — napi oldal gépelve **vagy kézzel írva** (iPad, Apple Pencil),
   halk hangulatjelöléssel, sorozatszámlálóval és a korábbi oldalak listájával.
   Kérdés csak akkor jelenik meg, ha kéred.

## Gyorsjegyzet

A határidő napló tetején egy mondatban le lehet írni a teendőt, és a helyére kerül:

**A dátumot ismeri fel, mást nem talál ki magától.** A megnevezés az marad, amit beírtál,
és típust vagy tárgyat csak akkor kap, ha te írtad oda.

| amit beírsz | ahova kerül |
|---|---|
| `bevásárlás ma` | saját teendő, mai dátummal |
| `fodrász jövő kedd` | saját teendő, jövő keddre |
| `római jog zh okt 3.` | Római jog I. → ZH, október 3. |
| `Zita: számla péntek` | Zita ügyfél → teendő, péntekre |
| `vegyél tejet` | dátum nélkül → gyorsjegyzetek közé |

Ért magyar dátumot hónapnévvel (`okt 3.`, `október 3-án`), számmal (`10.12`, `2026-10-20`),
relatívan (`ma`, `holnap`, `3 nap múlva`) és napnévvel (`pénteken`, `jövő kedd`).
Tárgyhoz vagy ügyfélhez csak akkor sorolja be, ha a nevét felismerhetően kiírtad —
egyébként sima saját teendő marad. A felismerés a böngészőben fut, beépített magyar
szabályokkal — nincs mögötte szerver, se API-kulcs.

## Jegyzetfüzet és kézírás

Kézírásos vászon tárgyanként és a naplóban is: toll, szövegkiemelő, radír, több oldal,
Apple Pencil nyomásérzékenységgel.

- **Írni csak tollal (Apple Pencil) vagy egérrel lehet** — az ujj soha nem hagy nyomot.
- **Két ujjal nagyítás** a lapon (100–500%), egy ujjal eltolás nagyított lapon,
  nem nagyított lapon pedig sima görgetés. Gombokkal is nagyítható.
- Kézírás **szöveggé alakítása**: a naplóban a *Gépelés* fülön iPadOS-en az Apple Pencillel
  közvetlenül a szövegmezőbe lehet írni, és a rendszer Scribble funkciója szöveggé alakítja.
  Az alkalmazás saját kézírás-felismerőt nem tartalmaz (ahhoz szerveroldali modell kellene).

Minden adat a böngésző `localStorage`-ában marad (kulcs: `biborka_hub_v1`) — szerver, fiók és feltöltés nincs.

## Használat

Nyisd meg az `index.html`-t böngészőben, vagy hosztold statikusan (pl. GitHub Pages).

PWA-ként telepíthető: a `manifest.webmanifest` és az ikonok mellette vannak, így
iPaden/iPhone-on a *Hozzáadás a kezdőképernyőhöz* után önálló appként indul, és menti az adatokat.

> Előnézetben (ahol a `localStorage` tiltott) a lap jelzi, hogy nem tud menteni.
