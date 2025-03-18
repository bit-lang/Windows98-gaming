# Windows 98 gaming

this is a wrapper app around [DosWasmX](https://github.com/nbarkhina/DosWasmX) (which in turn uses dosbox-x).

## playing Windows 98 games in your browser
- just click and run, NO virtual machines or emulators required. Never needing exhaustive installation and setup
- supports Windows 98 / 95 games, and DOS games without hassle
- Everything runs securely inside your browser (sandboxed), enabling it to run cross-OS, on 64bit Windows, and Linux

### comparing with other means to run Windows 9x games

| platform | GPU emulation | directx support | titles run well | titles can not run | note |
| --- | --- | --- | --- | --- | --- |
| doswasmx | S3 trio 64 | directx 6 | RedAlert (dx3), StarCraft1 (dx5), Age Of Empires (dx6) | Need For Speed 2, Delta Force | good for non-FPS gaming. no setup needed |
| |
| vmware / virtualbox | softGPU |directx 8 (up to directx 9) | Civilization3, Janes' IAF | Delta Force freezes | fast for most games. a little complex to setup |
| |
| 86box | various models, e.g.: voodoo 2000 | directx 6 / 7, depending on driver availability | Delta Force, Need for speed 2 in low graphics settings (640x480, 256 colors) | Civilization3, Jane's IAF | need drivers for chipsets, graphics, etc., which is sometimes hard to find |

### how to use the release
1. download the zip that matches your OS. for example, "AMD64-Linux" is for linux, where "AMD64-WIN" is for Windows
2. unzip the file to your specified folder
3. run the executable
   - Windows, just double click the .exe ( you need to grant the permission to run for the first time, if prompted by Windows 10 / 11 system )
   - Linux, chmod a+x on the extracted file, then run it in shell
4. your default browser will popup, click the "Start Windows" button to begin
5. for more usage instructions, see [here](https://github.com/nbarkhina/DosWasmX) or the [online manual](https://nbarkhina.github.io/DosWasmX/) 

### game installation, saving game play progress
- install the games you want to play
    - IMPORTANT: please remember to "save your harddrive" and "export harddrive", which includes changes you made (please refer to the above manual)
    - next time to run your installed games, use your exported hard disk image
- you can always install a new OS, or use your own disk image
    - you can find a copy of OS at [WinWorld](https://winworldpc.com/product/windows-98/98-second-edition)
    - find more Windows 9x games on [WinWorld](https://winworldpc.com/library/games) and on [archive.org](https://archive.org/details/software)

### about release files
- the pre-installed OS (Win 3.1 or 98) are just for convenience

| file | runs on | OS pre-installed |
| --- | --- | --- |
| win31runner-AMD64-Linux.zip | Linux on AMD64 | Windows 3.1 |
| win31runner-AMD64-WIN.zip | Windows 7(64bit)/10/11 on AMD64 | Windows 3.1 |
| win98runner-AMD64-WIN.zip | Windows 7(64bit)/10/11 on AMD64 | Windows 98 |

---

### below intro copied directly from the original repo

Supports the following features -
- Fully web based application - using web assembly
- Save hard drive to the browser (512mb, 1 gig, or 2 gig options)
- Automatic support for a variety of file formats (Iso, Zip, Bin, Cue, Img, 7z)
- Customize RAM (32mb, 64mb, 128mb)
- Import/export files into and out of the emulator
- Export your entire hard disk image for local saving
- Load/change CD while emulator is running
- Floppy Disk Support
- Speed up/slow down emulator time
- Mobile mode
- On scren keyboard
- Gamepad support
- Customize Mouse Sensitivity
- Dark Mode
- Audio support
- Full screen
- Zoom controls
- Mouse capture
- Resize resolution
- Customize CPU speed
- Host the application yourself
- Customize startup hard drive image
- Send CTRL/ALT/DELETE
- Pause/Unpause
- Import existing IMG hard disk if you already have one

# Screenshots

![screenshot](screenshots/screenshot2.png)


![screenshot](screenshots/screenshot3.png)


![screenshot](screenshots/screenshot4.png)


![screenshot](screenshots/screenshot5.png)


![screenshot](screenshots/screenshot6.png)


![screenshot](screenshots/screenshot7.png)


![screenshot](screenshots/screenshot8.png)

# Mobile Mode

![screenshot](screenshots/mobile.PNG)

# Overlay

- There is also a built in Overlay menu which can be accessed by pressing the tilde key on the keyboard "~"
- This can be useful for getting at certain functions when using a Gamepad Controller or to access the onscreen keyboard

![screenshot](screenshots/overlay.PNG)

![screenshot](screenshots/onscreenkeyboard.PNG)

# Installing Windows
DOS Wasm X supports installing Windows 95 or Windows 98 using your own copy of Windows. Simply drag and drop the ISO onto the startup page. DOS Wasm X will detect the Windows CD and begin the installation process. If you choose to Install Windows 95 you may get the error below. Simply click OK and then cancel when it asks you for the Path to the CD. This will allow you to continue with the installation. The reason for this error is because at this stage of the process the CD drivers have not yet been loaded. However after restarting Windows it will detect the CD Drive and finish installing the drivers successfuly. Always remember to shut down windows in the guest OS before exiting the page. This will automatically save your hard drive changes to the browser and prevent scandisk from running the next time you boot into Windows.

![screenshot](screenshots/win95error.PNG)

# References
The Following codebases were used in some part in creating this app

- DOSBox-X (Core Engine)
  - https://github.com/joncampbell123/dosbox-x 
- DOSBox Pure (Onscreen Keyboard)
  - https://github.com/schellingb/dosbox-pure
- JS Dos (JSDos Asyncify Module)
  - https://github.com/caiiiycuk/js-dos 
- Binaryen with Exceptions and Asyncify 
  - https://github.com/caiiiycuk/binaryen-fwasm-exceptions
- Emscripten 
  - https://github.com/emscripten-core/emscripten

# Disclaimer
This app was made for fun and is not affiliated or associated with Microsoft.
