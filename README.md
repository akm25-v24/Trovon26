# Trovon26 – Voron 2.4 350mm Klipper Config Backup

Backup repository for a **New Voron 2.4 350mm** build.  
This is a modified **Troodon 2.0 Pro** kit from [Formbot](https://www.formbot3d.com/).

## Hardware Summary

| Component | Details |
|---|---|
| Motion system | CoreXY – Voron 2.4 R2 |
| Build volume | 350 × 350 × 350 mm |
| Controller | BigTreeTech Octopus 1.1 |
| Drivers | TMC2209 (UART) |
| Stepper motors | LDO-42STH48-2004AC (A/B), LDO-42STH48-2004AC (Z×4) |
| Toolhead | Stealthburner + Clockwork 2 (CW2) |
| Extruder motor | LDO-36STH20-1004AHG |
| Hotend | Revo Voron (or Dragon HF) |
| Probe | Voron TAP (optical) |
| Heated bed | 350mm cast aluminium + silicone mounts |
| Display | BTT Mini 12864 |
| Host | Raspberry Pi 4B running MainsailOS |

## Software

- **Klipper** firmware
- **Mainsail** web interface
- **Moonraker** API layer

## File Structure

```
├── printer.cfg        # Main Klipper config (hardware pins, motion, sensors)
├── macros.cfg         # Print macros: PRINT_START, PRINT_END, etc.
├── mainsail.cfg       # Mainsail-required macros and settings
└── README.md          # This file
```

## Usage

1. Copy all `.cfg` files to `~/printer_data/config/` on your host.  
2. Verify pin assignments in `printer.cfg` match your actual wiring.  
3. Follow the [Voron Initial Startup](https://docs.vorondesign.com/build/startup/) guide before first print.

## Notes

- Quad-gantry-level (QGL) and bed mesh levelling are enabled.
- Input shaper (ADXL345) calibration values are stored in `printer.cfg`.
- All macros are located in `macros.cfg` to keep `printer.cfg` clean.

