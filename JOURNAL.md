# September 14: Planning

I was bored waiting for the parts to arrive for my flight controller so I started browsing Oshwlab looking for cool projects and I kept seeing a bunch of devboards, but the thing is that they are all specialized in one chip. After my 2 neurons grasped that fact, I came to realiz that I had nver seen a multi-devboard. They were all specialized boards for on chip but there wasnt one for a wide range of chips so I decided to change that.

I brainstormeda coolname for the project and the gneral form of the board. Originally I wanted it to becalled "Biblically Accurate devboard" but i didn't really ahv the mans to make it "3D" so I decided to us another name. taking in spiration frmo mythology like always, i decided n the name odin bcaue he'san all-knowwldgbl god that sacrificed an eye (this devboard) for knowledge, so itkinda fits lol.

Nowcoms the fun part of selecting the number an typ of chips on the board.

- STM32H743VGT6
- ESP32-WROOM-32E-N8
- RP2350A
- LFE5U-85F-7BG381I (I <3 FPGA)
- nRF5340
- ATmega328P (Arduino :0 )
- CH32V003 (Open ISA)
- ~K230 (OTG AI Slop!)~
- PIC18F4550
- 74Cxx gates (Gatekeeper)

Refrence Designs:

K230: https://www.kendryte.com/k230/zh/dev/00_hardware/K230_%E7%A1%AC%E4%BB%B6%E8%AE%BE%E8%AE%A1%E6%8C%87%E5%8D%97.html

RP2350: https://pro.easyeda.com/editor#id=a0a21c97b13d436db5579fc2a8b1625d,tab=*78ac95f57945486786729856f79f6ff5@a0a21c97b13d436db5579fc2a8b1625d|288080837e584f0cb80729859f7b9f1c@a0a21c97b13d436db5579fc2a8b1625d

ATmega: https://www.arduino.cc/en/uploads/Main/Arduino_Nano-Rev3.2-SCH.pdf

I started by finding a USB Hub that has 7 ports to connect up all the chips n then i started with the stm nd esp32, then i finished the raspberry pi looking at a reference design by jlcpcb.

# September 15: More Schematic Design

i started working on the other fchips design, more specifically the CH32v003, I was looking about how to connct it to usb c and foun an open source repo that bitbangs 2 pins to create a usb interface to program it: https://github.com/cnlohr/rv003usb.

After wiring that up i finished with the atmega and then started working on the fpga. I had no idea how to connect an fpga beforehand but i saw cheyao's icepi so I at least had a reference design for the hmi and usbc ports https://github.com/cheyao/icepi-zero. I still got stuck as I had to plan out everythign looking at both the footprint, the reference schematic, and also a sheets that lists out every pin from both fpgas that I made.

it was mentally straining a i was feeling burntout so I went to sleep

# September 16: Finished FPGA and start of K230

I finally finished the fpga and the nRF chip (still need to ad headers on all of the chips) and then ecided to start on the k230 as It is a machien elarning chip and I kinda wanted this board to be super powerful.

Aftr a while looking into the documentation I ecided to scrap the k230 for tim pirpouses and also bcause it was too complicated in the current timeframe so I opted for something retro to learn ho to write asembly: PIC18F4550
