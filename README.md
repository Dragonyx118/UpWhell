# ⚙️ UpWheel

![Status](https://img.shields.io/badge/Status-WIP-E74C3C?style=flat&logo=git&logoColor=white)
![Hardware](https://img.shields.io/badge/PCB-Custom-E7352C?style=flat&logo=kicad&logoColor=white)
![Firmware](https://img.shields.io/badge/Firmware-C%2FC%2B%2B-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Dragonyx118-181717?style=flat&logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-TBD-lightgrey?style=flat)

**Mobilità autonoma per tutti** — carrozzina intelligente open source, economica e controllabile da joystick, radiocomando e app.

Progetto scolastico realizzato per **Zero Barriere Crema**, con l'obiettivo di restituire autonomia di movimento a persone anziane o con difficoltà motorie, riducendo la dipendenza da un caregiver per gli spostamenti quotidiani.

> ⚠️ Prototipo dimostrativo in scala (modellino), non certificato per uso su persone.

## Team

- **Daniele Cerioli** — Elettronica e firmware (PCB, ESP32, sensori, motori, alimentazione)
- **Andrei Corduneanu** — Project Manager, sviluppo software (logica di controllo, comunicazione, integrazione)
- **Simone Panelli** — Sviluppo app (app smartphone, comandi vocali, interfaccia accessibile)

Docente tutor: Arcangelo Sorvillo · Cliente/partner: Zero Barriere Crema

## Caratteristiche

- Movimento tramite joystick fisico, radiocomando o app
- Sensore di distanza ToF (VL53L1X) per il rilevamento ostacoli
- Modulo GPS (NEO-6M) per il tracciamento posizione
- Monitoraggio batteria con indicatore LED e allarme sonoro
- Arresto di emergenza fisico e da app
- App con stato carrozzina (batteria, GPS) e comandi vocali
- Fail-safe: arresto motori in caso di perdita del segnale
- PCB personalizzate e modulari basate su ESP32

## Requisiti target

| Requisito | Target |
|---|---|
| Costo totale componenti | ≤ 100 € |
| Latenza comando → azione | < 250 ms |
| Autonomia batteria | ≥ 60 min |
| Portata | ≥ 20 m indoor |

## Stack tecnico

- **MCU:** ESP32
- **Comunicazione:** WiFi/BLE (app ↔ carrozzina), ESP-NOW (radiocomando fisico)
- **Sensori:** VL53L1X (ToF), NEO-6M (GPS), accelerometro
- **Toolchain:** Arduino / ESP-IDF
- **PCB:** EDA open source

## Struttura del progetto

```
/firmware     # Firmware ESP32 (controllo motori, sensori, fail-safe)
/app          # App smartphone (comandi, stato, comandi vocali)
/pcb          # Schemi elettrici e progetti PCB
/docs         # Documentazione, requisiti, project charter
```

## Stato del progetto

In fase di analisi e architettura (M0–M1). Vedi le milestone nella documentazione di progetto per il piano completo fino alla demo finale (maggio 2027).

## Fuori scope

Carrozzina a grandezza reale, certificazione CE/dispositivo medico, navigazione autonoma avanzata, superamento ostacoli fisici, uso outdoor/lunghe distanze, produzione in serie.

## Licenza

Progetto open source — licenza da definire.

## Contatti

Per informazioni sul progetto: Zero Barriere Crema / team UpWheel.