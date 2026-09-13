# Lightweight onewire library

LwOW is lightweight, platform independent library for Onewire protocol for embedded systems.
Its primary focus is UART hardware for physical communication for sensors and other slaves.
Alternatively, the separation of the LwOW and low-level system-related part allows direct GPIO in/out toggling, for a simple communication.

More about 1-Wire over UART can be found on link below.

https://www.maximintegrated.com/en/app-notes/index.mvp/id/214

[Open documentation](https://docs.majerle.eu/projects/lwow/)

## Features

* Written in C (C11), compatible with `stdint.h` data types
* Platform independent, uses custom low-level layer for device drivers
* 1-Wire protocol fits UART specifications at `9600` and `115200` baud
* Allows standard one-wire single-gpio manual control (when UART peripherals are not available on the system)
* Hardware is responsible for timing characteristics
    * Allows DMA to offload CPU
* Native driver for DS18x20 family of temperature sensors (DS18B20 and DS18S20)
    * Configurable sensor resolution from `9` to `12` bits, with conversion-time helper
    * Alarm temperature set/get and dedicated alarm search command
* API for device scan, reading and writing single bits
    * Bulk device search into an array or through a search callback function
* Public CRC-8 helper function for custom protocol needs
* Compatible with an operating system, since hardware handles the timing
    * Separate thread-safe API is available
    * Ships with CMSIS-OS, pthread, ThreadX and Win32 system ports
* User friendly MIT license

## Contribute

Fresh contributions are always welcome. Simple instructions to proceed:

1. Fork Github repository
2. Follow [C style & coding rules](https://github.com/MaJerle/c-code-style) and use `clang-format` to format the code
3. Create a pull request to `develop` branch with new features or bug fixes

Alternatively you may:

1. Report a bug
2. Ask for a feature request
