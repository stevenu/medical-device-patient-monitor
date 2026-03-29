Medical Device Patient Monitor

A six-phase connected patient monitoring system built to support a career pivot into medical device Field Application Engineering.
Web developer + electronics engineering technician certificate — learning in public.



System architecture

| Phase | Device | Protocol | Output | Status |
|-------|--------|----------|--------|--------|
| 1 | Arduino Uno + DS18B20 | 1-Wire + USB Serial | TM1637 LED display | ⏳ In progress |
| 2 | ESP32 + MAX30102 | I2C + BLE GATT | SSD1306 OLED + phone | |
| 3 | STM32 + ADS1292R ECG AFE | SPI + UART | Python ECG viewer | |
| 4 | Raspberry Pi gateway | MQTT + WebSocket | iPad Safari dashboard | |
| 5 | AWS IoT Core pipeline | MQTT/TLS + REST | Amplify dashboard + SNS | |
| 6 | HL7 v2 + FHIR R4 | HL7 ORU^R01 + FHIR | HAPI FHIR server | |



What this project builds

A complete connected medical device data platform from sensor to clinical interoperability:
sensor acquisition → embedded firmware → wired/wireless transport →
local gateway + alarm logic → cloud ingestion → FHIR R4 clinical observation

Each phase is fully standalone before connecting to the next.
Each phase has full engineering documentation in /docs.



Quick start

Phase 1 (Arduino) — requires Arduino IDE 2.x:
  1. Open phase1-arduino-temp/firmware/temp_monitor/temp_monitor.ino
  2. Install libraries: OneWire, DallasTemperature, TM1637Display
  3. Upload to Arduino Uno
  4. Wire per phase1-arduino-temp/README.md wiring table

Phase 4 (Pi gateway) — requires Raspberry Pi with Python 3.9+:
  cd phase4-rpi-gateway
  pip install -r requirements.txt
  python3 gateway/normalizer.py



Documentation

Full phase documents (BOM, wiring, test plan, protocol spec) are in /docs.
Each document was written to mirror ISO 13485 controlled document conventions.



Safety

This project is not a medical device. See SAFETY.md.
The Phase 3 ECG circuit has no patient electrical isolation.
Not for clinical use under any circumstances.



Author

[Steven Usrey](https://github.com/stevenu). 
LinkedIn: linkedin.com/in/stevenusrey. 
Building toward Medical Device FAE — following along via the LinkedIn post series.  
