# Space Colonization Simulation

A console simulation of spacecraft travelling between planets whose days have different lengths.

Java

```
Gezegenler:
             --- X ---           --- Y ---           --- Z ---           --- V ---
Tarih:       3.1.2025            4.1.2025            3.1.2025            4.1.2025
Nüfus:       2                   0                   3                   2

Uzay Araçları:
Araç Adı   Durum      Çıkış      Varış      Hedefe Kalan Saat    Hedefe Varacağı Tarih
A1         Yolda      X          Y          194                  --
A2         Yolda      Y          Z          150                  --
A3         Bekliyor   Z          X          300                  --
B2         IMHA       X          V          --                   --
```

Planets, spacecraft and passengers are read from text files. Each planet keeps its own clock and calendar, so an hour passes differently on every one of them. Spacecraft leave on their departure date, count down the hours to their destination and record the date they arrive. Every passenger's remaining life goes down hour by hour; a spacecraft whose passengers have all died is destroyed. The table above is redrawn every hour until the simulation ends.

## Running it

The ready-built jar in `dist/` needs Java 21. It has to be run from inside `dist/`, next to the text files.

```bash
git clone https://github.com/omeraydin00/PDP---Uzay-Simulasyonu.git
cd PDP---Uzay-Simulasyonu/Proje/dist
java -jar proje.jar
```

To build it yourself with Java 17 or newer:

```bash
cd PDP---Uzay-Simulasyonu/Proje
javac -encoding UTF-8 -d out src/pdp/*.java
cd dist && java -cp ../out pdp.Simulasyon
```

The input files are `Gezegenler.txt` (planets), `Araclar.txt` (spacecraft) and `Kisiler.txt` (passengers).

Made for the Programming Language Principles course at Sakarya University.
