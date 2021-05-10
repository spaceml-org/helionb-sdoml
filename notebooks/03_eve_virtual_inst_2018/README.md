# A Deep Learning Virtual Instrument for Monitoring EUV Solar Spectral Irradiance

### Introduction

The extreme ultraviolet (EUV) radiation from the Sun is the dominant driver of the Earth’s thermosphere/ionosphere system. During periods of elevated solar activity, enhanced solar EUV driving causes adverse space weather effects. These include communication blackouts, increased aerodynamic drag on satellites in low-earth orbit, and scintillation of Global Navigation Satellite Systems (GNSS) signals. 

To further understand solar activity, and how its variations affect life on Earth, NASA’s Solar Dynamics Observatory was launched in 2010. SDO consists of three main instruments, with two separate instruments monitoring the EUV environment: 

1. The Atmospheric Imaging Assembly (AIA; Lemen et al. 2012) captures 4096 x 4096 resolution images (with 0.6 arcsecond pixel size) of the full Sun in two ultraviolet, seven EUV (centered at 94, 131, 171, 193, 211, 304 and 335 Å), and one visible wavelength.

2. The EUV Variability Experiment (EVE; Woods et al. 2012) monitors the solar EUV spectral irradiance from 1 to 1050 Å. This is done by utilizing multiple EUV Grating Spectrographs (MEGS-A: 60 – 370 Å; MEGS-B: 360 – 1060 Å) which disperse EUV light from the full disk of the Sun and its corona onto a 1024 x 2048 CCD.

Unfortunately, an electrical malfunction of the EVE MEGS-A channel in 2014 compromised our ability to monitor EUV SSI in the 60 – 370 Å wavelength range (which contains roughly 60% of the solar irradiance in the EUV). The goal of this project was to fill this gap in measurement capabilities with a virtual replacement for MEGS-A, based on observations from AIA. This mapping was expected for three main reasons:

1. The same population of plasma is expected to be responsible for emitting the EUV radiation observed by the two instruments.
2. The EUV images taken by AIA (94 – 335 Å) have significant overlap with the spectra measured by MEGS-A (60 – 370 Å).
3. Each of the AIA filters has a different and overlapping response to radiation emitted by plasmas of different temperatures, enabling the use of AIA filters as the basis of a mapping between plasma temperature and irradiance.




### Results:

It was demonstrated that with 4 years’ worth of co-temporal SDO/AIA and SDO/EVE (MEGS-A) data, we were able to create a virtual MEGS-A that will be available as long as AIA is functioning. 

Our approach for nowcasting MEGS-A spectral irradiance measurements from AIA images achieves a median error of 1.6% across MEGS-A lines, outperforming a variety of approaches including a differential emission measure (DEM)-based approach (see SpaceML project DeepEM). In addition to quantitatively characterizing the performance of the method, Figure 1 provides evidence that the model is solving the AIA to MEGS-A mapping in a physically sensible way.

While this project showcases the potential for a new age of virtual instruments, this work would have been impossible without the data taken by the AIA and EVE instruments. Virtual instruments won’t replace the need for their hardware counterparts, but can leverage existing and historic scientific instruments to yield similar levels of scientific data products as hardware missions currently do. Other important examples of this potential include the estimation of photospheric velocities based on continuum images, and the assembly of superresolution magnetograms (see SpaceML Project). 



---

The code repository for this project is available: https://github.com/AlexSzen/sw-irradiance
