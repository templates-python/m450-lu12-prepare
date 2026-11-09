# M450 LU12.A01 - Testdaten erzeugen

Erstellen Sie eine Funktion, welche die Testdaten für ein SQL-Script
bereitstellt.

Wiki: <https://wiki.bzz.ch/modul/m450/learningunits/lu12/aufgaben/testdatencreate>

## Auftrag

Ergänzen Sie in `main.py` die vorbereitete Funktion `createTestdata` mit Code,
der zwei TXT-Dateien erzeugt:

- `clients.txt` mit 100 Klienten, die über eine eindeutige Kombination von Vor-
  und Nachnamen verfügen. Den Algorithmus dazu entwickeln Sie selber.
- `debits.txt` mit 10 Buchungen pro Klient, also insgesamt 1000 Buchungen. Der
  Betrag (Amount) wird zufällig aus Werten zwischen 10.00 und 99.90 generiert
  (2 Dezimalstellen).

Die Struktur der TXT-Dateien entnehmen Sie dem SQL-Script `LU12_A01_testdatadb`
aus Moodle. Passen Sie danach das SQL-Script so an, dass es die beiden Dateien
importiert, testen Sie es in der MySQL-Workbench und notieren Sie als
Vergleichswert die Summe aller Buchungen. Die Einzelheiten (u. a. die
Anpassung der `my.ini`) stehen im Wiki.

## Lokal testen

```bash
pip install -r requirements.txt
pytest
python _run_pylint.py
```

## Bewertung

| Teil | Punkte |
| --- | --- |
| Unittest `test` (`createTestdata` läuft ohne Fehler) | 1 |
| Linting von `main.py` | 5 |
| **Total** | **6** |

## Abgabe

Die Abgabe erfolgt durch den Push ins GitHub-Repository. Jeder Push wird
automatisch bewertet.
