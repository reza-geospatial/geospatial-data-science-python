# Data sources and licences

All datasets here are open data. Keep this file with the data and reproduce the
attribution in any video, slide or publication that uses them.

## 1. accidents_berlin_2018.geojson — 13,652 points

Road accidents in Berlin, 2018, from the **Unfallatlas** of the Statistical
Offices of the Federation and the States (Statistische Ämter des Bundes und der
Länder). Prepared extract with accidents matched to street segments:
https://github.com/tagesspiegel/Unfallatlas-Berlin-2018
Original source: https://unfallatlas.statistikportal.de/

**Licence: Datenlizenz Deutschland – Namensnennung – Version 2.0 (dl-de/by-2-0)**
https://www.govdata.de/dl-de/by-2-0

Attribution line to show on screen or in a caption:

> Unfallatlas 2018, Statistische Ämter des Bundes und der Länder, dl-de/by-2-0

| Column | Meaning |
|---|---|
| `UMONAT` | month (1–12) |
| `USTUNDE` | hour of day (0–23) |
| `UKATEGORIE` | severity: 1 = fatal, 2 = serious injury, 3 = slight injury |
| `ULICHTVERH` | light (0 = daylight, 1 = twilight, 2 = darkness) |
| `STRZUSTAND` | road surface (0 = dry, 1 = wet, 2 = snow/ice) |
| `IstRad` … `IstSonstig` | participant types (0/1) |
| `bezirk`, `oteil` | district and neighbourhood |
| `dn_id` | street segment id |

Note: this extract does **not** contain `UWOCHENTAG` (weekday). The full
national Unfallatlas does.

## 2. street_segments_berlin_2018.geojson — 7,413 lines

Berlin street segments ("Detailnetz", Berlin Senate) with accident counts per
segment. Same repository and licence as above.

## 3. berlin_ortsteile.geojson — 97 polygons

ALKIS Berlin Ortsteile (neighbourhoods), Berlin Open Data.
Via https://github.com/codeforgermany/click_that_hood
Source: http://daten.berlin.de/datensaetze/alkis-berlin-ortsteil-wfs

## 4. berlin_bezirke.geojson — 12 polygons

Berlin districts. Via https://github.com/m-hoerz/berlin-shapes

## Coordinate reference systems

All files are delivered in EPSG:4326. Every notebook projects to
**EPSG:25833 (ETRS89 / UTM 33N)** before measuring anything, because Berlin sits
in UTM zone 33 and that CRS has the metre as its unit.
