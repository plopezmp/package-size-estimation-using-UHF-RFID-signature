# package-size-estimation-using-UHF-RFID-signature
Datasets corresponding a combination of reading scenarios
- First letter indicates scenario's type: (I) Ideal, (S) Simple, (C) Complex.
- Second letter indicates distance between antennas (d): (P) 2 m, (M) 2.5 m, (G) 3 m.  
- Third letter indicates the number of boxes of the tested dataset: (P) 4 boxes, (M) 8 boxes, (G) 16 boxes. 

Files in TL1SXM, TL2SMF and TL3NMM correspond with the data and results of the tranfer learning approach.

## Data explanation
The interrogation process uses FSA with a fixed frame length of 16 slots. This experiment has been repeated 20000 times (each with a random
package configuration) to construct the datasets for training the predictive system.

The data collected in the experiments are in two `txt` files, `index` and `frames` for each configuration scenario. 
The `index` file summarizes, at each row, the high-level statistics for the interrogation procedure of each package.
An example of the data registered:

<img src='zfigs/index.png' width='750'>
That contains a summary of the interrogation performed on a box, such as the LxWxH dimensions or the position of the box with respect of the antennas.

The `frames` file provides low-level statistics for each interrogation frame. An example of statistics collected:

<img src='zfigs/frames.png' width='650'>

(note that the interrogation procedure for each package usually comprises multiple frames).
For example, the first package was inventoried in the 12 first frames. In the frame 12, a
last tag is identified.

These datasets has been used to train different models of ANNs. The results could be reviewed in the paper

Vales-Alonso,J; López-Matencio,P. *A machine learning approach for package size estimation using UHF RFID interrogation signature*, actually under reviewing process in **Applied Intelligence (APIN)** Journal.
