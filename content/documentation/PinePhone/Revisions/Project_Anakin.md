---
title: "Project Anakin"
draft: false
menu:
  docs:
    title:
    parent: "PinePhone/Revisions"
    identifier: "PinePhone/Revisions/Project_Anakin"
    weight:
aliases:
  - /wiki/Project_Anakin
---

## The Project "Anakin" - Phase 1 of PINE64 Smartphone "PinePhone" Development Kit

Project Anakin is a marsh-up kit for the PINE64 Smartphone dubbed "PinePhone". It is used in the early stages of development as a starting point for affiliated projects.

PinePhone development has been broken down into three distinct phases:

* First phase - Project Anakin
* Second phase - purpose-built development kit code named "Don’t be evil". It will be introduced at FOSDEM 2019
* Lastly, the third phase which is the PinePhone itself - scheduled to be released in Q3 2019 (pending on software development).

The Anakin kit consists of following components:

* SoPine Module
* SoPine Model A baseboard
* Pine A64 Wifi/BT module
* 16GB eMMC module
* 5 Mega Piixel CMOS Camera Sensor
* 7" Touch Screen LCD Panel
* Playbox Enclosure
* Lithium Ion Battery case (note: battery not included, can accommodate 1-3 pieces of 18650 size Lithium Ion batter. In general, one is good enough)
* Quectel EC20 R2.1 LTE Module (note: The SIM tray design not distinguish polarity well and all reverse slot in)

{{< figure src="/documentation/images/Anakin_kit_1.jpg" >}}
{{< figure src="/documentation/images/Anakin_kit_2.jpg" >}}
{{< figure src="/documentation/images/Anakin_kit_4.jpg" >}}
{{< figure src="/documentation/images/Anakin_kit_3.jpg" >}}

## Accessories Step-by-Step Guides

Under ['Guides for PINE A64(+) accessories'](/documentation/Accessories/Accessories_Step_by_Step_Guides) you can find instructions and guides concerning:

* Playbox Enclosure
* Bluetooth and WiFi module
* 7" Touch Screen LCD Panel

## SoC and Memory Specification

* Based on Allwinner A64/R18
* R18 and A64 are identical SoC but R18 committed for 10 years supply by vendor.

### CPU Architecture

* [Quad-core ARM Cortex-A53 Processor@1152Mhz](https://www.arm.com/products/processors/cortex-a/cortex-a53-processor.php)
* A power-efficient ARM v8 architecture
* 64 and 32bit execution states for scalable high performance
* Support NEON Advanced SIMD (Single Instruction Multiple Data) instruction for acceleration of media and signal processing function
* Support Large Physical Address Extensions(LPAE)
* VFPv4 Floating Point Unit
* 32KB L1 Instruction cache and 32KB L1 Data cache
* 512KB L2 cache

### GPU Architecture

* [ARM Mali400MP2 Dual-core GPU](https://www.arm.com/products/multimedia/mali-gpu/ultra-low-power/mali-400.php)
* Support OpenGL ES 2.0 and OpenVG 1.1 standard

### System Memory

* RAM Memory Variants: 2GB LPDDR3.
* Storage Memory: SPI Flash and optional eMMC module from 16GB up to 64GB

## Project Anakin, SOPine Module and Baseboard Information, Schematics, and Certifications

* Model "A" Baseoard Dimensions: 133mm x 80mm x 19mm
* Input Power: DC 5V @ 2A, 3.7V Li-Ion battery connector, 3.5OD/1.35ID Barrel DC Jack connector, Euler connector
* [PINE A64 Connector Layout @courtesy of norm24](https://wiki.pine64.org/images/7/7d/Pine64_Board_Connector.png)
* [PINE A64 Connector List](https://wiki.pine64.org/images/d/da/Pine64_Connector.JPG)
* [SOPine Module Pin Assignment ver 1.0](https://files.pine64.org/doc/SOPINE-A64/SOPINE-A64-Pin-Assignments-ver-1.0.pdf)
* [PINE A64 Pi-2/Eular/Ext Bus/Wifi Bus Connector Pin Assignment (Updated 15/Feb/2016)](https://files.pine64.org/doc/Pine%20A64%20Schematic/Pine%20A64%20Pin%20Assignment%20160119.pdf)
* [Good documentation about PINE A64, A64+, and A64-LTS GPIO pins article](https://synfare.com/599N105E/hwdocs/pine64/index.html)

SOPine Module Schematic:

* [SOPine Module Schematic](https://files.pine64.org/doc/SOPINE-A64/SOPINE-A64-Schematic-ver-0.9.pdf)

SOPine Model "A" Baseboard Schematic and PCB Board Resource:

* **SOPine model "A" Baseboard is an hardware open source project but is not "OSH" compliant**
* [SOPine Model "A" Baseboard Schematic capture Rev B DSN source file](https://files.pine64.org/doc/SOPINE-A64/SOPine%20Baseboard%20Model%20A%20Rev%20B20170207.DSN)
* [SOPine Model "A" Baseboard Schematic Rev B PDF file](https://files.pine64.org/doc/SOPINE-A64/SOPine%20Baseboard%20Model%20A%20Rev%20B20170207.pdf)
* [SOPine Model "A" Baseboard PCB Job source file](https://files.pine64.org/doc/SOPINE-A64/SOPine%20Model%20A%20baseboard%20PCB%20layout%20PCB%20Job.tar)
* [SOPine Model "A" Baseboard PCB Gerber file](https://files.pine64.org/doc/SOPINE-A64/SOPine%20Model%20A%20basedboard%20GERBER.tar)
* [SOPine Model "A" Baseboard PCB Layout PDF file](https://files.pine64.org/doc/SOPINE-A64/SOPine%20Model%20A%20baseboard%20PCB%20layout%20PDF.tar)

SOPine (together with model "A" baseboard) Certification:

* [SOPine with model "A" baseboard FCC Certificate](https://files.pine64.org/doc/cert/SOPine%20FCC%20certification%20VOC20170428.pdf)
* [SOPine with model "A" baseboard CE Certificate](https://files.pine64.org/doc/cert/SOPine%20CE%20certification%20VOC20170428.pdf)
* [SOPine with model "A" baseboard RoHS Certificate](https://files.pine64.org/doc/cert/SOPine%20ROHS%20certification%20VOC20170322.pdf)

### Datasheets for Components and Peripherals

Allwinner A64/R18 SoC information:

* **R18 and A64 are identical SoC but R18 committed for 10 years supply by vendor.**
* [Allwinner A64 SoC Brief Introduction](https://files.pine64.org/doc/datasheet/pine64/A64%20brief%20v1.0%2020150323.pdf)
* [Allwinner R18 SoC Brief Introduction](https://files.pine64.org/doc/datasheet/pine64/Allwinner-R18-Brief%20Sheet.pdf)
* [Allwinner A64/R18 SoC Data Sheet V1.1 (Official Released Version)](https://files.pine64.org/doc/datasheet/pine64/A64_Datasheet_V1.1.pdf)
* [Allwinner A64/R18 SoC User Manual V1.0 (Official Release Version)](https://files.pine64.org/doc/datasheet/pine64/Allwinner_A64_User_Manual_V1.0.pdf)

X-Powers AXP803 PMU (Power Management Unit) information:

* [AXP803 PMIC Datasheet](https://files.pine64.org/doc/datasheet/pine64/AXP803_Datasheet_V1.0.pdf)

LPDDR3 information:

* [Allwinner LPDDR3 Datasheet](https://files.pine64.org/doc/datasheet/pine64/AWL3A1632_mobile_lpddr3_1600Mbps.pdf)
* [Foresee LPDDR3 Datasheet](https://files.pine64.org/doc/datasheet/pine64/FORESEE%20178ball%2012x11.5%20LPDDR3%2016G%20Spec%20V1.0-1228.pdf)
* [Samsung LPDDR3 Datasheet](https://files.pine64.org/doc/datasheet/pine64/K4E6E304EE-EGCE.pdf)
* [Hynix LPDDR3 Datasheet](https://files.pine64.org/doc/datasheet/pine64/LPDDR3%20178ball%208Gb_H9CCNNN8JTALAR_Rev1.0.pdf)

eMMC information:

* [PINE64 eMMC module schematic](https://files.pine64.org/doc/rock64/PINE64_eMMC_Module_20170719.pdf)
* [PINE64 USB adapter for eMMC module V2 schematic](https://files.pine64.org/doc/rock64/usb%20emmc%20module%20adapter%20v2.pdf)
* [PINE64 USB adapter for eMMC module PCB in JPEG](https://files.pine64.org/doc/rock64/USB%20adapter%20for%20eMMC%20module%20PCB.tar)
* [SanDisk eMMC Datasheet](https://files.pine64.org/doc/datasheet/pine64/SDINADF4-16-128GB-H%20data%20sheet%20v1.13.pdf)
* [Hynix eMMC Datasheet](https://files.pine64.org/doc/datasheet/pine64/H26M64003DQR%20Datasheet.pdf)
* [Foresee eMMC Datasheet](https://files.pine64.org/doc/datasheet/pine64/FORESEE_eMMC_NCEMBSF9-xxG%20SPEC%20A0%2020150730.pdf)

SPI NOR Flash information:

* [WinBond 128Mb SPI Flash Datasheet](https://files.pine64.org/doc/datasheet/pine64/w25q128jv%20spi%20revc%2011162016.pdf)
* [GigaDevice 128Mb SPI Flash Datasheet](https://files.pine64.org/doc/datasheet/pine64/GD25Q128C-Rev2.5.pdf)

### Project Anakin module/component related information

5MPixel Rear CMOS Camera module information:

* [PINE64 YL-PINE64-4EC 5M Pixel CMOS Image Sensor Module (Description in Chinese)](https://files.pine64.org/doc/datasheet/pine64/YL-PINE64-4EC.pdf)
* [S5K4EC 5MP CMOS Image Sensor SoC Module Datasheet](https://files.pine64.org/doc/datasheet/pine64/S5K4EC%205M%208%205X8%205%20PLCC%20%20Data%20Sheet_V1.0.pdf)
* [S5K4EC 5MP CMOS Image Sensor SoC Chip Datasheet](https://files.pine64.org/doc/datasheet/pine64/S5K4ECGX_EVT1_DataSheet_R005_20100816.pdf)
* [S5K4EC 5MP CMOS Image Sensor Driver Source Code in C language](https://files.pine64.org/doc/datasheet/pine64/s5k4ec.c)

LCD Touch Screen Panel information:

* [7.0" 1200x600 TFT-LCD Panel Specification](https://files.pine64.org/doc/datasheet/pine64/FY07024DI26A30-D_feiyang_LCD_panel.pdf)
* [Touch Panel Specification](https://files.pine64.org/doc/datasheet/pine64/HK70DR2459-PG-V01.pdf)
* [GOODiX GT911 5-Point Capacitive Touch Controller Datasheet](https://files.pine64.org/doc/datasheet/pine64/GT911%20Capacitive%20Touch%20Controller%20Datasheet.pdf)

Ethernet PHY information:

* [Realtek RTL8211 10/100/1000M Ethernet Transceiver for PINE A64+ Board](https://files.pine64.org/doc/datasheet/pine64/rtl8211e(g)-vb(vl)-cg_datasheet_1.6.pdf)
* [Realtek RTL8201 10/100M Ethernet Transceiver for PINE A64 Board](https://files.pine64.org/doc/datasheet/pine64/rtl8201cp.pdf)

Wifi/BT module information:

* [Realtek RTL8723BS WiFi with BT SDIO](https://files.pine64.org/doc/datasheet/pine64/RTL8723BS.pdf)

Enclosure information:

* [Playbox Enclosure 3D file](https://files.pine64.org/doc/datasheet/case/playbox_enclosure_20160426.stp)

Connector information:

* [2.0mm PH Type connector specification use in Lithium Battery (VBAT) port and RTC Battery port](https://files.pine64.org/doc/datasheet/pine64/ePH.pdf)
* [0.5mm Pitch cover type FPC connector specification use in DSI port, TP port and CSI port](https://files.pine64.org/doc/datasheet/pine64/0.5FPC%20Front%20Open%20Connector%20H=1.5.pdf)

{{< figure src="/documentation/images/QUECTEL_EC20_Dongle-small.jpg" caption="right" >}}

LTE module information:

* Note: The current Project Anakin kit deploy on using Quectel EC20_R2.1 which belongs to EC25 family. Actual production will use EC25 and EG25-G (still preliminary) module pending on region.
* [Quectel EC20 R2.1 LTE Module Specification](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EC20_R2.1_LTE_Specification_V1.1.pdf)
* [Quectel EC25 LTE Module Specification](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EC25_LTE_Specification_V1.4.pdf)
* [Quectel EG25-G LTE Module Specification](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EG25-G_LTE_Specification_V1.1_Preliminary_20180522%20(002).pdf)
* [Quectel EC25 LTE Module AT Cammands Set Manual](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EC25&EC21_QuecCell_AT_Commands_Manual_V1.1.pdf)
* [Quectel EC25 LTE Module Hardware Design Guide](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EC25_Hardware_Design_V1.3.pdf)
* [Quectel EC25 LTE Module Reference Design Guide](https://files.pine64.org/doc/datasheet/project_anakin/LTE_module/Quectel_EC25_Reference_Design_Rev.D_20161111.pdf)

## Other Resources

* [Linux Sunxi Wiki page on PINE A64](https://linux-sunxi.org/Pine64#Manufacturer_images)
* [Linux Image created by Andre Przywara](https://github.com/apritzel/pine64)
* [PINE64 Linux build scripts, tools and instructions by Longsleep](https://github.com/longsleep/build-pine64-image)
* [PINE64 Linux image by Longsleep](https://www.stdin.xyz/downloads/people/longsleep/pine64-images/)
* [Shrinking images on Linux by FrozenCow](https://softwarebakery.com/shrinking-images-on-linux)
* [Quectel EC-25 LTE module open source information](https://osmocom.org/projects/quectel-modems/wiki/EC25/24)
