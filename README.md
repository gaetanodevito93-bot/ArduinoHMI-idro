# ArduinoHMI-idro 🌱

**HMI SCADA per sistema idroponico / fertirrigazione automatica su Arduino R4 WiFi**

---

## File

| File | Descrizione |
|------|-------------|
| `hmi_fertirrigazione.html` | Interfaccia HMI completa — single file, ~100 KB |
| `SCHEMA_COLLEGAMENTI_ARDUINO_R4.md` | Schema elettrico, pinout, lista componenti |

## Funzionalità HMI

- **Schema di processo animato** — flusso liquido nei tubi, rotori pompe peristaltiche, glow sui componenti attivi
- **5 schermate**: Quadro · Schema · Ricette · Config · Manutenzione
- **Gestione ricette colturali** — CRUD completo con persistenza localStorage
- **Controllo attuatori** — modalità auto/manuale per ogni elemento
- **Sensori live** — pH e EC con scala graduata, 4 zone igrometria
- **Countdown manutenzione** — timer 30s per comandi manuali
- **Mobile-first** — ottimizzato per operatori in campo

## Pinout Arduino R4 WiFi

```
Attuatori (relè):
  GPIO 2  →  Peristaltica A
  GPIO 3  →  Peristaltica B
  GPIO 4  →  Peristaltica pH
  GPIO 5  →  Pompa ricircolo
  GPIO 6  →  Valvola 3 vie

Sensori (ADC):
  A0  →  Sensore pH
  A1  →  Sensore EC
  A2  →  Igrometro zona 1
  A3  →  Igrometro zona 2
  A4  →  Igrometro zona 3
  A5  →  Igrometro zona 4
```

## Utilizzo

1. Caricare `hmi_fertirrigazione.html` su Arduino R4 (SPIFFS)
2. Connettere al WiFi `FertiControl_AP`
3. Aprire `192.168.4.1` nel browser del telefono
