# Krypto-Intelligenz-Aufdeckungs-Projekt

> Ein systematisches Framework zur vollständigen Aufdeckung komplexer kryptografischer, numerischer und struktureller Rätsel auf Geheimdienst-Niveau — in Texten, Medien, Infrastruktur, Code und überall sonst, wo Informationen verschlüsselt, kodiert oder verborgen sein können.

---

## Übersicht

Dieses Projekt stellt Methodik, Werkzeuge und Verzeichnisstruktur bereit, um komplexe kryptografische und numerische Rätsel aller Art vollständig zu lösen. Der Ansatz ist nicht linear, sondern iterativ-rekursiv: Jeder Fund kann neue Suchrichtungen eröffnen. Der Agent arbeitet wie eine **NSA/CIA-Kryptologie-Spezialeinheit** — **mehrfach-reasoning, multidimensional-analytisch, experimentell-forensisch, tief-verifizierend**.

---

## Verzeichnisstruktur

```
krypto_raetsel/
│
├── AGENTS.md                        ← Verhaltens- und Methodikregeln für den Agenten (NSA/CIA-Protokoll)
├── README.md                        ← Diese Datei
├── TEMPLATE/                        ← Vorlage für neue Rätsel-Verzeichnisse
│
├── raetsel_<id>_<kurzname>/         ← Ein Verzeichnis pro Rätsel
│   ├── README.md                    ← Rätsel-Beschreibung, Scope, Status, Lösung
│   ├── scope.md                     ← Definierter Untersuchungsbereich
│   ├── findings.md                  ← Alle bestätigten Funde
│   ├── hypotheses.md                ← Alle Hypothesen (offen / bestätigt / verworfen)
│   ├── timeline.md                  ← Chronologischer Untersuchungsverlauf
│   ├── tools_used.md                ← Eingesetzte Tools mit Parametern
│   │
│   ├── reasoning/                   ← Interne forensische Analyseprotokolle
│   │   ├── phase1_surface_analysis.md
│   │   ├── phase2_structure_analysis.md
│   │   ├── phase3_crypto_analysis.md
│   │   ├── phase4_steganography.md
│   │   ├── phase5_network_intel.md
│   │   ├── phase6_semantic_intel.md
│   │   └── phase7_cross_reference.md
│   │
│   ├── sources/                     ← Archivierte Rohdaten
│   │   ├── web/                     ← HTML-Snapshots, HTTP-Header-Dumps
│   │   ├── images/                  ← Heruntergeladene Originaldateien
│   │   ├── audio_video/             ← Mediendateien
│   │   ├── network/                 ← WHOIS/RIPE/DNS-Dumps
│   │   └── extracted/               ← Aus Quellen extrahierte Rohdaten
│   │
│   ├── analysis/                    ← Forensische Analyseergebnisse und Zwischenprodukte
│   │   ├── crypto/                  ← Kryptografie-Analysen und Decodierungen
│   │   ├── stego/                   ← Steganografie-Analysen
│   │   ├── network/                 ← Netzwerk-Intelligence-Analysen
│   │   ├── code/                    ├── Skripte und Auswertungen
│   │   └── fragments/               ← Identifizierte Teilinformationen/-segmente
│   │
│   └── REPORT_<id>.md               ← Abschlussbericht (nach Lösung)
│
├── raetsel_<id>_<kurzname>/         ← Weiteres Rätsel
│   └── ...
│
└── shared/                          ← Gemeinsam genutzte Ressourcen (Geheimdienst-Tools)
    ├── tools/                       ← Forensische Hilfsskripte und Spezial-Tools
    │   ├── lsb_extract.py
    │   ├── exif_dump.sh
    │   ├── ripe_query.py
    │   ├── decode_all.py
    │   ├── crypto_analyzer.py
    │   ├── network_intel.py
    │   └── forensic_suite.py
    ├── wordlists/                   ← Referenzlisten für Musterabgleich
    └── notes.md                     ← Projektübergreifende Erkenntnisse
```

---

## Rätsel anlegen

### Schritt 1: Verzeichnis erstellen

Benennungskonvention: `raetsel_<zweistellige-id>_<beschreibender-kurzname>`

Beispiele:
```
raetsel_01_webseite_xy
raetsel_02_musikalbum_zzz
raetsel_03_social_media_kampagne
```

### Schritt 2: TEMPLATE kopieren

```bash
cp -r TEMPLATE/ raetsel_<id>_<kurzname>/
```

### Schritt 3: scope.md ausfüllen

```markdown
# Scope — Rätsel <ID>

## Vom Benutzer vorgegebener Bereich
- [ ] Domain-beschränkt: `example.com` (inkl. alle Subdomains)
- [ ] Plattform-beschränkt: z.B. nur Twitter/X, nur Spotify
- [ ] Internet-weit: Keine Einschränkung, Quellen folgen Hinweisen

## Startpunkte
- URL / Plattform / Datei: ...

## Explizit ausgeschlossen
- ...

## Scope-Erweiterungen (chronologisch)
| Datum | Neue Quelle | Begründung |
|-------|-------------|------------|
| ...   | ...         | ...        |
```

### Schritt 4: Untersuchung starten

Dem Agenten wird die `README.md` und `scope.md` des Rätsel-Verzeichnisses übergeben. Der Agent folgt `AGENTS.md` vollständig.

---

## Rätsel-README-Vorlage

Jedes `raetsel_<id>/README.md` folgt diesem Schema:

```markdown
# Rätsel <ID> — <Kurzname>

## Beschreibung
<Vom Benutzer vorgegebene Beschreibung des Rätsels>

## Scope
Siehe scope.md

## Aktueller Status
- [ ] Phase 1: Oberflächenanalyse
- [ ] Phase 2: Strukturanalyse
- [ ] Phase 3: Kodierungsanalyse
- [ ] Phase 4: Steganografie
- [ ] Phase 5: Netzwerkebene
- [ ] Phase 6: Semantische Ebene
- [ ] Phase 7: Kombinatorik & Cross-Referenz
- [ ] Validierung
- [ ] Abgeschlossen

## Bekannte Fragmente
| Fragment | Wert | Quelle | Methode | Vertrauen |
|----------|------|--------|---------|-----------|
| F-01     | ...  | ...    | ...     | hoch      |

## Lösungskandidat
> Noch nicht final — wird nach vollständiger Validierung eingetragen

## Lösung (final)
> Wird nach Abschluss eingetragen

## Lösungskette
> Schritt-für-Schritt-Begründung, wie die Lösung aus den Fragmenten folgt
```

---

## Versteck-Dimensionen (Übersicht)

Die folgende Tabelle zeigt, wo Zahlen versteckt sein können. Details und Checkliste: siehe `AGENTS.md`, Abschnitt 4.

| Dimension | Beispiele |
|-----------|-----------|
| **Web / Quellcode** | HTML-Kommentare, CSS-Werte, JS-Variablen, HTTP-Header, URL-Struktur |
| **Bilder** | EXIF-Daten, LSB-Steganografie, Farbwerte, Abmessungen, Dateinamen |
| **Audio / Video** | Spektrogramm, BPM, Timecodes, Stille-Intervalle |
| **Netzwerk** | RIPE-Datenbank, WHOIS, DNS TXT-Records, TTL, IP-Oktette, SSL-Seriennummern |
| **Texte** | Akrostichon, Nth-Buchstabe, unsichtbare Unicode-Zeichen, ausgeschriebene Zahlen |
| **Social Media** | Follower-Zahlen, Like-Counts, Post-IDs, Zeitstempel |
| **Musik / Kultur** | Tracknummern, Lauflängen, Katalognummern, Chartplatzierungen |
| **Strukturell** | Anzahl von Elementen, verteilte Fragmente, mathematisch verknüpfte Teilwerte |

---

## Krypto-Referenz (Geheimdienst-Niveau)

Häufig verwendete Kodierungen und Verschlüsselungen, die der Agent prüft:

| Kodierung | Erkennungsmerkmal | Dekodierung/Analyse |
|-----------|-------------------|------------------|
| Base64 | Endet oft mit `=`, Zeichen `A-Za-z0-9+/` | `base64 -d`, CyberChef |
| Hex | Nur `0-9A-Fa-f`, oft Länge durch 2 teilbar | `xxd -r -p`, Python |
| ROT13 | Lesbarer Text, aber verschoben | `tr A-Za-z N-ZA-Mn-za-m` |
| Caesar | Wie ROT13 aber variabler Shift | Brute-Force über 25 Shifts |
| Morse | Punkte, Striche, Leerzeichen | Morse-Decoder, CyberChef |
| ASCII | Dezimalzahlen 32–126 | `python: chr(n)` |
| Unicode-CP | Dezimal oder U+XXXX | `chr()` / Zeichentabelle |
| LSB-Stego | Nicht sichtbar, in Binärdaten | `zsteg`, `stegsolve`, `steghide` |
| Akrostichon | Erste Buchstaben ergeben Wort/Zahl | Manuelle Extraktion |
| Zero-Width | Unsichtbar im Text | `cat -A`, Hex-Editor, Unicode-Analyse |
| **Advanced Crypto** | | |
| AES/RSA | Kryptografische Blöcke, Padding | `openssl`, `python cryptography` |
| Vigenère | Polyalphabetische Verschlüsselung | Kasiski-Analyse, Frequenzanalyse |
| One-Time-Pad | Zufällige Schlüssel gleicher Länge | Known-Plaintext-Angriffe |
| Steganografie | Bild/Audio/Video-Kanäle | `stegsolve`, `audacity`, spectral analysis |
| Watermarking | Digitale Wasserzeichen | `steghide`, `stegbreak` |
| QR/Barcodes | 2D/1D-Codes in Medien | `zbar`, `dmtx`, QR-Scanner |
| Hashes | MD5, SHA1, SHA256 etc. | Hash-Analyse, Rainbow-Tables |

---

## Qualitätsstandards

- Kein Rätsel gilt als gelöst, solange nicht alle 7 Phasen abgeschlossen und dokumentiert sind
- Jeder Fund braucht eine Quelle, eine Methode und eine Verifikation
- Verworfene Hypothesen bleiben im System — sie verhindern Doppelarbeit
- Der Abschlussbericht muss für einen Dritten ohne Vorwissen nachvollziehbar sein

---

## Schnellstart

```bash
# 1. Neues Rätsel anlegen
cp -r TEMPLATE/ raetsel_01_mein_raetsel/
cd raetsel_01_mein_raetsel/

# 2. Scope definieren
nano scope.md

# 3. Agenten starten
# → AGENTS.md und scope.md übergeben
# → Agent beginnt mit Phase 1 und dokumentiert alles unter reasoning/

# 4. Fortschritt verfolgen
cat findings.md
cat hypotheses.md
```

---

## Projektstatus

| Rätsel-ID | Kurzname | Status | Lösung |
|-----------|----------|--------|--------|
| 01 | haian.de | Abgeschlossen | Kein Rätsel gefunden (legitime Trauerseite) |

*Diese Tabelle wird mit jedem neuen Rätsel aktualisiert.*
