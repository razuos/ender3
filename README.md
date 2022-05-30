# Flashing

In order to flash new klipper versions on the SKR Mini E3 V2 board, i needed to reformat the sdcard using a MBR partition table and FAT32 file system and copy the firmware file and rename it as `FIRMWARE.BIN` in the root of the sdcard.

Then i needed to reboot the printer via PSU or reset switch on the SKR.

# Compiling firmware

- Ensure that the micro-controller architecture is set to ‘STM32’
- Ensure that the processor model is set to ‘STM32F103’
- Ensure that the Bootloader offset is set to ‘28KiB’
- Ensure that the Clock Reference is set to ‘8 Mhz’
- Ensure that “Enable extra low-level configuration options” is selected.
- Ensure that “Use USB for communication (instead of serial)” is selected.
- Ensure that “GPIO pins to set at micro-controller startup” includes ‘!PA14’.
