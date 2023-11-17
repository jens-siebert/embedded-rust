# embedded-rust

Code for Blinky example from the Embedded Rust talk given at the IoT Hessen Meetup (Kassel and Frankfurt).

## Requirements

- Raspberry Pi Pico (https://www.raspberrypi.com/products/raspberry-pi-pico)
- Rust Installation (https://www.rust-lang.org/learn/get-started)

## Getting started

- Clone this repo.
- Install thumbv6m-none-eabi target for the Rust compiler: ```cargo target add thumbv6m-none-eabi```.
- Install elf2uf2 runner: ```cargo install elf2uf2-rs```

## Run the program

- Connect the Raspberry Pi Pico to your computer using a USB cable. Press the BOOTSEL button on the Pico while connecting. The Raspberry Pi Pico shall be recognized as a external mass storage device by your operating system.
- In the project directory run ```cargo run --release``` to build the program and deploy it to the Raspberry Pi Pico automatically using ```elf2uf2```. The Pico should be reset automatically after the deploment finished sucessfully and the green LED should start to blink.
