---
title: PCB design
publishDate: 2020-03-02 00:00:00
img: /assets/carrier-front.jpg
img_alt: The Front of a custom pcb
description: |
  Full cycle development of a custom PCB and firmware
tags:
  - Design
  - Dev
  - KiCad
  - Rust
  - Embedded

---
 I designed, programmed, got manufactured and distributed an entirely custom PCB. This board is designed to act as a communication bus manager and un-iterupptable power supply for common single board Linux computers (RasberryPi, NVDIA Jetson, ect).

This project was designed to allow for the use of a single board computer (or Coprocessor) on a competition robot for the VEX University Robotics Compention and the VEX AI Robotics Competion. Natively the system only supports connection over micro USB with limited power and data transfer rates. This created a non-ideal setup that was prone to failure. My product streamlined this, allowing 5X higher baud communication, and is rated for higher powersuppuly capabilities, which allows the coprocessor to operate unthrottled. This board also allows for the connection of a secondary, external power source to use as a backup, to protect from brown outs in the uptime critical enviroment presented by our competition.

I also developed the complete firmware for this board, found open 
source on my gitlab: [here](https://gitlab.com/qvex/coprocessor-interface-firmware). This firmware is written in 100% Rust using the RTIC concurrency framework. 

![Back of board](/assets/carrier-back.jpg)

![Screenshot of the layout editor](/assets/carrier-layout.png)
![Screenshot of a render of the board](/assets/carrier-render.png)