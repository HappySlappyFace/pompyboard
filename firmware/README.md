# PompyBoard Firmware

## Must read

## Setting up

1. [Setup STM32CubeIde](https://www.st.com/en/development-tools/stm32cubeide.html)
2. Login to MyST in STM32CubeIde because it will download libraries/dev tools: Help -> STM32Cube -> Connection to MyST
3. open the workspace under Firmware/PompyBoard/PompyBoard ( i think lmfao, i hate eclipse )
4. if everything is fine you should see in the hierarchy the folders Binaries, Includes, Core, Drivers, Debug 
5. Run with middle green button lol

## Viewing Live Values in STM32CubeIDE

1. Start a **Debug** session (`F11` or 🐞 icon).
2. Go to: Window → Show View → Live Expressions
3. Click **“+”** and add:
sm_centerX
sm_centerY
4. Click the ⚡ **(Enable Live Expressions)** icon.
5. Press **Resume (F8)** — the values will update in real time.



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
