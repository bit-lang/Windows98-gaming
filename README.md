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
| vmware / virtualbox | softGPU |directx 8 (up to directx 9) | Civilization3, Jane's IAF | Delta Force freezes | must install vmware, and a little complicated to setup softGPU |
| |
| 86box | various models, e.g.: voodoo 2000 | directx 6 / 7, depending on driver availability | Delta Force, Need for speed 2 in low graphics settings (640x480, 256 colors) | Civilization3, Jane's IAF | need drivers for chipsets, graphics, etc., which is sometimes hard to find |

### see the Windows 3.1 demo
1. download win31-demo-AMD64.exe from release
2. double click to run. you may need to grant the permission to run for the first time, if prompted by Windows 10 / 11 system
   a command prompt window will open, along a browser window
   [first-run](images/win31-startup.jpg)
3. in the browser window, click the "Start Windows" button to begin
   [windows 3.1 demo](images/Win31-demo.png)
4. to stop the demo, [exit windows 3.1](images/exit-win31.png)
5. now you can type "stop" at the command window prompt, can close the browser

### install your own Windows 98 (or Windows 95)
1. download win9x_blank-disk-AMD64.zip from release, extract the file to a folder you want
2. double click to run the extracted exe file
   - DO NOT click on "start Windows", instead,  drag your Windows 98 installation ISO file to the page center frame (as indicated on page)
   - you will be granted with a command line, [to start installation](images/setup-win98.png)
   - type "d:\setup" the press enter to begin
   - [proceed with installation](images/setup-win98-02.png)
   - the system auto detects hardwares, installs drivers, and may reboot during the process
3. the above setup steps are done, you MUST save the completed Windows 98 image to your local disk, to re-use it
   - [DO shutdown Windows98](images/shutdown-win98.png), this ensures all data will be saved to browser cache, next,
   - [export the hard disk image](images/save-win98-harddisk.png)
   - the image (hdd.img) should be downloaded to local DOWNLOADS folder
   - you can try the image: exit the current session, then drag the image file to start your own Windows

for more usage instructions, see [here](https://github.com/nbarkhina/DosWasmX) or the [online manual](https://nbarkhina.github.io/DosWasmX/) 
- you can always install a new OS, or use your own disk image
    - you can find a copy of OS at [WinWorld](https://winworldpc.com/product/windows-98/98-second-edition)
    - find more Windows 9x games on [WinWorld](https://winworldpc.com/library/games) and on [archive.org](https://archive.org/details/software)

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
