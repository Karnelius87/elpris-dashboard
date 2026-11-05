# Elpris-dashboard

En sida för en gammal Android-platta som visar elpriset per kvart för idag och imorgon, i SE4. Den visar också när det är billigast att köra tvätt, disk och tork, och vad det kostar.

- Priser: [elprisetjustnu.se](https://www.elprisetjustnu.se) (spotpris per kvart).
- Verkligt pris per kWh = spotpris × 1,25 (moms) + E.ON nätavgift 77,30 öre (inkl. energiskatt) + Tibber 11,9 öre.
- Ingen byggprocess. `index.html` är skriven i ES5 för att fungera i gamla webbläsare.

## Inställningar i adressen

| Parameter | Standard | Betydelse |
|---|---|---|
| `omrade` | `SE4` | Elområde SE1–SE4 |
| `nat` | `77.3` | Nätavgift öre/kWh inkl. moms |
| `skatt` | `0` | Energiskatt öre/kWh om den inte ingår i nätavgiften (2026: 45) |
| `paslag` | `11.9` | Elhandlarens påslag och avgifter öre/kWh inkl. moms |
| `andel` | `33` | Procent av totalkostnaden som visas som "ert pris" |
| `fast` | `0` | Fasta avgifter kr/månad, visas bara i foten |
| `natt` | `23-6` | Svart skärm mellan dessa timmar, `av` stänger av |
| `tempurl` | – | Adress till JSON `{"inne": 21.5}` för innetemperatur |

Exempel: `index.html?andel=100&natt=av`
