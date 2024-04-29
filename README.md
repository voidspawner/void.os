# V O I D os

**⌜ V O I D os ⌟** is an Operating System that uses **V O I D lang** to run and create applications and games.

**The project is in the process of development. Code and description are subject to change and inconsistency.**

<img src="https://i.imgur.com/kx2UcUh.jpg" width="100%">

## Contains

- **V O I D lang**
- **V O I D format**
- **V O I D social**
- **V O I D engine**
- **V O I D ai**
- **V O I D tech**
- Spatial arrangement of speakers, screens and effects
- Unicode
- Network
- OpenGL / Vulkan
- Drivers
- Fonts
- Apps
  - Social
  - Office (Text / Cells / Code Editor)
  - Calc
  - Shop
  - Video / Sound / Image / 3D Editor
  - Video / Sound / Image / 3D Player
  - File Manager
  - Web Browser
  - Virtual Machine / Emulator
  - AI Helper
  - AI Translate
  - AI Creator
  - Settings
  - Cloud
- Games

## Structure

The operating system is in a **single file**. This makes it easy to transfer it to different devices, backup and control damage or modification.
```
void.void
```

## Security

Each application can run in a separate isolated space, with a limited set of actions, or in a separate virtual machine, so that no data corruption or stealing occurs.

## V O I D os retro

An Operating System with **V O I D lang** that can run on retro computers.

- **[Atari 65XE](https://en.wikipedia.org/wiki/Atari_8-bit_computers) / [8086 CPU](https://en.wikipedia.org/wiki/Intel_8086) / [80286 CPU](https://en.wikipedia.org/wiki/Intel_80286)**
- **1.8 / 5 / 12 Mhz CPU Clock**
- **8 / 16 Bit Architecture**
- **64 / 640 KB RAM**
- **40 MB HDD**
- **[TV](https://en.wikipedia.org/wiki/Analog_television) / [EGA](https://en.wikipedia.org/wiki/Enhanced_Graphics_Adapter) / [VGA](https://en.wikipedia.org/wiki/Video_Graphics_Array) / [SVGA](https://en.wikipedia.org/wiki/Super_VGA) Video Card**
- **Keyboard / Mouse / Joystick**

```assembly
        .org $c000    ; Starting address of the program

start   lda #<message ; Load message address
        sta $07f8     ; Set string output address
        lda #>message
        sta $07f9

        lda #13       ; Select color (text white, background black)
        jsr $e544     ; Calling system function

loop    lda message,x ; Load character from string
        beq done      ; If the character is null, terminate
        jsr $e716     ; Output the character to the screen
        inx           ; Increase string index
        bne loop      ; Go to next character

done    rts           ; Return from the program

message .byte "Hi World :)", 0 ; Message string
```

## A Bit of History

The first computers were just **advanced calculators**. To operate such a calculator, the Operating System was a programming language. Thus the **[IBM 5100](https://en.wikipedia.org/wiki/IBM_5100)** operating system was represented by two languages **BASIC** and **APL** (for working with matrix and other scientific calculations).

<img src="https://i.imgur.com/aZP4voi.jpeg">
<img src="https://i.imgur.com/cf2aFtE.jpeg" width=584>

**[Retroinformática: IBM 5100 (1975)](https://www.neoteo.com/retroinformatica-ibm-5100-1975/)**

Later operating systems extended their file handling functionality. **Unix**, **CP/M**, **DOS** were simplified versions of programming languages for working with the file system.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/DEC_VT100_terminal.jpg/1024px-DEC_VT100_terminal.jpg" width=584>

**[DEC VT100 3 KB RAM (1978)](https://en.wikipedia.org/wiki/VT100)**

And even later, with the appearance of multitasking operating systems, applications began to use operating system **API** calls to access devices and display **user interface** (UI).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Macintosh_128k_transparency.png/640px-Macintosh_128k_transparency.png" width=300>

**[Macintosh 128K (1984)](https://en.wikipedia.org/wiki/Macintosh_128K)**

Now it has come to the point where applications can be created in simple descriptive language **V O I D lang**, and all the complex functionality resides directly in the **V O I D os** operating system.


## V O I D lang
**[⌜ V O I D lang ⌟](https://github.com/voidspawner/void.lang)** is the language for rapidly creating applications in the **JSON format**. It is used as a replacement for both the standard Bash/CMD/etc. languages and for writing **UI Applications**, **Servers** and **Games**. The language uses one of the languages already preinstalled in the system. So you don't need to install anything else. Code and data are not separated. So the whole application fits in **one JSON file**. Since the **code is presented as data**, applications can be easily generated with **AI**, updated, installed and launched remotely.

## V O I D format
**[⌜ V O I D format ⌟](https://github.com/voidspawner/void.format)** is the data format that inherits the best features of **JSON**, **YAML**, **CSV** formats. Makes it easier to write and read data, both by human and by program.

## V O I D engine
**[⌜ V O I D engine ⌟](https://github.com/voidspawner/void.lang#game-engine)** is a compiled **V O I D spawner** game for rapidly creating apps and games in **V O I D lang**.

## V O I D ai
Generate **images・videos・texts・assets**. A limited number of uses are available for free. To use extra **V O I D ai** you can **pay** with **⦵ voids** digital currency.

## V O I D voids
Digital currency used in the **V O I D ecosystem**.

- Name ```voids```
- Symbol ```⦵```
- Exchange rate ```⦵ 1``` = ```$ 1``` = ```USD₮ 1```

The currency is also a **spawner**. Every month the profit is distributed among the **voids** holders. The number of voids increases proportionally and can be withdrawn to other digital currencies.

## V O I D social
**[⌜ V O I D social ⌟](https://voidsp.com)** is a **social network** for messaging, sharing apps, games, images, videos and other content. Buy and sell, find job, crypto exchange, transfer **V O I D voids** and more other.
