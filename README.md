# Vox (Temporary Name)

Word recognition application based on a Weightless Neural Network, WiSARD (Wilkes, Stonham and Aleksander Recognition Device).

## Requirements

Libs: FFTW, libsndfile, PortAudio
```bash
sudo apt-get update
sudo apt-get install libfftw3-3 libfftw3-bin libfftw3-dev libfftw3-double3 libfftw3-long3 libfftw3-quad3 libfftw3-single3 libsndfile1 libsndfile1-dev sndfile-tools libportaudio2
```

## How to Install

```bash
./install.sh
```

## How to Use

```bash
./execute.sh
```

It will ask for the name of a training data file and then actually start the program. To test different sound files just provide their paths. For instance: `realWavs/a1_Guilherme.wav`.

## How to modify parameters

To modify PreProcessing parameters, edit `include/PreProcessing.h`.
To modify WiSARD parameters, search for "WiSARD constructor call" on `src/main.cpp` file. This constructor can be modified according to [libwann github page](https://github.com/firmino/libwann).

After any changes, run the rebuild script: 

```bash
./rebuild.sh
```

## Results

### Temporal Resampling graphs
![Temporal Resampling and Thermometer downscale](https://github.com/FogoDev/voicer/blob/master/results/temporal%20resampling%20and%20thermometer%208%20downscale.png?raw=true)
![Temporal Resampling and Thermometer upscale](https://github.com/FogoDev/voicer/blob/master/results/temporal%20resampling%20and%20thermometer%208%20upscale.png?raw=true)

### Generated waves
![Generated wave with white noise](https://github.com/FogoDev/voicer/blob/master/results/genWAV%20with%20noise%20sample.png?raw=true)

### Treating waves
![Original audio](https://github.com/FogoDev/voicer/blob/master/results/pre%20processing/original%20wav.png?raw=true)
![Windowed audio](https://github.com/FogoDev/voicer/blob/master/results/pre%20processing/windowed.png?raw=true)
![Audio DFT](https://github.com/FogoDev/voicer/blob/master/results/pre%20processing/FFT.png?raw=true)

