# VOYAGER - A multi-stage Phase Shifter Eurorack module with CV for Stage and Feedback Loop Output Selection
This is a further development of one of my previous DIY projects for a [multi-stage phase shifter](https://github.com/TOILmodular/EurorackMultiStagePhaser).
The module offers a maximum number of 12 stages and several new control options, compared to the previous phaser.
However, it does not contain an internal modulation LFO anymore.
All frequency modulation needs to be provided from an external source.

<img height="500" src="https://github.com/user-attachments/assets/01446d95-0473-4d3b-b9a3-5225ded7acb2">
<img height="500" src="https://github.com/user-attachments/assets/69f20e1e-3432-4cd4-86a8-18f73488306c">

<img height="500" src="https://github.com/user-attachments/assets/e342242c-a15f-4865-82d4-7563d7c1b870">
<img height="500" src="https://github.com/user-attachments/assets/7032556f-7f79-4f03-a0fc-292b786f10b7">

## Features
- Multi-stage phase shifter module with selectable number of stages (up to 12 stages)
- Manual and voltage control over the stage output
- Manual and voltage control over the stage output into the feedback loop
- Manual selection of the fundamental frequency for the phase shift
- LED indicator for selected output stage and feedback loop output stage
- CV input for frequency modulation
- Manual depth control over the modulation strength
- Manual strength control over the feedback loop
- Two inputs with separate attenuators
- Different CV inputs for the phase shift (linear with attenuator, exponential, CV offset)
- Two outputs for mixed original/phase-shifted signals and mixed original/feedback-looped signals
- Module size 18HP

The general signal flow within the module is displayed in the following graph.

![VOYAGER Signal Flow](https://github.com/user-attachments/assets/0fa06d11-05c6-4cdd-8876-95d843c8085e)

A demo of the module is shown in the following YouTube video.

[<img width="500" src="https://github.com/user-attachments/assets/9066ff24-57cc-4a4d-a237-4a95bf5e229d">](https://youtu.be/96xOC4ow6FU)

## Stage Selection and CV
If no cable is plugged into the "STAGES" input, the output stage of the phase shifter can be selected manually by the "STAGES" knob.
The active stage output is made visible via the corresponding LED.
With a cable plugged in, the "STAGES" knob will not have any influence, but the LEDs will still show the selected stage output.

If no cable is plugged into the "FB STAGES" input, the output stage for the feedback loop can be selected manually by the "FB STAGES" knob.
The active stage output is made visible via the corresponding LED.
With a cable plugged in, the "FB STAGES" knob will not have any influence, but the LEDs will still show the selected feedback loop stage output.

The CV ranges for both the "STAGE" and "FB STAGE" inputs are 0V - 5V.
The CV ranges for each of those two CV inputs are roughly as follows:

- Stage 2: 0V - 0.6V
- Stage 4: 0.6V - 1.3V
- Stage 6: 1.3V - 1.9V
- Stage 8: 1.9V - 2.5V
- Stage 9: 2.5V - 3.1V
- Stage 10: 3.1V - 3.8V
- Stage 11: 3.8V - 4.4V
- Stage 12: >4.4V

## Frequency Modulation
The module does not contain any LFO for frequency modulation, common in other phase shifter modules.
The frequency can be modulated either manually via a dedicated knob "FREQUENCY", or via a CV input with a range between 0V and 5V.
If modulated externally, the "FREQUENCY" knob can be used for an offset to the modulation signal, while the "DEPTH" knob serves as an attenuator to the incoming modulation signal

## Module Build and PCBs
I added two different versions for the control board in the folder GerberFiles, an "original", and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

<img width="300" alt="CtrlPCB Orig" src="https://github.com/user-attachments/assets/0468003e-2455-4748-871b-be7dc96b8dae">

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB for the "Thonk" version with footprints for those components.

<img width="300" alt="CtrlPCB Thonk" src="https://github.com/user-attachments/assets/ab000af6-9b38-4eff-b188-9df042dd0723">

The main PCB is the same for both versions.

<img width="300" alt="MainPCB" src="https://github.com/user-attachments/assets/681a8697-4d46-40a9-90c0-b6dcfb4e93a6">

I created the Gerber files with the online tool EasyEDA and ordered the PCBs at JLCPCB.

## Components
The module contains several SMD components:
- TL074 Quad Op Amp IC (x4)
- NJM4580/TL072 Dual Op Amp IC (x2)
- V13700M Dual OTA (x6)
- MMBT3904 NPN Transistor (x2)
- MMBT3906 PNP Transistor (x1)
- 0.1uF capacitor (x36) - used as bypass caps for all ICs

All other components in the module are through-hole.

On the control board, you will find two electrolytic capacitors with rectangles next to them. Since this capacitors are too tall for standing upright on the board with the main board on top of it, they needs to be mounted in a rectangular position. The rectangle shows the position for the bent-over capacitors.

<img width="300" src="https://github.com/user-attachments/assets/e428799b-85bf-47be-8918-2808db317944">
