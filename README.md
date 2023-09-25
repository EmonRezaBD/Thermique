# Thermique
![GitHub Repo stars](https://img.shields.io/github/stars/EmonRezaBD/Data-Analyzer)![GitHub repo size](https://img.shields.io/github/repo-size/EmonRezaBD/Data-Analyzer?color=red) 
Before Scan            |  After Scan
:-------------------------:|:-------------------------:
![Fig. 1](https://github.com/EmonRezaBD/Thermique/blob/main/BeforeScan.PNG) | ![Fig. 2](https://github.com/EmonRezaBD/Thermique/blob/main/AfterSacn.PNG)
User is waiting for the forehead to detect | Scanning the RFID card and temperature from forehead is showing instantly

This codebase is created for the research purpose. However, materials presented here are introduced for our submission to [ICCA 2022](https://www.aiub.edu/2nd-international-conference-on-computing-advancements---icca-2022) <br>
It is accepted in ICCA 2022 and available in ACM Digital Library. For reading the full article visit here : <code>[https://doi.org/10.1145/3542954.3542978](https://dl.acm.org/doi/abs/10.1145/3542954.3542978)</code>

## Table of Contents 
The repository is organized as follow:
* <code>docs</code>contains few necessary documents
* <code>software</code>contains all the source files for using Lepton module and its interfaces
## Achievements
* It is featured in departmental blog <code>[Read here](https://mist.ac.bd/blog/cse/post/thermique_temperature_detection_using_thermal_image_for_covid_19_screening-149)</code>
* 

## This codebase was cloned from groupgets, and modified for personal necessities.
raspberrypi_video [Edited]

0. This is for raspberrypi_video only. raspberrypi_qt was not used in final production.
1. Enable I2C and SPI
2. Overclock the pi to a minimum of 1100MHz for Pi3. If using Pi4, don't do this.
3. Write the following into /boot/config.txt: [for Pi3 only, skip if using Pi4]

```
over_voltage=4  
sdram_freq=400  
core_freq=400  
gpu_freq=400  
```
4. In /boot/config.txt, make sure hdmi hotplug is set to 1.
5. Keep the module connected to pi using shortest possible wires.
6. DO NOT CONNECT BACKSIDE PINS TO Vcc and GND
7. Use the following to install necessary Qt libraries for compilation:

```
sudo apt-get install qt4-dev-tools
```

8. Finally, compile using:

```
qmake && make
```

8. To clean, use the following:

```
make sdkclean && make distclean
```

9. Since Lepton Module ver3.5 is being used, run the executable with:

```
./raspberrypi_video -tl 3
```

10. Press 'r' on keyboard for FFC reset.

## BibTeX Citation

If you use this article, we would appreciate using the following citations:
```
@inproceedings{reza2022thermique,
  title={Thermique: An Integrated AI-Based Temperature Sensing and Management System to Hold Back COVID-19 Contamination},
  author={Reza, Md Rokonuzzaman and Saleh, Shaqran Bin and Fatema, Tashfia and Hasan, Ishraq and Bin Munir, Muhaimin and Rabbi, Md Fazle},
  booktitle={Proceedings of the 2nd International Conference on Computing Advancements},
  pages={156--164},
  year={2022}
}
```
