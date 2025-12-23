# Intro

This project is my hobbyist attempt to update the TrellisBoard to a production-level state in 2026. 

## About Me

 - I barely know anything about PCB prototyping, but I think the TrellisBoard project is very cool and useful, so I want to revive it. I am currently employed by an aerospace company as a control engineer, so I will be working on this project in my free time only. No deadlines, just fun. 
 - Using mostly luck and LiteX, I managed to get a fully working Linux rv64 system running on my ULX3S board with a full RocketChip core. However, due to the RAM limitations of that board, I couldn’t do anything particularly interesting with it. That’s why I see this project as a good way to waste my free time.

## Next steps
 - Current DDR3L chip is obsolete, need to do minor changes to the board for a replacement.
 - The board fails several ~400 robustness checks when run in KiCad 7. Since the project was originally designed in KiCad 5, I want to confirm whether these are all false flags, which may take a while.
 - 3D model is currently not working on Kicad 7 as expected, need to check why.
 - stuff


## Key Features 
 - Largest ECP5; LFE5UM5G-85F
 - PCIe 2.0 x2 card edge connector on two SERDES channels
 - Remaining two SERDES channels on M.2 E-key connector
 - 1GByte x32 DDR3L (two x16 chips)
 - Dedicated HDMI output, using TFP410 serialiser
 - 1000BASE-T GbE connector with RGMII PHY
 - USB-A 2.0 host connector with ULPI PHY
 - FT2232H for debug JTAG and UART/FIFO with type-C connector
 - PCIe, external 12V or USB power input
 - 12 bicolour (tristate) user LEDs, 4 user buttons, 8 user DIP switches
 - 128Mbit QSPI flash for boot and data
 - microSD card connector
 - Dual PMOD connector with extra "middle" IO pins
 - As many remaining IO as possible on high speed FFC connectors with a differential optimised pinout (3x 24 IO). Selectable 1.8V/2.5V/3.3V

## Layout
 - PCIe card form factor
 - At least Ethernet, USB-A, USB type-C power/debug and HDMI out
 - Other connectors probably would have to be on other sides. FFC connectors probably on top so they can loop over to another card to form a 2-slot card (e.g. with ADCs/DACs for SDR/DAQ)

## Possible accessories using high-speed FFC connectors
 - MIPI DSI smartphone-style LCDs
 - MIPI CSI-2 cameras
 - High speed ADC/DAC
 - HDMI in/out, direct or using serialiser chip
 - LVDS video in/out for LCDs or block cameras
 - Breakout board to dual or triple PMOD
