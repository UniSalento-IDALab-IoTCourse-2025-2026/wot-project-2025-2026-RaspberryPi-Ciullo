# wot-project-2025-2026-ESP32-Ciullo

# SMARTCARE — Sistema Intelligente EDGE per Monitoraggio Scompenso Cardiaco

## Descrizione del progetto
SMARTCARE è un sistema intelligente EDGE per la raccolta di parametri biomedici 
e il rilevamento di anomalie in pazienti affetti da scompenso cardiaco.
Il sistema monitora in tempo reale parametri fisiologici (battito cardiaco, 
saturazione ossigeno, temperatura corporea, postura e movimento), rileva 
situazioni anomale tramite tecniche di intelligenza artificiale eseguite 
direttamente sul dispositivo edge (smartphone), e notifica automaticamente 
il medico curante e il hub del pronto soccorso in caso di eventi critici.

## Architettura del sistema
Il sistema è composto da 6 componenti principali:
1. **Sensori wearable + ESP32** — acquisizione parametri biomedici via BLE
2. **App smartphone (edge node)** — elaborazione locale, anomaly detection, GPS
3. **AI Engine** — Isolation Forest + soglie adattive per anomaly detection
4. **Backend** — broker MQTT Mosquitto, MongoDB, REST API, alert engine
5. **Dashboard medico** — web app React.js per monitoraggio realtime
6. **Hub pronto soccorso** — integrazione webhook per dispatch ambulanza
