# Legacy Firmware dumps

## Backup

```bash
sudo avrdude -c stk500v2 -P /dev/ttyUSB0 -p atmega2560   -U flash:r:flash1.hex:i
sudo avrdude -c stk500v2 -P /dev/ttyUSB0 -p atmega2560   -U eeprom:r:eeprom1.hex:i
```

## Restore

Both, firmware and eeprom have to be flashed to restore to a working state

```bash
sudo avrdude -c stk500v2 -P /dev/ttyUSB0 -p atmega2560   -U flash:w:flash1.hex:i
sudo avrdude -c stk500v2 -P /dev/ttyUSB0 -p atmega2560   -U eeprom:w:eeprom1.hex:i
```
