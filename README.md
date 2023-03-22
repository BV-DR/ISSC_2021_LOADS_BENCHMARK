# ISSC 2021 - Loads Committee - BENCHMARK


The aim of this benchmark is to better evaluate the capability of current sea-keeping codes to evaluates vertical bending moment, on **extreme waves**, on rigid hulls. Reference results are model tests performed at Ecole Centrale de Nantes ([Experimental analysis of wave-induced vertical bending moment in steep regular waves](https://www.sciencedirect.com/science/article/abs/pii/S0889974622000287))

Benchmark specification can be found below.


## Experimental model

The model is  a 6750 TEU container-ship, at scale 1:65. Geometry can be found in IGES format. (file [input / 6750TEUcontainership-scale1_65-breakwater.igs]()). The hull geometry is the same as the one used in [Benchmark study on motions and loads of a 6750-TEU containership](https://www.sciencedirect.com/science/article/pii/S0029801816300804), and mass properties are very close. 

The geometry here provided corresponds exactly to the model (including protection from green-water for measurement equipment).

<img src="https://github.com/Guillaume4/ISSC_2021_LOADS_BENCHMARK/blob/master/Input/iges_picture.png" alt="IgesImage" width="200"/>  <img src="https://github.com/Guillaume4/ISSC_2021_LOADS_BENCHMARK/blob/master/\Experiments/experiment_illustration.png" alt="waveImage" width="200"/>

All coordinates are here given from aft perpendicular. Aft perpendicular is located 0.09045m forward from the transom.

### Main dimension


|         | Units           | Model  | Full scale |
| ------------- |:-------------:| -----:|-----:|
|Lpp  | m | 4.41 | 286.6|
|Beam | m | 0.615 | 40 |
|Draft | m | 0.1843 | 11.98  |
|Mass | kg | 312.61 | 85849972|
|X_CoG |m | 2.13 | 143.70|
|Y_CoG |m |0.0 | 0.0|
|Z_CoG |m | 0.256 | 16.66|
|R_xx | m |0.18 | 12.0|
|R_yy | m |1.10 | 71.5|
|R_zz | m |1.10 | 71.4|
|R_xz | m |-0.11 | -7.0|

### Mass distribution


Segment | Mass | X_CoG | Y_CoG |Z_CoG|I_xx|I_yy|I_zz|I_xz|X Segment connection|
| ------------- |:-------------:| -----:|:-------------:| -----:|-----:|-----:|-----:|-----:| -----:|
S1|31.749|0.365|0.0|0.265|0.866|1.805|1.819|0.082|0.62755
S2|32.913|0.807|0.0|0.290|1.490|1.474|1.031|-0.237|1.03755
S3|25.975|1.242|0.0|0.185|0.719|0.722|0.871|0.001|1.44755
S4|44.082|1.745|0.0|0.207|1.022|1.490|1.670|-0.150|1.90455
S5|40.669|2.054|0.0|0.214|1.025|1.481|1.658|0.021|2.36155
S6|39.974|2.565|0.0|0.305|1.718|1.557|1.067|-0.017|2.77155
S7|34.666|3.002|0.0|0.305|1.413|1.367|1.019|0.166|3.18155
S8|33.553|3.406|0.0|0.291|1.221|1.273|0.907|0.193|3.59155
S9|29.027|3.919|0.0|0.242|0.567|1.959|1.999|0.039


### Mooring

The vessel is restrain with a soft mooring, which results in a surge natural period of 11.8s (95s full scale). This is considered far enough from the wave period not to impact significantly the wave loads. 

<img src="https://github.com/Guillaume4/ISSC_2021_LOADS_BENCHMARK/blob/master/\Experiments/mooring.png" alt="mooringImage" width="200"/>

k1 = k2 = k3 = k4 = 56 N/m

alpha = 45 degrees



## Runs

Following waves are to be run by benchmark participants. All conditions are pure head waves, without any forward speed.

|   ID      | PERIOD (s) | HEIGHT (m)  |LAMBDA (m)| Steepness (%)|
| ------------- |:-------------:| -----:|:-------------:|--------:|
|Base case | (Lambda = Lpp)| |
179|1.68|0.093|4.41|2.1%
115|1.67|0.168|4.41|3.8%
118|1.66|0.229|4.41|5.2%
140|1.62|0.384|4.41|8.7%
142|1.59|0.463|4.41|10.5%
|Optional | (steepness = 5.2%)| |
123|1.44|0.172|3.31|5.2%
124|1.85|0.287|5.51|5.2%
125|2.03|0.344|6.61|5.2%
145|2.19|0.401|7.72|5.2%




## Output

To ease the post-processing of the results, participants are kindly requested to respect the following guidelines.

1. Calculation information ( file to be named "participantId\_info.dat" )
	- Institution who is running the calculation
	- Software category (among CFD, SPH, Fully non-linear potential, weakly non-linear potential)
	- Software used
	- Calculation time (order of magnitude).

2. Time series of Heave, Pitch and Vertical Bending Moment ( file to be named "participantID\_caseID.dat" )
	- 11 columns (time (s), heave (m), pitch (rad) and VBM_i (N.m), for all inter-segment from 1 to 8, separated with whitespace
	- Results given at model scale
	- Results should include still water loads
	- First line will be interpreted as still water behavior (this first line could be added "manually" in case simulation would not start from rest)
	- Time range considered as steady-state for each case should be specified in file "participantId\_STABLE.dat"


Example of results are shown in folder "Example"


Results should be send by email.


