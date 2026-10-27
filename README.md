# ESP32-C6 Temperature and humidity sensors

Custom environmental sensor node based on the ESP32-C6 (Wi-Fi 6, BLE 5, Zigbee/Thread). It features three distinct temperature and humidity sensors on a shared I2C bus, is powered via USB-C (3.3V LDO), and includes two external 3-pin headers for hardware expansion.

## IC List

- ESP32-C6 (MCU)
- HDC2080 (humidity & temperature sensor)
- TMP102 (temperature sensor)
- LM75 (temperature sensor)
- TLV75733PDBVR (LDO)

## Top preview
<img width="1271" height="831" alt="Thermometer2" src="https://github.com/user-attachments/assets/c64ba8fe-3b03-4a5f-be08-3abf14026bf8" />

## Preview 3d render
<img width="1264" height="816" alt="Thermometer3" src="https://github.com/user-attachments/assets/5fe4c36f-7b80-422d-8bdd-5e65f5fcd92e" />

```c
// Shared I2C bus (Sensors)
#define I2C_SCL_PIN GPIO7
#define I2C_SDA_PIN GPIO6

// Expansion connectors (External 3-pin headers)
#define EXT_HEADER_1_PIN GPIO2
#define EXT_HEADER_2_PIN GPIO3

// Hardware sensor interrupts
#define DRDY_PIN GPIO20   // HDC2080 interrupt
#define ALERT_PIN GPIO19  // TMP102 alert
#define OS_PIN GPIO18     // LM75 thermal alarm
```
