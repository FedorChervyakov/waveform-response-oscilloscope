# Automated Frequency Response Measurements of Optical Sensors

This is a LabVIEW Project which uses Keysight's DSOX2014 oscilloscope to perform automated frequency response measurements.
It was developed for an assignment in uni, where the task was to measure and study frequency responses of LDR and photodiode optical sensors.

Unfortunately, I have lost the latest version of this project which included saving the measurements to a report.
Nevertheless, this version does perform oscilloscope configuration, wavegen configuration, and swept measurements and could be easily extended.

## Description

This project is using VIs from [InfiniiVision X-Series Oscilloscope LabVIEW Instrument Drivers] to communicate with the scope.

Code is split in 3 parts:
- Sweep VIs
- Waveform generator VIs
- Main VIs

`Sweep VIs` contain SubVIs used to generate linspace and logspace arrays. VIs located in `Waveform generator VIs` are used to configure
and control oscilloscope's waveform generator. `Square wave response measurements.vi` is the "main" VI in this project.

```
src
├── Init session.vi
├── Optical sensors measurements.aliases
├── Optical sensors measurements.lvlps
├── Optical sensors measurements.lvproj
├── Set average acquisition mode.vi
├── Set timebase horizontal scale.vi
├── Square wave response measurements.vi
├── Sweep VIs
│   ├── Linear sweep (linspace).vi
│   ├── Log sweep.vi
│   └── Sweeps.vi
└── Waveform generator VIs
    ├── Load Impedance.ctl
    ├── Set wavegen DC signal parameters.vi
    ├── Set wavegen PULSe signal parameters.vi
    ├── Set wavegen RAMP signal parameters.vi
    ├── Set wavegen SINe signal parameters.vi
    ├── Set wavegen SQUare signal parameters.vi
    ├── State machine.ctl
    ├── Waveform generator.vi
    ├── Waveform type.ctl
    ├── Wavegen parameters.ctl
    ├── Wavegen set frequency.vi
    └── Wavegen turn on.vi
```




## Prerequisites

**Software Requirements**:
- LabVIEW 2021
- [IO Libraries Suite](https://www.keysight.com/us/en/lib/software-detail/computer-software/io-libraries-suite-downloads-2175637.html)
- [InfiniiVision X-Series Oscilloscope IVI and MATLAB Instrument Drivers](https://www.keysight.com/us/en/lib/software-detail/driver/infiniivision-xseries-oscilloscope-ivi-and-matlab-instrument-drivers-2019021.html).
- [InfiniiVision X-Series Oscilloscope LabVIEW Instrument Drivers](https://www.keysight.com/us/en/lib/software-detail/driver/infiniivision-xseries-oscilloscope-labview-instrument-drivers-2862255.html)
- I also had to install  .NET Framework 3.5
