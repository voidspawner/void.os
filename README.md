# V O I D os

## About

**⌜ V O I D os ⌟** is an **[Operating System](https://en.wikipedia.org/wiki/Operating_system)** that uses **[V O I D lang](https://github.com/voidspawner/void.lang)** to run and create applications and games.

> [!IMPORTANT]
> **The project is in the process of development.**

<img src="https://i.imgur.com/kx2UcUh.jpg" width="100%">

## Structure

The operating system is in a **single file**. This makes it easy to transfer it to different devices, backup and control damage or modification.
```
os.void
```
The operating system contains viewing and editing media and office files, working with the file system, web browser, social network client and server, network load balancing, interfacing with peripherals, virtualization tools, AI helper, creating applications and 3D・2D・VN games.

## Security

Each application can run in a separate isolated space, with a limited set of actions, or in a separate virtual machine, so that no data corruption or stealing occurs.

## V O I D os retro

An Operating System with **V O I D lang** that can run on retro computers.

|                   | <p align="center">**[Atari 65XE](https://en.wikipedia.org/wiki/Atari_8-bit_computers)**</p> | <p align="center">**[8086 CPU](https://en.wikipedia.org/wiki/Intel_8086)**</p> | <p align="center">**[80286 CPU](https://en.wikipedia.org/wiki/Intel_80286)**</p> |
| ----------------- | -------------------------------- | ----------------------------- | ----------------------------- |
| **Year**          | <p align="center">1985</p>       | <p align="center">1978</p>    | <p align="center">1982</p>    |
| **Transistors**   | <p align="center">3 510</p>      | <p align="center">29 000</p>  | <p align="center">134 000</p> |
| **Technology**    | <p align="center">8 μm</p>       | <p align="center">3 μm</p>    | <p align="center">1.5 μm</p>  |
| **Architecture**  | <p align="center">8 bit</p>      | <p align="center">16 bit</p>  | <p align="center">16 bit</p>  |
| **Instructions**  | <p align="center">55</p>         | <p align="center">81</p>      | <p align="center">109</p>     |
| **Clock Rate**    | <p align="center">1.79 Mhz</p>   | <p align="center">4 Mhz</p>   | <p align="center">12 Mhz</p>  |
| **Data Bus**      | <p align="center">8 bit</p>      | <p align="center">16 bit</p>  | <p align="center">16 bit</p>  |
| **Address Bus**   | <p align="center">16 bit</p>     | <p align="center">20 bit</p>  | <p align="center">24 bit</p>  |
| **Memory**        | <p align="center">64 kb</p>      | <p align="center">640 kb</p>  | <p align="center">640 kb</p>  |
| **HDD**           | <p align="center">-</p>          | <p align="center">40 Mb</p>   | <p align="center">40 Mb</p>   |
| **Floppy**        | <p align="center">5.25"</p>      | <p align="center">5.25"</p>   | <p align="center">5.25"</p>   |
| **Cartridge**     | <p align="center">+</p>          | <p align="center">-</p>       | <p align="center">-</p>       |
| **Cassette Tape** | <p align="center">+</p>          | <p align="center">-</p>       | <p align="center">-</p>       |
| **Joystick**      | <p align="center">+</p>          | <p align="center">-</p>       | <p align="center">-</p>       |
| **Mouse**         | <p align="center">+</p>          | <p align="center">+</p>       | <p align="center">+</p>       |
| **Keyboard**      | <p align="center">+</p>          | <p align="center">+</p>       | <p align="center">+</p>       |
| **Modem**         | <p align="center">300 baud</p> | <p align="center">300 baud</p>  | <p align="center">300 baud</p> |
| **Monitor**       | <p align="center">[TV](https://en.wikipedia.org/wiki/Analog_television)</p> | <p align="center">[EGA](https://en.wikipedia.org/wiki/Enhanced_Graphics_Adapter)</p> | <p align="center">[EGA](https://en.wikipedia.org/wiki/Enhanced_Graphics_Adapter)</p> |
| **Width**         | <p align="center">320</p>        | <p align="center">640</p>     | <p align="center">640</p>     |
| **Height**        | <p align="center">192</p>        | <p align="center">350</p>     | <p align="center">350</p>     |
| **Columns**       | <p align="center">40</p>         | <p align="center">80</p>      | <p align="center">80</p>      |
| **Rows**          | <p align="center">24</p>         | <p align="center">25</p>      | <p align="center">25</p>      |
| **Colors**        | <p align="center">16 (256)</p>   | <p align="center">16 (64)</p> | <p align="center">16 (64)</p> |

The operating system can be written using **[Assembly](https://en.wikipedia.org/wiki/Assembly_language)** and **[C++](https://en.wikipedia.org/wiki/C++)** languages. Or the direct use of **[opcodes](https://en.wikipedia.org/wiki/Opcode)**.

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

The first computers were just **advanced calculators**. To operate such a calculator, the Operating System was a programming language. Thus the **[IBM 5100](https://en.wikipedia.org/wiki/IBM_5100)** operating system was represented by two languages **[BASIC](https://en.wikipedia.org/wiki/BASIC)** and **[APL](https://en.wikipedia.org/wiki/APL_(programming_language))** (for working with matrix and other scientific calculations).

<img src="https://i.imgur.com/aZP4voi.jpeg" height=250> <img src="https://i.imgur.com/cf2aFtE.jpeg" height=250>

**[Retroinformática: IBM 5100 (1975)](https://www.neoteo.com/retroinformatica-ibm-5100-1975/)**

Later operating systems extended their file handling functionality. **[Unix](https://ru.wikipedia.org/wiki/Unix)**, **[CP/M](https://en.wikipedia.org/wiki/CP/M)**, **[DOS](https://en.wikipedia.org/wiki/DOS)** were simplified versions of programming languages for working with the file system.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/DEC_VT100_terminal.jpg/1024px-DEC_VT100_terminal.jpg" width=400>

**[DEC VT100 3 KB RAM (1978)](https://en.wikipedia.org/wiki/VT100)**

And even later, with the appearance of multitasking operating systems, applications began to use operating system **API** calls to access devices and display **user interface** (UI).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Macintosh_128k_transparency.png/640px-Macintosh_128k_transparency.png" height=270> <img src="https://upload.wikimedia.org/wikipedia/commons/7/79/Computer_macintosh_128k%2C_1984_%28all_about_Apple_onlus%29.jpg" height=270> <img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Macintosh-motherboard.jpg" height=270>

**[Macintosh 128K (1984)](https://en.wikipedia.org/wiki/Macintosh_128K)**

Computer technology is continually evolving.

| <p align="center">**Type**</p> | <p align="center">**Name**</p>                                                    | <p align="center">**Year**</p> |
| -----------------------  | --------------------------------------------------------------------------------------- | ------------------------------ |
| **Print**                | [**Johannes Gutenberg's Printing Press**](https://en.wikipedia.org/wiki/Printing_press) | <p align="center">1440</p>     |
| **Programmatic Control** | [**Jacquard Machine**](https://en.wikipedia.org/wiki/Jacquard_machine)                  | <p align="center">1804</p>     |
| **Programming Language** | [**Short Code**](https://en.wikipedia.org/wiki/Short_Code_(computer_language))          | <p align="center">1950</p>     |
| **OS**                   | [**GM-NAA I/O**](https://en.wikipedia.org/wiki/GM-NAA_I/O)                              | <p align="center">1956</p>     |
| **Game**                 | [**Spacewar!**](https://en.wikipedia.org/wiki/Spacewar!)                                | <p align="center">1962</p>     |
| **Multitasking OS**      | [**PDP-6**](https://en.wikipedia.org/wiki/PDP-6)                                        | <p align="center">1964</p>     |
| **3D Game**              | [**Battlezone**](https://en.wikipedia.org/wiki/Battlezone_(1980_video_game))            | <p align="center">1980</p>     |
| **HTTP Server**          | [**CERN httpd**](https://en.wikipedia.org/wiki/CERN_httpd)                              | <p align="center">1990</p>     |
| **Web Browser**          | [**WorldWideWeb**](https://en.wikipedia.org/wiki/WorldWideWeb)                          | <p align="center">1990</p>     |
| **Encoding**             | [**Unicode**](https://en.wikipedia.org/wiki/Unicode)                                    | <p align="center">1991</p>     |
| **Compress**             | [**Gzip**](https://en.wikipedia.org/wiki/Gzip)                                          | <p align="center">1992</p>     |
| **Web Language**         | [**JavaScript**](https://en.wikipedia.org/wiki/JavaScript)                              | <p align="center">1995</p>     |
| **Social Network**       | [**SixDegrees**](https://en.wikipedia.org/wiki/SixDegrees.com)                          | <p align="center">1997</p>     |
| **Web Data Format**      | [**JSON**](https://en.wikipedia.org/wiki/JSON)                                          | <p align="center">1999</p>     |
| **3D Craft Game**        | [**Minecraft**](https://en.wikipedia.org/wiki/Minecraft)                                | <p align="center">2009</p>     |
| **AI**                   | [**Stable Diffusion**](https://ru.wikipedia.org/wiki/Stable_Diffusion)                  | <p align="center">2022</p>     |

Now it has come to the point where applications can be created in simple descriptive language **V O I D lang**, and all the complex functionality residing directly in the **V O I D os**.

## V O I D lang
**[⌜ V O I D lang ⌟](https://github.com/voidspawner/void.lang)** is the language for rapidly creating applications in the **V O I D** or **[JSON format](https://ru.wikipedia.org/wiki/JSON)**. It is used as a replacement for both the standard Bash/CMD/etc. languages and for writing **UI Applications**, **Servers** and **Games**. The language uses one of the languages already preinstalled in the system. So you don't need to install anything else. Code and data are not separated. So the whole application fits in **one V O I D or JSON file**. Since the **code is presented as data**, applications can be easily generated with **AI**, updated, installed and launched remotely.
