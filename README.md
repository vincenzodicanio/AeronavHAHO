# AERONAV HAHO — Release Point Planner & Tactical Navigator

Applicazione web progressiva (**PWA**) installabile su smartphone e pronta per la pubblicazione diretta su **GitHub Pages** o qualsiasi hosting statico HTTPS.

## Novità v9
* **Mappa satellitare**: nella scheda `IMPOSTAZIONI` del navigatore nuova sezione `MAPPA DI SFONDO` (Stradale OSM / Satellite Esri World Imagery). La scelta è salvata e applicata anche al Planner (che ha anche un selettore livelli sulla mappa). I tasselli satellitari richiedono connessione dati.
* **Quota lancio e quota apertura** separate nel Planner (al posto del campo unico "Apertura"). I vecchi dati salvati vengono migrati con lancio = apertura.
* **Deriva a paracadute chiuso**: il calcolo HARP ora include la caduta libera (lancio → apertura), con ratei di caduta libera impostabile (default 10.500 ft/min ≈ 53 m/s). Il corpo è trasportato solo dal vento; il tratto è mostrato tratteggiato in arancio.
* **Punto di apertura**: MGRS, deriva (distanza, direzione, tempo di caduta libera) e **pressione al suolo sulla verticale** riferita al QNH (atmosfera ISA, quota suolo da DEM). Il QNH si precompila da Open-Meteo (pressione al livello del mare) ma resta modificabile a mano. Il GPX include il waypoint `OPEN`.

## Novità v8
* **Scheda `IMPOSTAZIONI` nel navigatore**:
  * **Calibrazione Bussola**: quadrante bussola live, procedura guidata di calibrazione magnetometro a 8 (10 secondi), allineamento rapido a rilevamento DIP (`ALLINEA A ROTTA DIP`) e regolazione fine dell'offset / declinazione magnetica (`-180°` / `+180°`).
  * **Unità di Misura**: commutazione immediata tra **Piedi (`ft`) / Metri (`m`)** per quote e distanze, e **Nodi (`knots`) / Metri al secondo (`m/s`)** per velocità orizzontale e rateo di discesa, sincronizzata tra Navigatore e Planner.
