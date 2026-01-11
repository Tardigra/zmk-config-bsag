# Totem ZMK Config

## Flashing Instructions (Seeed XIAO BLE)

### Enter Bootloader Mode
Double-tap the reset button quickly. A USB drive will appear.

### First Time / Pairing Issues
If the halves don't communicate, flash the settings reset first to clear old Bluetooth bonds:

1. Flash `settings_reset.uf2` to both halves (order doesn't matter)
2. Flash `totem_right.uf2` to the **right half first** (peripheral)
3. Flash `totem_left.uf2` to the **left half last** (central)

The central (left) half initiates pairing, so it should boot after the peripheral (right) is ready.

### Regular Firmware Updates
If both halves are already paired and working:

1. Flash `totem_left.uf2` to the left half
2. Flash `totem_right.uf2` to the right half

Only use settings_reset when experiencing pairing/connection issues.
