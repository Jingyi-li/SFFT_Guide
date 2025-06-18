# System
Ubuntu 22.04; gcc 11.4.0
SFFT requires to install FFTW previously
# FFTW
Download [FFTW3](https://www.fftw.org/download.html).  
Install fowllow the [installation guide](https://www.fftw.org/fftw2_doc/fftw_6.html)  
**-lfftw3f**  
```<bash>
./configure --enable-float  
make  
sudo make install
```
**-lfftw3**
```<bash>
./configure
make  
sudo make install
```
# GNUplot Install
```<bash>
conda install -c conda-forge gnuplot
```
*Current cannot work!*

# Compile SFFT
Download the [Code](https://groups.csail.mit.edu/netmit/sFFT/code.html)
Need to adjust the fft.h fftw.cc and other files for current version  
The adjusted files are in [here](https://github.com/Jingyi-li/SFFT_Guide/blob/main/sFFT-1.0-2.0_new.zip)  
```<bash>
make all
```

# Test
```<bash>
./experiment -N 65536 -K 50 -B 4 -E 2 -M 128 -m 6 -L 10 -l 4 -r 2 -t 1e-8 -e 1e-8
```
