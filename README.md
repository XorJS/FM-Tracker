# FM-Tracker

FM-Tracker is a tracker I did for my computer science school project in 2000.
It was a tool I created for my main project (3d game). Both were in 100% assembly code.

![Screenshot0](/Screenshots/screenshot0.png)

![Screenshot1](/Screenshots/screenshot1.png)

More info here: https://www.jsr-productions.com/blogpost3319ddc.html

## Examples

[![FM-Tracker: Kubic Quest Game Song 001](http://img.youtube.com/vi/MQVUb87Btz0/0.jpg)](http://www.youtube.com/watch?v=MQVUb87Btz0 "FM-Tracker: Kubic Quest Game Song 001")

[![FM-Tracker: Kubic Quest Game Song 002](http://img.youtube.com/vi/xT0vLQ_nlxE/0.jpg)](http://www.youtube.com/watch?v=xT0vLQ_nlxE "FM-Tracker: Kubic Quest Game Song 002")

## Requirements

### Run

- Download and install DosBox: https://www.dosbox.com/

### Compile

- Turbo Assembler: https://en.wikipedia.org/wiki/Turbo_Assembler 

## Files

- **Build.bat**: Launch turbo assembler (TASM) to compile and generate the FM-Tracker executable
- **dosbox-template.conf**: My DosBox config that work with FM-Tracker
- **FM.ASM**: FM-Tracker source code
- **FM2000.exe**: Official version to run on real hardware (e.g Dos 6.22 / 386dx)
- **FM.exe**: Fixed version for DosBox
- **License***: MIT License
- **README.md**: Déjà Vu!
- **PEPSI1.FMT, PEPSI2.FMT, TESTFF.FMT**: Test songs
- **Screenshots**: Screenshot folder

## Build
```
tasm fm.asm
tlink fm.obj /3
```

If you want to run on real hardware, you should replace those lines in FM.asm:

```
[4294] ;[DosBox] Call Get_Free_Xms
[4295] ;[DosBox] Call Check_Flat_Mode
[4296] ;[DosBox] Call Install_Flat_Mode
```
by
```
[4294] Call Get_Free_Xms
[4295] Call Check_Flat_Mode
[4296] Call Install_Flat_Mode
```

## Notes

*Did in 2000, the code was in English but comments in French… Sorry!*
