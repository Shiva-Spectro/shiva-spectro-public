# Shiva Spectro

**Shiva - SpectrograpHy Instrumentation Visual Analysis** is a desktop program for amateur astronomical
spectrography. It takes you from the raw images of a spectrograph to a calibrated, corrected and analysed
spectrum, with methods of professional grade.

This repository is the public area: compiled versions, documentation and change log. The source code is kept
in a private repository.

## What Shiva does

- **Calibrate**: loads target, dark, flat and lamp images, stacks them (hot-pixel interpolation, sigma clipping,
  cosmic-ray rejection), follows the spectrum trace, extracts the 1D spectrum and calibrates its wavelength scale
  on a lamp or on known lines.
- **Reduce**: instrumental response from a MILES reference star (or a Pickles template), optional telluric
  correction, dereddening (CCM89) with E(B-V) taken from the CSFD dust map or from the Balmer decrement.
- **Calculate**: sums, differences and ratios of two spectra or of a spectrum and a continuum; cutting,
  smoothing and normalisation.
- **Analyse**: display of several spectra, continua and peaks, line identification, wavelength differences and
  FWHM, line series, spectral classification of stars and diagnostics of planetary nebulae (excitation class,
  electron temperature and density).
- **Simbad** and **Miles** menus: look up the current object in SIMBAD and search the MILES reference stars
  near it (spectral class and magnitude shown).

## Download and installation

Compiled versions are published as **Releases** of this repository (see the *Releases* page, current version
2.1.4):

- `Shiva_V2.1.4_Windows.zip`: unzip, then run `Shiva\Shiva.exe`.
- `Shiva_V2.1.4_Linux.tar.gz`: unpack, then run `Shiva/Shiva`.

Each archive holds the program, the reference libraries and databases (`_Reduction_Instrumentale`: MILES,
Pickles, CSFD dust map, solar spectrum) and the settings file `shiva_config.ini`. No installation of Python is
needed. Keep the folder structure as it is.

`shiva_config.ini` is optional and can be edited with a text editor: default working directory, hiding of the
Pickles frame in Reduce, wavelength limits, Calibrate defaults, telluric bands, folder of the reference
libraries, default radius of the MILES search.

## Documentation

- `doc/Shiva_Guide_utilisateur_2_1_4.docx`: user guide (in French).
- `doc/Shiva_Documentation_Dereddening.docx`: documentation of the dereddening method.
- `doc/Shiva_Documentation_Nebuleuses_Planetaires.docx`: documentation of the planetary nebula analysis (in French).
- `RELEASES.txt`: change log of all versions.

## Credits and data

SIMBAD and the CDS services (Strasbourg), the MILES library (Sanchez-Blazquez et al. 2006; Falcon-Barroso et
al. 2011), the Pickles stellar flux library (Pickles 1998) and the CSFD dust map (Chiang 2023). The complete
references are given in the *About* window of the program.
