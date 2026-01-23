# IntamixX

**IntamixX is a 3-band (high/mid/low) 2-input / 6 output crossover filter available in LV2 and VST3 formats.  It is suitable for integration into audio racks for live sound crossovers, multiband processing and DAWs.
This patch implements the two-frequency, 3-pole Butterworth crossover / filter network butterkreuz3~ from AudioLab that is 3rd-order (18 dB/octave) Butterworth.**

![alt text](https://github.com/intamixx/IntamixX/blob/main/Intamixx.png?raw=true)

All filters are 3rd-order (18 dB/octave) Butterworth, providing:
- flat magnitude response in the passband
- smooth phase behavior
- no ripple

Multiband processing

Crossovers for speakers

Spectral effects

Phase-coherent band splitting

Modular DSP building blocks

Made with Pure Data and Camomile
```
                     ┌───────────────┐
                     │  frequency-1  │
                     └───────┬───────┘
                             │
[inlet~] ──┬─────────────────┼─────────────────┬───────────────
           │                 │                 │
           │                 │                 │
     ┌─────▼─────┐     ┌─────▼─────┐     ┌─────▼─────┐
     │  LP @ f1  │     │  HP @ f1  │     │  HP @ f2  │
     │  3rd BW   │     │  3rd BW   │     │  3rd BW   │
     └─────┬─────┘     └─────┬─────┘     └─────┬─────┘
           │                 │                 │
           │           ┌─────▼─────┐           │
           │           │  LP @ f2  │           │
           │           │  3rd BW   │           │
           │           └─────┬─────┘           │
           │                 │                 │
     ┌─────▼─────┐     ┌─────▼─────┐     ┌─────▼─────┐
     │  LOW OUT  │     │  MID OUT  │     │ HIGH OUT  │
     └───────────┘     └───────────┘     └───────────┘
```
     
     
LOW  → subwoofer
MID  → midrange
HIGH → tweeter
Why this patch is good for it:

Butterworth = smooth, musical slopes

Phase-aligned bands

No harsh resonances


Add gain sliders after each outlet and you’ve built a 3-band isolator EQ.
