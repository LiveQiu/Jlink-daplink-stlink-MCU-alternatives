# Jlink-daplink-stlink-MCU-alternatives（[中文](/README_zh.md))

## Introduce

- I have tested the MCU in the current table, if there are more domestic alternatives that I hope to test, welcome to leave a message to my issues, I will test as soon as possible
- I hope you can share information, including the scheme/schematic you use in DIY and the specific model of MCU you can use and the firmware version that you have tested, and I will summarize and update it
- The purpose of this repository is to allow everyone to reduce the number of times to replace MCUs when DIY various debuggers, and I found that some MCUs are not fully compatible with STM32, especially the USB part, in order to provide you with DIY reference

## Test schematic

- Jlink-ob uses the official latest schematic, the main control scheme is STM32F103 series, I added a few additional ESD diodes, the test is independent of the MCU function
  - [Jlink-ob Details page](https://www.segger.com/products/debug-probes/j-link/models/j-link-ob/)
  - [Jlink-ob Schematic-STM32F103](https://www.segger.com/downloads/jlink/UM08023_JLinkOBSTM32F103.pdf)

## Test PCB

- Jlink-ob STM32F103 is a PCB that I drew myself according to the official schematic, super mini two-layer board debugger, test use passed

  <img src="https://raw.githubusercontent.com/LiveQiu/Jlink-daplink-stlink-MCU-alternatives/main/img/jlink-ob-tkmk-top.png" width="250px" />
  <img src="https://raw.githubusercontent.com/LiveQiu/Jlink-daplink-stlink-MCU-alternatives/main/img/jlink-ob-tkmk-bottom.png" width="250px" />

## Test MCU

- Jlink-ob STM32F103 test, pay attention to distinguish between C8T6 and CBT6, pay attention to look at the suffix

|      MCU      | Firmware (2009) | Firmware (Latest) | Reason for failure | Software version | Place of purchase |  Price  | Recommend |
| :-----------: | :-------------: | :---------------: | :----------------: | :--------------: | :---------------: | :-----: | :-------: |
| STM32F103C8T6 |      PASS       |       PASS        |                    |      V6.98       | Refurbished chips | 4-5 CNY |     √     |
| AIR32F103CBT6 |      PASS       |       FAIL        |      USB FAIL      |      V6.98       |   Taobao Luatos   | 4.8 CNY |     ×     |
| APM32F103CBT6 |      PASS       |       PASS        |                    |      V6.98       |      Taobao       | 3.5 CNY |     √     |
| APM32F103C8T6 |      PASS       |       FAIL        |      USB FAIL      |      V6.98       |      Taobao       | 3.5 CNY |     ×     |

## TODO

- Jlink-ob STM32F072（Serial Port surport）
- Jlink-ob STM32F103 add TBU6 update
- DAPlink update test
- Jlink update test
- STlink update test

## Designed by ThinkerMaker

- [Thinkermaker Bilibili](https://space.bilibili.com/11945069)
- [Thinkermaker Github](https://github.com/LiveQiu)
- [Thinkermaker website](https://thinkermaker.xyz)

## Reference project

- [JLink-OB_32f103 LC open source project-LSanor](https://oshwhub.com/LSanor/jlink-ob_32f103)