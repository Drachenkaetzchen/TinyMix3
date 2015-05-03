# TinyMix3

TinyMix3 is a very small, 3 channel stereo audio mixer for your pocket. It features touch and USB control and is meant
to be powered by USB. 

## Features

- Very low power consumption (<50mA). Can be powered by an USB Power Bank
- USB powered
- Touch control
- USB control (presented as serial interface to the host)

## Purpose

You can use TinyMix3 to:

- Automate 3 channel stereo mixing
- Mix 3 stereo channels on the go, ideal for musicians who don't want to carry around bulky mixers

## Usage

Manual mixing

- Connect your inputs and your output
- Touch the "CH" button to switch between the three input channels. The selected channel is indicated via the LEDs.
- After a second, TinyMix3 indicates the volume for the selected channel
- You can then use the + and - touch buttons to adjust the volume
- After 10 seconds, the LEDs turn off to save power

Automatic mixing

- Connect to the TinyMix3 using a serial terminal
- TBD: Which commands the TinyMix3 supports

## Design

Heart of the TinyMix3 is the TDA7448. It is a 6 channel mono / 3 channel stereo mixer controlled via I²C. For combining
the 3 stereo channels into a single stereo output, the TS912 rail-to-rail OpAmp is used. The main logic is implemented
using an Atmega8, which uses V-USB to provide USB control. It also implements the touch interface and controls the LEDs
on the front panel.