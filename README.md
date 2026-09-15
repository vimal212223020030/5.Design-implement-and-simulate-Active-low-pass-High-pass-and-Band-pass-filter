# 5.Design-implement-and-simulate-Active-low-pass-High-pass-and-Band-pass-filter

**AIM:**
To design and obtain the frequency response of i)	First order Low Pass Filter (LPF) ii)	First order High Pass Filter (HPF) iii)	Band pass filter and also simulate it using LT-Spice.

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range
1.	Function Generator	3 MHz
2.	DSO	30 MHz
3.	Dual RPS	(0 – 30) V
4.	Op-Amp	µA741
5.	Bread Board	
6.	Resistors	1.6K,10K,5.86K,38.8K,7.9K
7.	Connecting wires and probes	As required
8.  LT SPICE software

**THEORY:**

**LOW PASS FILTER**

A LPF allows frequencies from 0 to higher cut of frequency, fH. At fH the gain is 0.707 Amax, and after fH gain decreases at a constant rate with an increase in frequency. The gain decreases 20dB each time the frequency is increased by 10. Hence the rate at which the gain rolls off after fH is 20dB/decade or 6 dB/ octave, where octave signifies a two fold increase in frequency. The frequency f=fH is called the cut off frequency because the gain of the filter at this frequency is down by 3 dB from 0 Hz. Other equivalent terms for cut-off frequency are -3dB frequency, break frequency, or corner frequency.
 
**HIGH PASS FILTER**

The frequency at which the magnitude of the gain is 0.707 times the maximum value of gain is called low cut off frequency. Obviously, all frequencies higher than fL are pass band frequencies with the highest frequency determined by the closed –loop band width all of the op-amp.

**BAND PASS FILTER**

A band pass filter has a pass band between two cutoff frequencies fH and fL such that fH > fL. Any input frequency outside this pass band is attenuated. There are two types of band-pass filters. Wide band pass and Narrow band pass filters. We can define a filter as wide band pass if its quality factor Q <10. If Q>10, then we call the filter a narrow band pass filter. A wide band pass filter can be formed by simply cascading high-pass and low-pass sections. The order of band pass filter depends on the order of high pass and low pass sections.

**DESIGN:LPF & HPF**

Given: fH = 1 KHz = 1/ (2πRC)
Let C = 0.1 µF, R = 1.6 KΩ
For n = 2, α (damping factor) = 1.414, Passband gain = Ao = 3 - α =3 – 1.414 = 1.586.
Transfer function of second order butterworth LPF as:
H(s) = 1.586/S2 + 1.414 s + 1
Now	Ao = 1 + (Rf / R1) = 1.586 = 1 + 0.586
Let Ri = 10 KΩ, then Rf = 5.86 KΩ

**DESIGN: BAND PASS FILTER**

Design a BPF to pass a band of 400Hz to 2KHz with a pass band gain of 4.
1.	Select the highest cut-off frequency of LPF as fH = 10 KHz and the lowest cut-off frequency of HPF as fL = 1 KHz.
2.	Design the HPF first by taking fL = 1KHz. Assume the value of C < 1μf.
3.	 Let C = 0.1μf.
4.	Calculate R from the expression. Given: fH = 2KHz = 1/ (2πR1C1)
5.	Let C1 = 0.1 µF, R1 = 7.9 KΩ
Given: fL = 400Hz = 1/ (2πR2C2)
Let C2 = 0.1 µF, R2 = 39.8 KΩ
Pass band Gain=4
Now		Ao = 1 + (Rf / R1) 2-1=(Rf / Ri)
Ri = Rf
Let Ri = Rf = 10 KΩ


**PROCEDURE - (LPF & HPF):**

1.	Connect the circuit as shown in the circuit diagram.
2.	Select the corresponding cut-off frequency (higher or lower) and determine the value of C&R. select the value of R1 & Rf depending on desired passband gain Af..
3.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
4.	Tabulate the output voltage Vo with respect to different values of input frequency.
5.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 
**BAND PASS FILTER**

1.	Select the lower and higher cut-off frequency and calculate the value of R & C for the given frequencies.
2.	Design for LPF & HPF separately and then combine the circuit by first placing the HPF followed by a LPF (i.e) HPF in series with LPF.
3.	Connect the circuit as shown in the circuit diagram.
4.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
5.	Tabulate the output voltage Vo with respect to different values of input frequency.
6.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 

**LPF:**
  **CIRCUIT DIAGRAM**
<img width="1600" height="940" alt="image" src="https://github.com/user-attachments/assets/71fe62ec-43d7-4d0f-8a09-629d2b601dd3" />

  **MODEL GRAPH:**
<img width="1594" height="1148" alt="WhatsApp Image 2026-09-14 at 8 19 02 PM" src="https://github.com/user-attachments/assets/6ccd1b92-a986-4c62-9265-d72c6a7d217a" />

  **TABULATION:**
 <img width="1600" height="1034" alt="image" src="https://github.com/user-attachments/assets/62011a07-bb12-4567-a1d9-cccd655cf0cb" />
  **GRAPH:**
  <img width="1600" height="985" alt="image" src="https://github.com/user-attachments/assets/8d9f5772-b1c3-47dc-bee9-e8e088c12557" />

**HPF:**
  **CIRCUIT DIAGRAM**
<img width="1600" height="831" alt="WhatsApp Image 2026-09-14 at 8 21 53 PM" src="https://github.com/user-attachments/assets/e9cb4512-f29b-4a4d-9843-264d237a336e" />

  **MODEL GRAPH:**
<img width="1600" height="856" alt="WhatsApp Image 2026-09-14 at 8 22 12 PM" src="https://github.com/user-attachments/assets/737a110b-e346-4ed6-9cff-e765fae0e966" />

  **TABULATION:**
<img width="1403" height="1148" alt="image" src="https://github.com/user-attachments/assets/35b62298-0067-4ffc-b104-3785398291cb" />
  **GRAPH:**
  <img width="1600" height="1064" alt="image" src="https://github.com/user-attachments/assets/0b499332-7ca9-476a-aef5-92aa0b094c08" />

  **BPF:**
  **CIRCUIT DIAGRAM**
<img width="1442" height="812" alt="image" src="https://github.com/user-attachments/assets/41621e9a-5c8f-4b48-a56e-f97dd4ec67c9" />

  **MODEL GRAPH:**
<img width="1583" height="848" alt="image" src="https://github.com/user-attachments/assets/301a440d-c66b-4552-bc81-c11155639c3b" />

  **TABULATION:**
<img width="1288" height="1148" alt="WhatsApp Image 2026-09-14 at 8 26 14 PM" src="https://github.com/user-attachments/assets/5b22b616-7821-42c7-a012-268db3915c99" />

  **GRAPH:**
  <img width="1600" height="1083" alt="image" src="https://github.com/user-attachments/assets/8d6a2b87-75da-439a-b09f-52239a6a0024" />

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  **HPF**
  <img width="1771" height="877" alt="(ADAIC) High pas filter" src="https://github.com/user-attachments/assets/d0be201a-9b15-4433-bc06-4a259b1977c9" />
  **LPF**
  <img width="1703" height="835" alt="(ADAIC) Low pass filter" src="https://github.com/user-attachments/assets/1aa09c34-043d-43c5-b1a0-233ae688f04b" />
  **BPF**
  <img width="1746" height="860" alt="(ADAIC) Band pass filter" src="https://github.com/user-attachments/assets/56e5afec-08ed-49d6-b6f6-986f437736c5" />


**RESULT:**
Thus the Active Low pass, High pass and Band Pass Filters are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
 
