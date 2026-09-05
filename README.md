# Tanulószoba

Bíborka személyes tanulószobája — egyetlen, függőség nélküli HTML fájl.

## Mit tud

- **Iskolák / területek** — több képzés párhuzamosan, saját színnel.
- **Tárgyak** — tanár, elérhetőség, jegyek és átlag, ZH-k és beadandók.
- **Naptár** — havi nézet, iskolánként, a napra kattintva rögtön új esemény.
- **Határidők** — visszaszámlálás a kezdőlapon és a tárgykártyákon.
- **Ügyfelek** — kapcsolat, teendők határidővel, szabad szöveges jegyzet.
- **Jegyzetfüzet** — kézírásos vászon (toll, szövegkiemelő, radír, oldalak),
  Apple Pencil nyomásérzékenységgel; ha ceruzát érzékel, a tenyérérintést figyelmen kívül hagyja.

Minden adat a böngésző `localStorage`-ában marad (kulcs: `biborka_hub_v1`), szerver nincs.

## Használat

Nyisd meg az `index.html`-t böngészőben, vagy hosztold statikusan (pl. GitHub Pages).

PWA-ként telepíthető: a `manifest.webmanifest` és az ikonok mellette vannak, így
iPaden/iPhone-on a *Hozzáadás a kezdőképernyőhöz* után önálló appként indul, és menti az adatokat.

> Előnézetben (ahol a `localStorage` tiltott) a lap jelzi, hogy nem tud menteni.
