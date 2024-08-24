# Vestax-PDX-2000-Phono-Preamp
Integrated phono preamp for Vestax PDX-2000 turntables. Board taps into internal +15V/-15V/GND for power (with 12V regulators for ripple reduction) and is hardwired into the audio path. Designed for moving magnet catridges- specifically Shure M44-7 and Ortofon Mix Concorde Mk II.

<p align='center'>
    <img width=90% alt='Phono preamp on schematic' src='pics/preamp_schematic.jpg'>
</p>

Specs:
* Gain ~42.7dB at 1kHz.
* Loading 47kΩ, 360pF.
* Simulated amplitude within +/-0.05dB of RIAA.
* Actual amplitude within +/-0.5dB of RIAA.
* Left/right channel amplitude within +/-0.22dB.
* Left/right channel phase within +/-0.67°.

The board uses existing PCB screws on board P100 to mount in the chasis. The existing cable on J704 is re-routed to J4, and new wires and an 11-pin JST connector go to J704. The tonearm wires are routed to the input section of the PCB, and new wires connect the output of the amplifier to the original output PCB and RCA jacks.

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='pics/preamp_installed.jpg'>
</p>

Overall performance is very good with minimal deviations from RIAA, simulation, and left/right channels. Note that some plots below use a heavily magnified delta on the right axis.

The [LTSpice simulation](spice/) closely follows the RIAA amplitude curve within +/-0.05dB:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/mag_spice_riaa.png'>
</p>


Simulations with 1% tolerance parts give a max amplitude error of +/-0.15dB:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/spice_mag_montecarlo.png'>
</p>

The actual amplitude error is within +/-0.5dB, with the majority being within +/-0.1dB:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/mag_riaa.png'>
</p>

The frequency response of the left and right channels is closely matched:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/mag_lr.png'>
</p>

The phase is very similar to the simulation:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/phase_spice.png'>
</p>

The phase response of the left and right channels is closely matched:

<p align='center'>
    <img width=90% alt='Phono preamp installed' src='plots/phase_lr.png'>
</p>