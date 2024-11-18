# Zolotarev Low Pass Filter

This lpf filter has been described by Gary Cobb, G3TMG, in QEX (November-December 2016). 

Based on this model, Kjell LA2NI designed a complete low-pass filter, capable of handling (at least) 600W of RF power. 

It's the ideal companion for the Munin400 linear amplifier designed by the same author.

This repository is a strict copy of the original work, using Kicad 8.xx. Original pcb design was made with Ultiboard software

![LPF vu de dessus](https://github.com/F6ITU/k_zolotarev/blob/main/documentation/lpf_up.png)

![LPF vu de dessous](https://github.com/F6ITU/k_zolotarev/blob/main/documentation/lpf_dwn.png)

# Building notes : 

** All capacitors used in the active part of the filter have been sourced as "Vishay Vitramon VJ Hifreq" in 1111 format./**

For   safety reasons and voltage/power handling, the operating voltage of each capacitor should not be less than 1kV.

In other words, since the voltage withstand of MLCC capacitors (or any other technology) decreases as the capacitance increases, the maximum value of each component must not exceed 180 pF (beyond this value, the voltage withstand
resistance collapses at 630 V).

This is why parallel capacitor associations have been provided on the pcb (referenced with the suffix Cxxb1, Cxxb2 etc).

** Two kind of output are available.

- One on SMA connectors

- The other by soldering a coaxial cable directly to the pcb (pigtail input/output)

The second method is preferable, as it's more practical for many hobbyists. However, at these frequencies (1 to 60 MHz), SMA connectors support these power levels perfectly. Avoid connectors made in China.

Input and output wiring on 5mm coax such as RG233 or equivalent (or hand formable SM141 coax cable if SMA are used).

Toroid should be wound with 6 to 8 tenths of a mm wire, air-cores with 8/10 silver-plated wire.


# Work in progress ?

The current state of the filter is considered as "RTM", Beta 1, and considered as "almost definitive" for a first version.
