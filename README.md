`freqcpu` - limit CPU frequency 

## Syntax:

```
freqcpu -c  --> create initial configuration file
freqcpu -d  --> run daemon for set CPU frequency
freqcpu -r  --> set limit CPU frequency
freqcpu -f  --> show current CPU frequency
freqcpu -g  --> show current CPU governor
freqcpu -o  --> show CPU cores
freqcpu -h  --> show help
```

## Configuration:

To create the initial configuration file, you must run the command: 

```
freqcpu -c
```

Then edit the `/etc/freqcpu/freqcpu.conf` file to your own values.

## Example configuration file:

```
cores_cpu=16
freq_min=2000Mhz
freq_max=3600Mhz
governor=powersave
```

## Boot with system:

```
sudo systemctl daemon-reload
sudo systemctl enable freqcpu
```

## How to install:

```
git clone https://github.com/dmesg00/freqcpu
cd freqcpu
sudo make install
```

## How to uninstall:

```
git clone https://github.com/dmesg00/freqcpu
cd freqcpu
sudo make uninstall 
```

## Dependencies
* bash
* cpupower or cpufrequtils
* watch

