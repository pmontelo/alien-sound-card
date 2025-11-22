# SP0256-AL2 Allophone Reference

This document provides a complete reference for the allophones supported by the SP0256-AL2 speech synthesis chip used in the Alien Sound Card. Allophones are basic speech sound units that can be combined to form words and phrases. The chip has 64 allophones, including pauses.

Data is sourced from the official General Instrument SP0256-AL2 datasheet. Use these codes in your BASIC programs by POKEing the decimal values to the card's address.

## Allophone Table

| Decimal | Hex   | Symbol | Example   | Duration (ms) |
|---------|-------|--------|-----------|---------------|
| 0       | 0x00  | PA1    | PAUSE     | 10            |
| 1       | 0x01  | PA2    | PAUSE     | 30            |
| 2       | 0x02  | PA3    | PAUSE     | 50            |
| 3       | 0x03  | PA4    | PAUSE     | 100           |
| 4       | 0x04  | PA5    | PAUSE     | 200           |
| 5       | 0x05  | OY     | Boy       | 420           |
| 6       | 0x06  | AY     | Sky       | 260           |
| 7       | 0x07  | EH     | End       | 70            |
| 8       | 0x08  | KK3    | Comb      | 120           |
| 9       | 0x09  | PP     | Pow       | 210           |
| 10      | 0x0A  | JH     | Dodge     | 140           |
| 11      | 0x0B  | NN1    | Thin      | 140           |
| 12      | 0x0C  | IH     | Sit       | 70            |
| 13      | 0x0D  | TT2    | To        | 140           |
| 14      | 0x0E  | RR1    | Rural     | 170           |
| 15      | 0x0F  | AX     | Succeed   | 70            |
| 16      | 0x10  | MM     | Milk      | 180           |
| 17      | 0x11  | TT1    | Part      | 100           |
| 18      | 0x12  | DH1    | They      | 290           |
| 19      | 0x13  | IY     | See       | 250           |
| 20      | 0x14  | EY     | Beige     | 280           |
| 21      | 0x15  | OO1    | Could     | 70            |
| 22      | 0x16  | UW1    | To        | 100           |
| 23      | 0x17  | AO     | Aught     | 100           |
| 24      | 0x18  | AA     | Hot       | 100           |
| 25      | 0x19  | YY2    | Yes       | 180           |
| 26      | 0x1A  | AE     | Hat       | 120           |
| 27      | 0x1B  | HH1    | He        | 130           |
| 28      | 0x1C  | BB1    | Business  | 80            |
| 29      | 0x1D  | TH     | Thin      | 180           |
| 30      | 0x1E  | UH     | Book      | 100           |
| 31      | 0x1F  | UW2    | Food      | 260           |
| 32      | 0x20  | AW     | Out       | 370           |
| 33      | 0x21  | OO2    | Do        | 160           |
| 34      | 0x22  | GG3    | Wig       | 140           |
| 35      | 0x23  | VV     | Vest      | 190           |
| 36      | 0x24  | GG1    | Got       | 80            |
| 37      | 0x25  | SH     | Ship      | 160           |
| 38      | 0x26  | ZH     | Azure     | 190           |
| 39      | 0x27  | RR2    | Brain     | 120           |
| 40      | 0x28  | FF     | Food      | 150           |
| 41      | 0x29  | KK2    | Sky       | 190           |
| 42      | 0x2A  | KK1    | Can't     | 160           |
| 43      | 0x2B  | ZZ     | Zoo       | 210           |
| 44      | 0x2C  | NG     | Anchor    | 220           |
| 45      | 0x2D  | LL     | Lake      | 110           |
| 46      | 0x2E  | WW     | Wool      | 180           |
| 47      | 0x2F  | XR     | Repair    | 360           |
| 48      | 0x30  | WH     | Whig      | 200           |
| 49      | 0x31  | YY1    | Yes       | 130           |
| 50      | 0x32  | CH     | Church    | 190           |
| 51      | 0x33  | ER1    | Fir       | 160           |
| 52      | 0x34  | ER2    | Fir       | 300           |
| 53      | 0x35  | OW     | Beau      | 240           |
| 54      | 0x36  | DH2    | They      | 240           |
| 55      | 0x37  | SS     | Vest      | 90            |
| 56      | 0x38  | NN2    | No        | 190           |
| 57      | 0x39  | HH2    | Hoe       | 180           |
| 58      | 0x3A  | OR     | Store     | 330           |
| 59      | 0x3B  | AR     | Alarm     | 290           |
| 60      | 0x3C  | YR     | Clear     | 350           |
| 61      | 0x3D  | GG2    | Guest     | 40            |
| 62      | 0x3E  | EL     | Saddle    | 190           |
| 63      | 0x3F  | BB2    | Business  | 50            |

## Usage Notes
- **Pauses (0-4)**: Use PA3 (2) or PA4 (3) for short word breaks, PA5 (4) for longer sentence pauses.
- **Combining Allophones**: Experiment with sequences to approximate English words. For example, "Hello" might be: HH1 (27), EH (7), LL (45), OW (53).
- **Timing**: The durations are approximate; your BASIC code's delay loops should account for processing time to avoid overlapping sounds.
- **Datasheet Reference**: For more details, consult the original SP0256-AL2 documentation from General Instrument (now Microchip).
