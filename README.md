# Quick Starter Guide for RFduino

RFduino: Shrunk down an Arduino to the size of a finger-tip and made it Wireless!

* Get the hardware here: <http://RFduino.com>

## Installation

This installation steps are for Windows systems with Chocolatey packages. If you don't know what Chocolatey is, head over to <http://chocolatey.org> and install it first.

* Install Arduino IDE 1.5.5, Git

Open a Command Shell and type in following commands

    cinst arduinoide -Version 1.5.5-beta -Pre
    cinst git.commandline

* Install the RFduino libraries

Then open a command prompt with **privileged rights (Run as administator)** and install the RFduino library into the Arduino installation.

    cd /D %ProgramFiles%\Arduino\hardware\arduino
    set PATH=%PATH%;%SystemDrive%\git\cmd
    git clone https://github.com/RFduino/RFduino.git

* Install the FTDI Virtual COM Port USB driver

Head over to <http://www.ftdichip.com/Drivers/VCP.htm> or use the following command to download the setup for XP/Win7:

    wget http://www.ftdichip.com/Drivers/CDM/CDM20830_Setup.exe
    CDM20830_Setup.exe

* Download the RFduino Fritzing Part

If you want to document your work built with RFduino, use this part in Fritzing.

    cinst fritzing -Pre
    cinst wget
    wget http://goddess-gate.com/projects/assets/archives/arduino/rfduino.fzpz


## Compile the first project: LedButton

* Plug in your RFduino into the USB

* Install the RFduino LedBtn app on your iPad3 from the App Store.

* Start Arduino IDE

* Select the RFduino in the menu: **Tools / Boards / RFduino**

* Select the right COM port in the menu: **Tools / Port / COMx**

* Open the example project in the menu: **File / Examples / RFduinoBLE / LedButton**

* Compile and upload the sketch into your RFduino by pressing the **Upload** toolbar button.

* Wire up the following parts on a breadboard. I power the RFduino from the USB shield which is also connected to the breadboard.

![RFduino LedBtn Breadboard](https://raw.github.com/StefanScherer/RFduino-guide/master/images/RFduino_LedBtn_Steckplatine.png)

* Start the RFduino LedBtn app on your iPad, connect to your RFduino and press the button on the breadboard and in the iPad app.

* Enjoy!
