# NES

- [Assembly Simulator](http://skilldrick.github.io/easy6502/)
- [6502 Documentation](http://www.6502.org/tutorials/6502opcodes.html)
- [Tutorial](https://www.kibrit.tech/en/blog/nes-game-development-part-1)

## Editor
 - VS Code
 - Extension: [ca65 Macro Assembler Language Support (6502/65816)](https://marketplace.visualstudio.com/items?itemName=tlgkccampbell.code-ca65)

## Assembler
[ca65](https://cc65.github.io/) is a cross-platform assembler for the 6502/65816 microprocessors.

## Emulators
- [BusyRock]()
- [FCEUX](https://fceux.com/web/home.html)


## Hardware

### CPU:
### PPU: Picture Processing Unit.
### PPU RAM:
#### 1) Pattern Tables
  - 2 Pattern Tables
  - 64kb of memory
  - Each tile is 8px x 8px
  - 256 Sprite Tiles / Table (16 x 16 tiles = 256)
- CHR-RAM: Character RAM.
#### 2) Nametables (Screen background design)
 - 32 x 30 tiles (fullscreen: 256px x 240px)
 - Each tile is 8px x 8px
 - 1 byte per tile
 - From Pattern Tables 
#### 3) Pallets (Colors)
 - $00 $01 $02 $03 $04 $05 $06 $07 $08 $09 $0A $0B $0C $0D $0E $0F
 - $10 $11 $12 $13 $14 $15 $16 $17 $18 $19 $1A $1B $1C $1D $1E $1F
 - $20 $21 $22 $23 $24 $25 $26 $27 $28 $29 $2A $2B $2C $2D $2E $2F
 - $30 $31 $32 $33 $34 $35 $36 $37 $38 $39 $3A $3B $3C $3D $3E $3F
- Palette RAM: can store 8 colors at time. 4 for background and 4 fore foreground.
#### 4) OAM: Object Attribute Memory. Is the sprites memory.
 - Independent Sprites
 - In front or behind Backgrounds
 - Characters, enemies, effects, etc.
 - Bytes:
   - 1: y-coordinate 
   - 2: Pattern tile
   - 3: Sprite attributes 
     - B7: Flip Vertical 
     - B6: Flip Horizontal
     - B5: Above/Below Background toggle
     - B4 B3 B2: Unused 
     - B1 B0: Pallet Select
   - 4: x-coordinate 

Televisions
CRT: Cathode Ray Tube
NTSC: North America / Japan. 60 frames per second. 525 scanlines.
SECAM:
PAL or PAL/SECAM: Europe, Africa, etc. 50 frames per second. 625 scanlines.

## 6502 Processor Program

### Storage Memory: 6 registers:
 - A: general programming.
 - X: general programming. Index Register
 - Y: general programming. Index Register
 - PC: internal information.
 - SP: internal information.
 - SR: internal information.

### System Memory
 - 64kb
 - RAM, PRG-ROM
 - 16-bit Addressing

### Instructions
 - ADC: Addition (with Carry)
 - SBC: Subtraction (with Carry)
 - ASL: Arithmetic Shift Left ("multiply by 2")
 - LSR: Logical Shift Right ("divide by 2")
 - INX: Increment X
 - INY: Increment Y
 - DEX: Decrement X
 - DEY: Decrement Y
 - CMP: CoMPare accumulator
 - BNE: Branch on Not Equal
 - BCS: Branch on Carry Set
 - LDX: LoaD X register
 - LDY: LoaD Y register
 - RTS: ReTurn from Subroutine

### .nes file
CTRL+Shift+P: run build task
