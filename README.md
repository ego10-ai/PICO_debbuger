# Pico Debugger
A project for debugging and development with Raspberry Pi Pico.

## Description
Pico Debugger is a custom-built hardware debugger powered by the Raspberry Pi RP2350 microcontroller.Instead of using a messy breadboard and a standard Raspberry Pi Pico this custom board provides built-in voltage protection, debugs your code but also protects your computer from electrical spikes, adapts to any voltage, and tells you exactly how much power your project is consuming.

I accidentally crashed my Raspberry Pico debugger due to a voltage spike.
standard debuggers only operate at 3.3 volts—if you accidentally plug them into a 5-volt board, you fry your debugger , And that’s exactly what happened to me too


<img width="2722" height="1536" alt="green pcb" src="https://github.com/user-attachments/assets/2cdb3990-44ef-4c47-a548-720f644eb6a9" />

## Hardware Specifications (For the Nerds)
- Microcontroller: Raspberry Pi RP2350A (QFN-60)
- Memory: 16MB QSPI Flash (Winbond W25Q128JV)
- Core Power: Custom Switched-Mode Power Supply (SMPS) utilizing a 3.3µH inductor.
- Logic Level Shifting: * TXB0104 (4-Channel Auto-Direction) for SWD and UART.
- GT74LVC2T45 (Direction-locked) for Target Hardware Reset.
- Current Monitoring: INA226 Power Monitor with the high-power 0.1Ω Shunt Resistor.
- Target Power Supply: LM317 Linear Regulator.

## Board Stackup: 4-Layer PCB
- Layer 1:-Signal
- Layer 2:-Ground Plane
- Layer 3:- Power Plane (3.3V  |  1.1V  |   5V)
- Layer 4:- Signal

## hardware design and size
![](https://image-pro.easyeda.com/pullimages/ec28c74ef3a7441e872d8489a68be87a.webp)

## schemetic 
![](https://image-pro.easyeda.com/pullimages/3c2d42d304f94754812a3e237929c995.webp)

## BOM Table
## Bill of Materials (BOM)

| No. | Quantity | Comment | Designator | Footprint | Value | Manufacturer Part | Manufacturer | Supplier Part | Supplier |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 2 | TS-1187A-C-B-B | BOOTSEL,SYS_RST | SW-SMD_4P-L5.1-W5.1-P3.70-LS6.5-TL_H1.6 | | TS-1187A-C-B-B | XKB Connectivity | C1121873 | LCSC |
| 2 | 14 | 100nF | C1,C2,C3,C4,C5,C6,C7,C8,C9,C10,C15,C16 | C0603 | 100nF | | | | |
| 3 | 1 | 1µF | C11 | C0603 | 1µF | | | | |
| 4 | 1 | 2.2µF | C12 | C0603 | 2.2µF | | | | |
| 5 | 2 | 15pF | C13,C14 | C0603 | 15pF | | | | |
| 6 | 5 | 4.7µF | C17,C18,C19,C20,C21 | C0603 | 4.7µF | | | | |
| 7 | 1 | USBLC6-2SC6 | D2 | SOT-23-6_L2.9-W1.6-P0.95-LS2.8-BL | | USBLC6-2SC6 | TECH PUBLIC | C2827654 | LCSC |
| 8 | 2 | HDR-M_2.54_1x4P | Debug_Header,Serial_Header | HDR-TH_4P-P2.54-V-M | | | | | |
| 9 | 1 | HDR-M_2.54_2x4 | H1 | HDR-TH_8P-P2.54-V-M-R2-C4-S2.54 | | | | | |
| 10 | 1 | 3.3uH | L1 | IND-SMD_L2.0-W1.6 | 3.3uH | AOTA-B201610S3R3 | ABRACON | C42411119 | LCSC |
| 11 | 1 | WS2812B-V5 | LED1 | LED-SMD_4P-L5.0-W5.0-LS5.4-TL-1 | | WS2812B-V5 | worldsemi | C2846931 | LCSC |
| 12 | 2 | 5.1kΩ | R1,R2 | R0402 | 5.1kΩ | | | | |
| 13 | 2 | 27R | R3,R4 | R0402 | 27R | | | | |
| 14 | 1 | 330R | R5 | R0402 | 330R | | | | |
| 15 | 1 | 240R | R6 | R0402 | 240R | | | | |
| 16 | 1 | 390R | R7 | R0402 | 390R | | | | |
| 17 | 1 | UCR18EVHFS | R10 | R1206 | | UCR18EVHFS | ROHM | C20110261 | LCSC |
| 18 | 1 | 33R | R11 | R0402 | 33R | | | | |
| 19 | 2 | 4.7kΩ | R12,R13 | R0402 | 4.7kΩ | | | | |
| 20 | 1 | 1K | R14 | R0402 | 1K | | | | |
| 21 | 1 | RP2350A | U1 | QFN-60_L7.0-W7.0-P0.40-TL-EP3.4 | | RP2350A | Raspberry Pi | C42411118 | LCSC |
| 22 | 1 | 12MHz | U2 | CRYSTAL-SMD_4P-L3.2-W2.5-BL | 12MHz | ABM8-272-T3 | ABRACON | C20625731 | LCSC |
| 23 | 1 | TXB0104PWR | U3 | TSSOP-14_L5.0-W4.4-P0.65-LS6.4-BL | | TXB0104PWR | TI | C60708 | LCSC |
| 24 | 1 | W25Q128JVSIQ | U8 | SOIC-8_L5.3-W5.3-P1.27-LS8.0-BL | | W25Q128JVSIQ | Winbond | C113767 | LCSC |
| 25 | 1 | AP2112K-3.3TRG1 | U9 | SOT-25-5_L2.9-W1.6-P0.95-LS2.8-BL | | AP2112K-3.3TRG1 | DIODES | C51118 | LCSC |
| 26 | 1 | LM317 | U10 | TO-252-3_L6.5-W5.9-P4.60-LS10.0-BL | | LM317 | GOODWORK | C42457465 | LCSC |
| 27 | 1 | GT74LVC2T45V8 | U11 | VSSOP-8_L2.3-W2.0-P0.50-LS3.1-BL | | GT74LVC2T45V8 | GTIC | C22356905 | LCSC |
| 28 | 1 | INA226AIDGSR | U13 | MSOP-10_L3.0-W3.0-P0.50-LS5.0-BL | | INA226AIDGSR | TI | C49851 | LCSC |
| 29 | 1 | TYPE-C16PIN | USB1 | USB-C-SMD_TYPE-C16PIN | | TYPE-C16PIN | SHOU HAN | C393939 | LCSC |

## Files

- `Netlist_Schematic1_2026-04-05.tel`: Netlist file
- `ProPrj_pico debugger_2026-04-05.epro`: Project file

## Usage
You plug the probe into your PC using a standard USB-C cable and your computer automatically recognizes it as a standard "CMSIS-DAP" debugging device. You connect the probe's debug wires to your target circuit. Using standard software (like VS Code and OpenOCD), you can click "Run" to flash your firmware step through your C/C++ or Rust code line-by-line and read serial printf() outputs all through one single USB cable.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
