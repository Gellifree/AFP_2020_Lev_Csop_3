## Funkcionális specifikáció

### Áttekintés
Egy olyan programot szeretnénk készíteni, ami megkönnyíti a hétköznapjait, azoknak az oktatóknak, akik *Bevezetés az informatikába* című tárgyat oktatják. Hogy megszüntessük a repetitív teszteket, amelyeket a diákok nagyobb erőfeszítés nélkül kijátszhatnak, változatos feladatgenerálás is a céljaink közé tartozik. Ezenkívül a gyakorlatok során, esetenként a vizsgaalkalom, vagy zárthelyi dolgozat során, az oktatónak előre kell készülnie a feladatsorokkal, vizsgán feltett gyakorlati kérdésekkel, és azok megoldásával. Ezt is segíti a program, hiszen egyszerű átváltásokat is képes lesz, részletesen lépésenként megjelenjteni a szoftver, ami gyorsítja ezeknek az előre elkészített feladatoknak a megtervezését. Ezen kívül, a rögtönzött feladatok megoldását is nagy mértékben gyorsíŧja, hiszen megadva az elvégezendő feladatot, annak eredményét, vagy igény szerint részeredményeit is azonnal megjeleníti, hiba arány nélkül. Így a táblánál elvégzett, levezetett feladatot, elég összehasonlítani a program álltal kijelzett eredménnyel, és azonnal észrevehetjük, ha a diák hibát vétett valahol, ami sok esetben idő, és energiaigényes feladat volna, manuálisan. Kifejezetten fontosnak tartjuk, hogy a felhasználói felületben gyorsan lehessen navigálni, arra alapozva, hogy a felhasználó alapvetően kiismeri magát, egy terminál alapú programban.

### Jelenlegi helyzet leírása
Jelenleg, amennyiben a gyakorlaton, egy diáknak elkell végeznie, akár egy egyszerű átváltást is, valamilyen számrendszerből, valamilyen számrendszerbe, annak az ellenőrzése, egy manuális folyamat. Attól eltekintve, hogy kiváló fejszámolási képességgel rendelkeznek az oktatók, bizonyos feladatok, és részfeladatok, igen komplikált mélységekbe is beleérhetnek, aminek kijavítása, esetleg hibakeresése, hosszas, időigényes feladat, ami az óra, értékes, másra fordítható időkeretéből vesz el. Előfordulhat olyan helyzet is, hogy a tárgyat oktató személy, nem rendelkezik elég idővel, hogy minden csoportnak, külön külön feladatsort készítsen el, változatos feladatokkal. Sok csoportnál, ez igen hosszas folyamat, és mégjobban meghoszabbítja, a dolgozatok kijavításához szükséges időt. Ez egy gyengepont a dolgozatok szempontjából, hiszen ha a diákok rendelkeznek egymás közötti kapcsolati hálóval, akkor könnyedén elvégezheti, egy kiváló tanuló a tesztet, ami aztán futótűzként terjedhet végig az illetékes diákokon. Akik immáron, ismerik a feladatok megoldásait, részeredményeit, és trükkjeit, ezálltal könnyedén megtörténhet, hogy a csalásra hajlamos hallgatók, így különösebb erőfeszítés nélkül megússzák a zárthelyi dolgozatot, jeles eredménnyel. Igen sok munka szüskéges a tárgyat oktató személytől, hogy ezeket a gyengepontokat kiküszöbölje, és ezzel a saját munkáját sokszorozza meg, a javítás során, amivel csökken a többi feladatára szánható értékes időkeret.

### Vágyálom rendszer
A cél, egy olyan szoftver elkészítése, ami ezeket a gyengepontokat megszüntetni, a folyamatokat felgyorsítja, és elsősorban tehermentesíti a tárgyat oktató személyt. Egy könnyen, és gyorsan navigálható menürendszer segítségével, azonnal elérhető minden funkció, kivételes sebességgel. Bizonyos szituációkban, igen nagy prioritással rendelkezik egy feladat megoldásának sebessége, ezért sem rendelkezünk grafikus felülettel. Habár a mostani hardverek több mint képesek, kiméletlenül gyorsan megjeleníteni egyszerű grafikus felületeket, azonban egy terminálablak elindítása, és egy parancs begépelését, mindenekelőtt gyorsabbnak, és hatékonyabbnak gondoljuk. Főleg olyan felhasználók körében, akik Linux alapú operációs rendszerrel rendelkeznek, hiszen a legtöbb ilyen felhasználó nem idegenkedik egy terminálablaktól, legtöbb munkafolyamatát itt végzi, ezért ismerős a környezet számára. Szerencsére, jelenlegi helyzetünkben, a legtöbb oktató Linux alapú operációs rendszereket használ, így ideális megoldásnak tartjuk a grafikus felület hiányát. A feladatsorok legenerálására, egy olyan algoritmust szeretnénk, amely hasonló koncepció alapján készíŧi a feladatokat, ugyan abban a nehézségi szintben, azonban a feladatok alapértékei mások, így nem megoldható a megoldások továbbadása. Akik alapvetően a koncepciókkal tisztában vannak, azoknak a feladatok nem különböznek egymástól, így nem is érzékelnek mérhető különbséget. Ezenkívül kiváló lehetőséget nyújt ez a megoldás, egy próba zárthelyi dolgozat megírására is, a gyakorlaton résztvevő hallgatók között, akik látni fogják ugyan a dolgozat vázát, és koncepcióját, ugyanakkor a konkrét megoldások csak segítenek nekik a tanulás elmélyítésében. A feladatsor legenerálása során, generálunk egy megoldásokat tartalmazó fájlt is, amivel a javítás során, csak összekell hasonlítani a dolgozatokat. Ezzel töredékére csökkentve, a feladatok elkészítéséhez szükséges időt, és azok javításához szükséges befektetett energiát.

### Követelménylista
| Modul | ID | Név | Kifejtés |
| --- | --- | --- | --- |
| Funkció | K1 | Átváltás 10-ből | A felhasználó képes legyen bármilyen alapú számrendszerbe átváltani tizes alapú számrendszerből, egész, és tizedes értékeket egyaránt, és lehessen választani, a rsézeredmények megjelenítése, és csak a végeredmény megjelenítése között. |
| Funkció | K2 | Átváltás 10-be | A felhasználó, bármilyen alapú számrendszerből, képes legyen tizes alapú számrendszerbe átváltani, egész, és tizedes értékekkel egyaránt, és szintén lehessen választani, hogy a részeredményeket megkívánjuk-e tekinteni, vagy csak a végeredményre vagyunk kiváncsiak. |
| Funkció | K3 | Feladat generálás | A program rendelkezzen olyan funkcióval, ami képes X számú feladatot generálni, mindig hasonló tematikában, csupán változó értékekkel, hasonló nehézségi szinten. |
| Funkció | K4 | Ellenőrzés | Egy adott legenerált feladatsort, mentsen le, és ehhez készítse el, a részletes megoldási információkat is, egy külön fájl-ban, hogy azt majd a megírt tesztekkel, elég legyen csak összehasonlítani. |
| Megjelenés | K5 | Átlátható felület | A terminálablakban tisztán, és egyértelműen jelenleg meg a program, könnyedén navigálható menürendszerrel. Rendelkezzen egy segítő dokumentummal, ami leírja a program működését, és funkcióit, ez a dokumentum legyen elérhető a programon belülről, és a programnak paraméterként átadott --help jelzővel. |
| Megjelenés | K6 | Dinamikus megjelenítés | Amennyiben Linux alapú rendszeren fut a program, így kifejezetten könnyedén kérhetjük le a terminálablak fizikai paramétereit, és változtathatunk a színeken. Ezzel készítsünk el, egy olyan megjelenítési formát, ami vonzó a felhasználónak, és igény esetén, a emgjelenítés alkalmazkodik a terminál méretéhez. (A program nevét a terminál közepére igazítja stb) |

### Használati esetek

### Használati esetek - követelmény megfeleltetés

### "Képernyő" tervek

Mivel egy terminálablakban futó alkalmazásról van szó, ezért a képernyőtervek, nem annyira beszédesek, azonban megpróbáljuk a lehető legjobban átadni a program funkcionalitását, és felépítését.

Amikor elindítjuk a programot, a következő menü fogadna bennünket: 

```
2020                                Számrendszer átváltó és feladatgeneráló

    [0] Átváltás tizes számrendszerből
    [1] Átváltás tizes számrendszerbe
    [2] Feladatsor generálása
    [3] Tárolt feladatsorok megtekintése
    [3] Segítség
    [Q] Kilépés

  >> _
```
Itt megadhatjuk a menüpontot reprezentáló számot, a '>>' jel után, ami enter leütésénél, kiválasztja az adott opciót. A program a 'Q' karakter leütésénél, megkérdezi, hogy biztosan ki szeretnénk-e lépni:

```
2020                                Számrendszer átváltó és feladatgeneráló

    [0] Átváltás tizes számrendszerből
    [1] Átváltás tizes számrendszerbe
    [2] Feladatsor generálása
    [3] Tárolt feladatsorok megtekintése
    [3] Segítség
    [Q] Kilépés

  >> Q

 Biztos vagy benne hogy kiszeretnél lépni? [I/n]
 >> _
```
### Funkció - követelmény megfeleltetés