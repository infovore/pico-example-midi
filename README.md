# Raspberry Pi Pico: MIDI demo.

This is [the MIDI example from Tinyusb][tinymidi], tweaked and configured such that it'll compile on a Raspberry Pi Pico out of the box.

It uses a highly similar CMake configuration to the [Raspberry Pi Examples][examples], so should be compilable in a very similar way: I'm just cribbing from the ["Getting started with Raspberry Pi Pico" document][picostart].

When compiled successfully, the Pico will appear as a USB MIDI Device, emitting a stream of note data. You can connect this to a software synthesizer, or view it in a MIDI monitor tool to confirm success.

[tinymidi]: https://github.com/raspberrypi/tinyusb/tree/pico/examples/device/midi_test/src
[examples]: https://github.com/raspberrypi/pico-examples/
[picostart]: https://datasheets.raspberrypi.org/pico/getting-started-with-pico.pdf
