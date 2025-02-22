# Instruction

The file `test_boot.bin` and `test_no_boot.bin` in this folder are the firmware for those who need to test their board or accessories before formal use. 

**Please don't install the board to your machine if you want to use this test firmware.**

## How to flash

`test_boot.bin` boot address is 0x0810000 , so you need a bootloader to make it work. You can follow the instruction [here](https://github.com/FYSETC/FYSETC-SPIDER/tree/main/bootloader) (in `Upload the bootloader` section) to flash the bootloader before you flash the `test_boot.bin`. And you can follow the instruction [here](https://github.com/FYSETC/FYSETC-SPIDER) to flash the test firmware (in  `Upload the firmware(SDCARD)` and `Upload the firmware(DFU)` section ).

`test_no_boot.bin` is the test firmware which you don't need a bootloader, so follow the instruction [here](https://github.com/FYSETC/FYSETC-SPIDER) to flash the firmware (in`Upload the firmware(DFU)` section，**but remember to change the `Start address` from 0x08010000 to 0x08000000** ).

## How to use

After you flash the test firmware, you need extra parts , list is below. Remember , all these parts are not necessary except `FYSETC mini 12864 v2.1` as the test firmware need  a display to show the test results. For other parts , you only need them when you want to test them.

| Parts you need                                               |
| ------------------------------------------------------------ |
| 8*TMC2130                                                    |
| 9*stepper motors                                             |
| sdcard                                                       |
| FYSETC mini 12864 v2.1                                       |
| 100k thermistor                                              |
| ws2812 RGB strip                                             |
| 24v fans ( You can use 12v fans , but need to change the fan voltage selection jumper) |

After prepare the  parts you need , you need to  jump the jumpers as below shows

<img src="Jumpers.jpg" style="zoom:60%;" />

Then plug in or insert your desire test part to the board , just as this , i just show you the universal set

![](Accessaries.jpg)

Then you can power up the board.

## How will it act

| Parts                  | How it act                                |
| ---------------------- | ----------------------------------------- |
| 8*TMC2130              | Show the status in 12864 : TMC Ok or bad  |
| 9*stepper motors       | Rotate and reverse in loop one by one     |
| sdcard                 | Show the status in 12864 : Card Ok or bad |
| FYSETC mini 12864 v2.1 | Ok : Light up and show status             |
| 100k thermistors       | Show temperatures in 12864                |
| ws2812 RGB strip       | Light up                                  |
| fans                   | Will turn on                              |
| leds in the board      | Will turn on and off in loop              |

![](12864.jpg)