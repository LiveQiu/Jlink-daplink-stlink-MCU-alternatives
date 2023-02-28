# 各种调试器制作方案与MCU选型（Jlink-daplink-stlink）

## 介绍

- 目前表格里的MCU我已经测试过，如果有更多希望测试的国产替代方案，欢迎给我的issues留言，我会尽快测试
- 希望大家可以共享信息，包括自己DIY使用的方案/原理图和可以使用的MCU具体型号和测试过的固件版本，我会将其汇总并更新
- 这个仓库的目的是为了让大家DIY各种调试器的时候减少更换MCU的次数，我在制作的工程中发现一些国产MCU并不能完全兼容STM32，特别是USB部分，是为了给大家提供DIY的参考

## 测试使用的原理图

- Jlink-ob使用的官方最新原理图，主控方案为STM32F103系列，我额外增加了几个esd二极管，测试与MCU功能无关
  - [Jlink-ob 详情页](https://www.segger.com/products/debug-probes/j-link/models/j-link-ob/)
  - [Jlink-ob 原理图-STM32F103](https://www.segger.com/downloads/jlink/UM08023_JLinkOBSTM32F103.pdf)

## 测试使用的PCB

- Jlink-ob STM32F103是我根据官方原理图自己绘制的PCB，超级迷你的二层板调试器，测试使用通过

  <img src="https://raw.githubusercontent.com/LiveQiu/Jlink-daplink-stlink-MCU-alternatives/main/img/jlink-ob-tkmk-top.png" width="250px" />
  <img src="https://raw.githubusercontent.com/LiveQiu/Jlink-daplink-stlink-MCU-alternatives/main/img/jlink-ob-tkmk-bottom.png" width="250px" />

## 参考项目

- [JLink-OB_32f103 立创开源项目-作者LSanor](https://oshwhub.com/LSanor/jlink-ob_32f103)