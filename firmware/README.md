# PompyBoard Firmware

## Must read

## Setting up

1. [Setup STM32CubeIde](https://www.st.com/en/development-tools/stm32cubeide.html)
2. Login to MyST in STM32CubeIde because it will download libraries/dev tools: Help -> STM32Cube -> Connection to MyST
3. open the workspace under Firmware/PompyBoard/PompyBoard ( i think lmfao, i hate eclipse ) 

## Commands

### Flash and run

See https://probe.rs/docs/tools/probe-rs/ for more information.

```bash
cargo run --release
```

### List USB devices

```bash
lsusb
```

### Show device descriptor

```bash
lsusb -v -d 1209:02d7 # (vid:pid)
```

### Show HID descriptor

You can use https://eleccelerator.com/usbdescreqparser/ to parse the output.

```bash
usbhid-dump -m 1209:02d7 # (vid:pid)
```
