[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# DAC waveform generation with DMA

This example application shows how to use the DAC with the DMA to generate a 5 KHz sinusoidal waveform without CPU intervention.

## Description

The DAC Peripheral library is used in hardware trigger mode to generate a Sine wave. The TC peripheral is configured to generate a trigger every two microseconds. Trigger is connected to the DAC using the EVSYS peripheral. DMA is used to setup a linked list to transfer sine wave samples from lookup table to the DAC "DATABUF" register. In this application, the number of DAC samples per cycle(0 to 360 degrees sine wave) is 100.

## Downloading and building the application

To download or clone this application from Github, go to the [top level of the repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_sam_ha1) and click

![clone](../../../docs/images/clone.png)

Path of the application within the repository is **apps/dac/dac_wav_gen_dma/firmware** .

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

- Connect an oscilloscope to monitor the DAC pin PA02 (Pin 3 of the EXT1 )
- Connect the Debug USB port on the board to the computer using a micro USB cable

## Running the Application

1. Build and Program the application using its IDE
2. Observe a sine wave of 5 KHz frequency on DAC output pin
3. Refer to the below table for dac output pin details:

| Board      | DACC output pins |
| ----------------- |-----------|
| [SAM HA1G16A Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/PartNO/ATSAMHA1G16A-XPRO) | PA02 (Pin 3 of the EXT1 header) |
|||