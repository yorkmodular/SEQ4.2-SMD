## York Modular SEQ4.2 - 4-step CV sequencer with reset

A revamped version of my original 4-step CV sequencer.

Nothing flash here, just a regular sequencer with four steps, a reset input and an output - no muss, no fuss. Plus, it fits behind a 4HP panel.

The obligatory blinkenlights are present and correct, too. Trigger and clock require at least 3V to activate (more is better, within reason)

### Construction notes
The build is fairly straightforward, although there are a couple of things to note:

* **The counter IC should be a CD4017BM or similar **- I've had mixed success with other ICs. *74HC-series ICs should not be used* as their max supply voltage is only 5.5V or thereabouts, which limits their usefulness considerably. The ONSemi HC4017 won't work at all for reasons I've yet to fathom. The ICs I generally use are manufactured by TI and are available from the usual outlets (RS, Farnell et.al.)

* The range of the CV outputs will be determined by the voltage regulator used - assuming that red LEDs are used, there's a total voltage drop of around 2.2V between the output of the 4017 and the final output (~1.6V for the LED, 0.6V for the diode). If you want a range of 5V then I recommend a 7808/7809 regulator - if you use a 7805 (5V) regulator then the final range will be around 3V (ie. 3 octaves). Future revisions of the board may use a variable regulator.

* 100k linear taper pots are recommended for the controls - Alpha pots will give more support to the panel, but anything with a compatible footprint can be used (Alps, Bourns etc.)

### Files

* `seq4-schematic.png` - the module schematic.
* `seq4-panel.dxf` - module panel in AutoCAD DXF format.
* `seq4-panel.fpd` - module panel in Schaeffer FPD format. If you want to customise the panel then use this file and re-export it as a DXF or SVG.
* `seq4-BOM.xlsx` - Bill of Materials (BOM) file.
