OMEN Alpha Monitor v4
=====================

Alpha Monitor Version 4 brings some new features. The main feature is a modular conception.

You can use the remain of 32 kB EEPROM for your user programs, seamlessly integrated into the system.

Monitor has a new command "U" - List user modules. This command check the whole EEPROM for a module signature.

Modules has begin at addresses xx00h. Its first instruction should be JMP somewhere. From the address xx03h has to be a "magic string", followed by a module name string (stored as "last character OR 80h"). Magic string is "MOD4". So for example:

```
 .ALIGN 256
 JMP MODBEGIN
 DB "MOD4"
 .ISTR "Example module"
MODBEGIN: ...
```

See module-test and module-basic files.

You can now use some monitor routines:

`RST 1` sends the value in accumulator to the serial port.

`RST 2` calls the SERIN routine - it checks serial port and returns the last character received in the A register (accumulator). If there is no character waiting, it sets Z flag.

`RST 3` is a SYSCALL - System call routine. It is followed by a byte, which specify the desired function. Values are:

| value | function |
| --- | --- |
| 0 | Reset |
| 1 | Warm restart |
| 2 | SERST - Serial Receiver Status. If none is received, returns A=0, Z=1, otherwise Z=0, A=FFh |
| 3 | SERIN - as RST 2 |
| 4 | SEROUT - as RST 1 |
| 5 | STROUT - sends string from HL to serial port. String is ended by a character with bit 7 = 1 |

```
    LXI H, HELLO
    RST 3
    DB 5
     ...

HELLO:
    .ISTR   "Test module",$0d,$0a 
; or: .DB   "Test module",$0d,$0a+$80 
```
