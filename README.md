# AERONAV HAHO — Release Point Planner & Tactical Navigator

Applicazione web progressiva (**PWA**) installabile su smartphone e pronta per la pubblicazione diretta su **GitHub Pages** o qualsiasi hosting statico HTTPS.

## Struttura del Pacchetto
- `index.html`: **Pianificatore HAHO** — Calcola il punto di lancio (**HARP**) sopravvento rispetto al **DIP** per effettuare la navigazione a favore di vento (in coda) fino al bersaglio. Integra quota DEM automatica e profili vento reali da **Open-Meteo**, *Safety Factor* in migliaia di piedi, efficienza vela e rilevamento altitudine cartografica.
- `nav.html`: **Navigatore Tattico in Volo (stile Garmin GPSMAP 64st)** — Mappa a tutto schermo orientata con la bussola del telefono (`HDG UP` / `NORTH UP`), coordinate **MGRS / WGRS** ovunque, calcolo **Velocità Verticale Reale** e **Velocità Verticale a Destinazione** come sul Garmin 64st, distanza al suolo, velocità, direzione in gradi e **5 DIP alternativi** commutabili con un tocco.
- `mgrs-core.js`: Motore geodetico bidirezionale `WGS84 <-> MGRS/WGRS`, calcolo rotte/distanze, client DEM Open-Meteo e gestore aggiornamento automatico PWA.
- `manifest.json` & `sw.js`: Configurazione PWA installabile con strategia *Network-First* che forza l'aggiornamento ad ogni apertura dell'app.
- `icon-192.svg` & `icon-512.svg`: Icone vettoriali dell'applicazione.

## Pubblicazione su GitHub Pages
1. Carica tutti i file contenuti in questo archivio nella root del repository `AeronavHAHO`.
2. Vai su **Settings -> Pages** e seleziona il branch `main` (cartella `/ (root)`).
3. Apri l'URL HTTPS generato dal browser dello smartphone e seleziona **Installa app / Aggiungi a schermata Home**.
