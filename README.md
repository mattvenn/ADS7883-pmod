# PMOD 2 x ADS7883 ADC

the ADS7883 is a 12 bit, serial ADC. It can sample up to 3MHz, and can be supplied up to 5v.

It needs 3 pins to operate: clk, select and data.

Supply can be 3.3v from the PMOD (limits maximum range of ADC to 3.3v), or 5v with a 
precision regulator and an external supply between 5.5v and 16v.

Use the ext/pmod jumper to select the source.

![schematic](schematic.pdf)

![board](board.pdf)

# BOM

If you are using PMOD 3.3v for supply, you don't need C7, U1, C5.

LED D1 and R2 are optional for indicating PSU is good.

C1 to C4 are bypass caps and will help to improve noise performance if added.

* ADC1 and 2: ADS7883 http://es.farnell.com/texas-instruments/ads7883sbdbvt/adc-sar-12bit-3msps-6sot23/dp/2082426
* U1: ref5050 http://es.farnell.com/texas-instruments/ref5050aidg4/ref-de-tensi-n-serie-5v-soic-8/dp/1439628

# Verilog Core

[adc.v](adc.v) is tested Verilog for the ADC.
