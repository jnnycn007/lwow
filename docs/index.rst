LwOW |version| documentation
============================

Welcome to the documentation for version |version|.

LwOW is a lightweight, platform independent library for Onewire protocol for embedded systems.
Its primary focus is UART hardware for physical communication for sensors and other slaves.

.. image:: static/images/logo.svg
    :align: center

.. rst-class:: center
.. rst-class:: index_links

    :ref:`download_library` :ref:`getting_started` `Open Github <https://github.com/MaJerle/lwow>`_ `Donate <https://paypal.me/tilz0R>`_

Features
^^^^^^^^

* Written in C (C11), compatible with ``stdint.h`` data types
* Platform independent, uses custom low-level layer for device drivers
* 1-Wire protocol fits UART specifications at ``9600`` and ``115200`` baud
* Allows standard one-wire single-gpio manual control (when UART peripherals are not available on the system)
* Hardware is responsible for timing characteristics
  * Allows DMA to offload CPU
* Native driver for DS18x20 family of temperature sensors (DS18B20 and DS18S20)
  * Configurable sensor resolution from ``9`` to ``12`` bits, with conversion-time helper
  * Alarm temperature set/get and dedicated alarm search command
* API for device scan, reading and writing single bits
  * Bulk device search into an array or through a search callback function
* Public CRC-8 helper function for custom protocol needs
* Compatible with an operating system, since hardware handles the timing
  * Separate thread-safe API is available
  * Ships with CMSIS-OS, pthread, ThreadX and Win32 system ports
* User friendly MIT license

Requirements
^^^^^^^^^^^^

* C compiler
* Platform dependent drivers
* Few *kB* of non-volatile memory

Contribute
^^^^^^^^^^

Fresh contributions are always welcome. Simple instructions to proceed:

#. Fork Github repository
#. Respect `C style & coding rules <https://github.com/MaJerle/c-code-style>`_ used by the library
#. Create a pull request to ``develop`` branch with new features or bug fixes

Alternatively you may:

#. Report a bug
#. Ask for a feature request

License
^^^^^^^

.. literalinclude:: ../LICENSE

Table of contents
^^^^^^^^^^^^^^^^^

.. toctree::
    :maxdepth: 2
    :caption: Contents

    self
    get-started/index
    user-manual/index
    api-reference/index
    examples/index
    changelog/index
    authors/index

.. toctree::
    :maxdepth: 2
    :caption: Other projects
    :hidden:

    LwBTN - Button manager <https://github.com/MaJerle/lwbtn>
    LwDTC - DateTimeCron <https://github.com/MaJerle/lwdtc>
    LwESP - ESP-AT library <https://github.com/MaJerle/lwesp>
    LwEVT - Event manager <https://github.com/MaJerle/lwevt>
    LwGPS - GPS NMEA parser <https://github.com/MaJerle/lwgps>
    LwCELL - Cellular modem host AT library <https://github.com/MaJerle/lwcell>
    LwJSON - JSON parser <https://github.com/MaJerle/lwjson>
    LwMEM - Memory manager <https://github.com/MaJerle/lwmem>
    LwOW - OneWire with UART <https://github.com/MaJerle/lwow>
    LwPKT - Packet protocol <https://github.com/MaJerle/lwpkt>
    LwPRINTF - Printf <https://github.com/MaJerle/lwprintf>
    LwRB - Ring buffer <https://github.com/MaJerle/lwrb>
    LwSHELL - Shell <https://github.com/MaJerle/lwshell>
    LwUTIL - Utility functions <https://github.com/MaJerle/lwutil>
    LwWDG - RTOS task watchdog <https://github.com/MaJerle/lwwdg>
