---
parent: Harmony 3 peripheral library application examples for SAM HA1 family
title: DAC waveform generation 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# DAC waveform generation

This example application shows how to use the DAC to generate a 1 KHz Sine or Sawtooth wave with a lookup table.

## Description

This example application shows how to use the DAC Peripheral library to generate a 1 KHz Sine or Sawtooth wave with lookup table. DAC starts conversion on a trigger from a timer period interrupt configured to occur at every 10 microseconds. In this application, the number of the DAC samples in a lookup table is 100.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_sam_ha1) and then click **Clone** button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/dac/dac_wav_gen/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| sam_ha1_xpro.X | MPLABX project for [SAM HA1G16A Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMHA1G16A-XPRO) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| sam_ha1_xpro.X | [SAM HA1G16A Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMHA1G16A-XPRO)
|||

### Setting up [SAM HA1G16A Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMHA1G16A-XPRO)

- Connect an oscilloscope to monitor the DAC pin PA02 (Pin 3 of the EXT1 header)
- Connect the Debug USB port on the board to the computer using a micro USB cable

### Note:
*ATSAMHA1G16A device in SAM HA1G16A Xplained Pro board is not recommended for new design, hence replace the device with ATSAMHA1G16AB device. Connect the supported external debugger to Cortex Debug Port*

## Running the Application

1. Build and Program the application using its IDE
2. Observe a sine wave of 1 KHz frequency on DAC output pins
3. Press switch to toggle the waveform shape from sine wave to sawtooth wave and back
4. Refer to the below table for dac output pin and switch details:

| Board      | DAC output pins | Switch Name |
| ----------------- |-----------|-------------|
| [SAM HA1G16A Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMHA1G16A-XPRO) | PA02 (Pin 3 of the EXT1 header) | SW0 |
||||
