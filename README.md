# Earthquake_Newsfeed
Data Wrangling (API; Json)

Dieses Projekt bietet einen automatisierten Newsfeed für aktuelle Erdbebeninformationen, der kontinuierlich aktualisiert wird und die Erdbeben der letzten 24 Stunden anzeigt. Das System greift auf die globalen Erdbebendaten des US Geological Survey (USGS) zu und nutzt deren JSON API, um relevante Informationen über Erdbeben in verschiedenen Zeitintervallen (Stunde, Tag, Woche, Monat) zu sammeln.

## Hauptfunktionen:

### Datenimport:
Die Erdbebendaten werden automatisch von der USGS API heruntergeladen und in eine geeignete Datenstruktur eingelesen.

## Datenaufbereitung:
Die hierarchische JSON-Datenstruktur wird in ein flaches DataFrame umgewandelt.
Nicht notwendige und unvollständige Spalten werden entfernt. Zeitstempel werden in lesbare Datumsformate konvertiert.
Koordinaten (Breiten- und Längengrad) sowie die Tiefe des Erdbebens werden extrahiert und geprüft.

### Explorative Datenanalyse:
Es werden Visualisierungen erstellt, um die Verteilung der Erdbebenstärken (Magnituden) und der Epizentren-Tiefen zu analysieren.
Eine Prüfung auf mögliche Tsunami-Warnungen wird durchgeführt.
Erdbeben werden auf einer Weltkarte visualisiert, wobei Magnitude und Position hervorgehoben werden.

<div style="display: flex; gap: 20px;">
  <img src="https://github.com/user-attachments/assets/8059b304-0616-4bf7-ae5c-4ec0598623d2" alt="image" width="450"/>
  <img src="https://github.com/user-attachments/assets/2fd16d4d-9f40-4a35-9a6e-e73d6515843f" alt="image" width="450"/>
  <img src="https://github.com/user-attachments/assets/fc880a7b-b061-46df-92f1-0a912efeb901" alt="image" width="800"/>
</div>


### Pipeline:
Eine effiziente Pipeline wurde entwickelt, die automatisch Daten herunterlädt, verarbeitet und in das gewünschte Format überführt. Die Pipeline kann flexibel mit verschiedenen URLs (z. B. Erdbeben der letzten Woche oder des letzten Monats) verwendet werden.

### Verwendete Technologien:
R Packages: tidyverse, geojsonio, sf, jsonlite, leaflet, ggplot2, dplyr, purrr, lubridate
Datenquelle: US Geological Survey (USGS) Earthquake API GeoJSON Feed
