## **Dodavanje LMG poligona u Stellarium**

Počevši od verzije Stellarium-a 0.16.1 (2016. godina), prisutna je opcija sazvežđa i asterizama kao dva odvojena layer-a za prikaz. Za LMG poligone u Stellariumu iskoristili smo tu opciju i ubacili ih kao layer asterizama kako bi istovremeno bila vidljiva i sazvežđa i poligoni.

Da bi ste ih ubacili u Stellarium, potrebno je da preuzmete arhivu **stellarium-poligoni-master.zip** pritiskom na zeleno dugme **Clone or download** -> **Download ZIP** i nakon preuzimanja, fajlove iz arhive raspakujete u instalacioni direktorijum Stellarium-a na lokaciji:  


**Windows** ->  **`C:\Program Files\Stellarium\skycultures\poligoni`**

**Linux** ->  **`/usr/share/stellarium/skycultures/poligoni`** <sup>1</sup>

![Izgled instalacionog direktorijuma sa poligonima na Windows-u](/poligoni/uputstvo/slika1.png)

**Slika** **1** Izgled instalacionog direktorijuma sa poligonima na Windows-u

![Izgled instalacionog direktorijuma sa poligonima na Linux-u](/poligoni/uputstvo/slika2.png)


**Slika** **2** Izgled instalacionog direktorijuma sa poligonima na Linux-u

Nakon kopiranja foldera poligoni u Stellarium direktorijum, potrebno je sazvežđa prebaciti na LMG poligone (koji uključuju standardna sazvežđa i poligone kao asterizme).

U Stellariumu izabrati **Sky and viewing options window** -> **Starlore** i iz liste izabrati opciju **LMG poligoni.**

Zbog lakšeg pregleda, zgodno je odmah promeniti i boju linija asterizama, kod opcije **Show asterism lines**.




![Izgled menija Sky and viewing options, opcija Starlore sa selektovanim LMG poligonima](/poligoni/uputstvo/slika3.png)

**Slika** **3** Izgled menija **Sky and viewing options**, opcija **Starlore** sa selektovanim LMG poligonima



----------
1 *Prilikom dodavanja foldera u Linuxu u sistemski direktorijum nije moguć direktni copy/paste pa je najlakše folder poligoni raspakovati na Desktop i koristiti komandu za pomeranje **mv**  u terminalu:

**`sudo mv /home/vaš-username/Desktop/poligoni /usr/share/stellarium/skycultures/poligoni`**

  
  
## **Napredno – kako se menjaju fajlovi koji definišu asterizme i sazvežđa**

Skyculture opcija sastoji se iz dva layer-a – Constellation i Asterism. Fajlovi koji definišu jedan skyculture su:

- **asterism_lines.fab** – fajl u kome se definišu linije asterizama (definisano HIP oznakama zvezda i parovima koji definišu jednu       liniju)
- **asterism_names.eng.fab** – fajl u kome se definišu imena asterizama
- constellation_names.eng.fab
- constellationsart.fab
- constellationship.fab
- **description.en.utf8** – fajl sa opisom koji se vidi u Stellariumu u Starlore meniju
- **info.ini** – fajl koji definiše naziv skyculture-a
- **reference.fab** – fajl u kome su reference za dati skyculture
- **star_names.fab** – fajl u kome su nazivi zvezda i kroz koji su dodate magnitude graničnih zvezda u naziv 
- PNG slike sazvežđa

Boldovani i opisani su fajlovi koje je bilo potrebno izmeniti kako bi se dodali poligoni kao asterizmi. Na sličan način se menjaju i definicije sazvežđa.


| ![Definicije imena oblasti](/poligoni/uputstvo/slika41.PNG) | ![Definisanje linija koje ograničavaju poligon](/poligoni/uputstvo/slika42.PNG) | 
|--|--|
|  **Slika 4.1** Definicije imena oblasti | **Slika 4.2** Definisanje linija koje ograničavaju poligon |

Na slici 4 prikazani su fajlovi kojima su definisane oblasti. Na slici 4.2 prva kolona su nazivi promenljive datog asterizma. Druga kolona klasa objekta u Skyculture-u (1 – asterism). Treća kolona predstavlja broj zvezda koje definišu dati asterizam. Četvrta kolona su linije asterizma definisane preko HIP oznaka graničnih zvezda:

| O1 | 1 | 4 | 94376 89937 | 89937 83895 | 83895 87585 | 87585 94376 |
|--|--|--|--|--|--|--|
| ID oblasti | klasa | broj linija | 1. linija | 2. linija | 3.linija | 4.linija |
