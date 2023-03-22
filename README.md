# XTIDE-OLM
A Compact Flash to ISA bus adapter with XTIDE BIOS support

Based on Glitch Works XT-IDE: https://github.com/glitchwrks/xt_ide


So far tested with SST39F010 and AT28C64 Flash(writen with "xtidecfg.com") and 27C512 burned with TL866 programmer.
Works on PC-XT and PC-AT. Tested with 8088, 286, 386 and 486 computers. 

Designed for Keystone 9202 bracket. The bracket has no window for CF card, so it must be drilled manually.
Also the bracket can be 3D-printed. The 3D model is in "XTIDE_OLM-bracket.STL" file.

For 32K BIOS ROM R14 and R15 need to be be removed and mounted for 8K ROM (e.g. 2864).
There is no issue if R14 and R15 unmounted with 8K ROM, but in this case BIOS ROM window is 32K and configured by SW1.1 and SW1.2 only.

# XTIDE BIOS:
Can be obtained here: https://www.xtideuniversalbios.org/

# How to configure:
1. Set BIOS and I/O addresses by DIP switches SW1 and SW2.
2. Configure BIOS using XTIDECFG.
- Start XTIDECFG
- Select "Load BIOS from file" and load BIOS you want to flash.
- Go to "Configure XTIDE Universal BIOS". Usually I select "Auto configure"(CF card must be inserted) or manually configure it as needed.
- Go to "Flash EEPROM" and select "2864" or "SS39SFxx"(depends on installed Flash IC) and flash the BIOS.
- Reboot your computer.

![image](https://user-images.githubusercontent.com/81614352/210622587-e67f588a-6c4d-4cc8-9c85-02a1a3515ecb.png)
