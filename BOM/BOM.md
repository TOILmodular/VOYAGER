# BOM

| Description | Value | Quantity | |
| --- | --- | --- | --- |
| Resistor 1/4W | 1K | 14 | |
| Resistor 1/4W | 2K | 1 | |
| Resistor 1/4W | 10K | 42 | |
| Resistor 1/4W | 20K | 12 | |
| Resistor 1/4W | 30K | 24 | |
| Resistor 1/4W | 33K | 1 | |
| Resistor 1/4W | 43K | 1 | |
| Resistor 1/4W | 47K | 6 | |
| Resistor 1/4W | 68K | 2 | |
| Resistor 1/4W | 100K | 6 | see footnote *) below |
| Resistor 1/4W | 150K | 1 | |
| Resistor 1/4W | 430K | 1 | |
| Resistor 1/4W | 1M | 2 | |
| Resistor 1/4W | LED | 16 | Limiting resistors for LEDs - value depending on the LED used and the preferred brightness - I used 100K |
| Capacitor Electrolytic | 22uF | 2 | |
| Capacitor Electrolytic | 10uF | 1 | |
| Capacitor Electrolytic | 1uF | 2 | |
| Capacitor Ceramic | 1uF | 2 | |
| Capacitor Ceramic | 0.1uF | 36 | SMD (metric 1608, imperial 0603) |
| Capacitor Ceramic | 4700pF | 12 | |
| Capacitor Ceramic | 100pF | 1 | |
| Capacitor Ceramic | 20pF | 2 | |
| Diode | 1N5819 | 2 | |
| Diode | 1N4148 | 14 | |
| Diode | LED | 16 | 3mm |
| Transistor | MMBT3904 | 2 | SMD (SOT-23) |
| Transistor | MMBT3906 | 1 | SMD (SOT-23) |
| Regulator | LM08L09 | 1 | |
| Regulator | LM09L09 | 1 | |
| Op Amp | TL074 | 4 | SMD (SOP14) |
| Op Amp | TL072 or NJM4580 | 2 | SMD (SOP8) |
| OTA | V13700M | 6 | SMD (SOP16) |
| Quad XOR Gate | CD4030 | 6 | |
| 8-channel Multiplexer | CD4051 | 2 | |
| Potentiometer | B100K | 4 | |
| Potentiometer | B50K | 2 | |
| Potentiometer | B10K | 1 | |
| Mono Jack | 3.5mm | 7 | |
| Header | 2.54mm Male 1x6 | 1 | Connector Main Board |
| Header | 2.54mm Male 1x5 | 2 | Connector Main Board |
| Header | 2.54mm Male 1x6 | 1 | Connector Main Board |
| Header | 2.54mm Male 1x3 | 1 | Connector Main Board |
| Header | 2.54mm Female 1x6 | 1 | Connector Control Board |
| Header | 2.54mm Female 1x5 | 2 | Connector Control Board |
| Header | 2.54mm Female 1x4 | 1 | Connector Control Board |
| Header | 2.54mm Female 1x3 | 1 | Connector Control Board |
| Header | 2.54mm Male 2x5 | 1 | Power Connector |

*)Two resistors with value 100K might have to be replaced by 120K resistors, depending on the module behavior. Those resistors are part of the resistor chains in the two voltage dividers related to the STAGE and FB STAGE selections.
In the schemaitc those two resistors have the numbers R7 and R91. On the silk screen of the main PCB they are labelled with asterisk belind the resistor value 100K (see picture below).
After finishing the module build, turn the knobs STAGE and FB STAGE fully clockwise.
If the last LEDs for stage 12 do not light up, rwplace those two resistors with 120K resistors.

<img width="400" src="https://github.com/user-attachments/assets/5df2db97-c19e-4831-aadc-a91169670d85" />
