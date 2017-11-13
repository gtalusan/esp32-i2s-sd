# ADMP441 MEMS I2S sample for ESP32

## Breakout Board

Purchased from [OSHPark](https://oshpark.com/shared_projects/ypqAU3CH) via https://github.com/SamEA/ADMP441_Microphone.git

### BOM
![OSHPark](https://raw.githubusercontent.com/SamEA/ADMP441_Microphone/master/ADMP441%20Breakout%20Board%20Top.png)

1. R1 - 100kOhm
2. C1 - 100nF
3. U1 - ADMP441 MEMS desoldered from Amazon Dash

## ESP32

|ADMP441|ESP32|
|-------|-----|
|WS     |IO25 |
|SD     |IO22 |
|SCK    |IO26 |
|VCC    |3.3V |
|GND    |GND  |

Wire SD card to VSPI and CS=21

## Usage

Dumps I2S PCM data to track.i2s on SD card.

Run,

```
ffmpeg -f s32le -ar 16000 -ac 1 -i track.i2s track.wav
```

to convert to a WAV file.  QED.
