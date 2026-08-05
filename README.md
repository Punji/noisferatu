# NOISFERATU / Texture Synth
## Alternative firmware by Punji

Demo video: https://youtube.com/shorts/sy0JyycAC2k?si=m8qY6WxEv8yCJvSo

## Project Overview
Noisferatu is a compact handheld generative texture synthesizer by Phil Schatzmann.

TalkiePCM is a speech synthesis library by Phil Schatzmann that emulates the Texas Instruments TMS5220,
a variant of the chip used in the Speak&Spell toy from 1978.

This alternative firmware for Noisferatu adds a new bank of voices based on TalkiePCM.
Three of the algorithms use a large vocabulary of speech data with over 600 words while the other six algorithms generate random speech frames. 

This project was inspired by the Error Instruments Speak&Glitch box while still trying to fit the Noisferatu style.

### Bank 6: Talkie (9 algorithms)

<br>

| # | Name | Core Technique | pot1 | pot2 |
|---|------|---------------|------|------|
| 1 | Single word | Standard playback | word selection | pitch delta |
| 2 | All words | Time-stretch playback | playback speed | pitch delta |
| 3 | Garbled word | Word frames randomization | word selection | pitch randomization |
| 4 | Voice glitch | Statistical frame generation | silent frame probability | frame repeat probability |
| 5 | Noise glitch | Statistical frame generation | silent frame probability | frame repeat probability |
| 6 | Evolving voice | Single frame mutation | silent frame probability | frame repeat probability |
| 7 | Evolving tape | Multiple frame mutation | silent frame probability | frame repeat probability |
| 8 | Random pitch | Frame pitch randomization | silent frame probability | frame repeat probability |
| 9 | Noise burst | Frame energy randomization | silent frame probability | frame repeat probability |

## Build Instructions
1. Open the firmware folder in Arduino IDE
1. Set the board type to Seeduino XIAO SAMD21
1. Import the TM1637 by Avishay Orpaz and the TalkiePCM by Phil Schatzmann libraries
1. Upload the firmware

Alternatively, upload the **firmware/Noisferatu.ino.bin** file using the Sketch → Upload Using Programmer option.

## Credits

### Noisferatu
Robert Heel 2026 \
https://github.com/rob-scape/noisferatu

### TalkiePCM
Phil Schatzmann 2024 \
https://github.com/pschatzmann/TalkiePCM