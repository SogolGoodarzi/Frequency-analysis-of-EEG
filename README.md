# Frequency-analysis-of-EEG
<p align="justify"> EEG is obtained by recording the electrical activity of the brain through the installation of surface electrodes on the head. In EEG, the electrical effect of the activity of brain neurons is recorded and displayed as a time signal. The following figure shows the types of brain signals along with their frequencies. </p>

![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/fcb8a3ae-3537-42f2-afa7-994011037433)

* <p align="justify"> Among the data with the format .mat in data file, select three of them and enter them in the MATLAB environment using the load command. These data are the brain signals obtained from EEG, which were stored in a period of 10 seconds. (Each of these signals has 65 lines, as desired, choose one of the first 64 lines to perform the next steps. For this part of the data, we choose V2, V4 and V6. For the next sections, among the first 65 lines, we choose the 20th line for the first signal and the 40th and 60th lines respectively for the next signals. </p>

* <p align="justify"> To plot three signals in the time domain, we must first define the parameter t. The signals have been measured in the time interval of 0 to 10 seconds. "t" can be defined by specifying the sampling frequency with appropriate commands. The graph of the signals in the time domain will be as follows. </p>

![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/4da22ec5-add4-4879-8b03-d321e8f61338)

![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/1331b263-5ac2-4bd8-8099-89697b683da8)

<p align="justify"> For the frequency domain, we first define the "f" parameter based on the number of signal samples and the sampling frequency and plot the desired graphs as below. </p>

![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/7ae0d311-75a6-46ba-94df-64e3c2f70212)

![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/3ab809af-d2b1-4394-8a69-169f2dd732f1)

* <p align="justify"> Consider one of the signals, we want to extract alpha, beta, delta, theta and gamma waves. For this purpose, in turn, we zero the frequencies outside the predicted band; With Fourier inversion, we plotted the desired brain wave in the time domain, in seconds. </p>

<p align="justify"> We can see carefully in the shape of the first signal that its amplitude range, or rather its largest peak, has a larger amplitude than the other two signals. In its Fourier transform, it can be seen that the peak amplitude of its Fourier transform is smaller than the other two signals. For the second signal, its time range is smaller than the other two signals, and it can be seen in its Fourier transform that its frequency range is larger than the frequency range of the other two signals. For the third signal, whose time domain is intermediate between the other two signals, we can see that its frequency domain also has values ​​between the values ​​of the frequency domain of the other two signals. So it can be concluded that the relationship between the amplitude of the brain signal and its frequency range have an inverse relationship and if we consider these two parameters as the parameters of a function, then we will have a descending function. </p>

* <p align="justify"> To extract each of the mentioned waves, we have to remove the Fourier transform in the frequencies that are not in the range of the considered wave, then by inverting the Fourier transform, we plot the desired wave in the time domain. We have plotted the output for each of the waves. </p>

### Gamma:
![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/1c575a8b-f619-4385-80a4-3e001acd1d71)

### Betta:
![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/c3f06ec8-f262-460c-a1fa-f20c0de0ea71)

### Alpha:
![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/5835657f-663b-4b95-9c85-ddd6e2d49bf5)

### Theta:
![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/e169b96e-bd2c-4bb1-b732-f2dc81cb11aa)

### Delta:
![image](https://github.com/SogolGoodarzi/Frequency-analysis-of-EEG/assets/125180530/8b8730ff-bdd6-4037-a83a-22650fdb014c)

* <p align="justify"> According to the shape of the five waves extracted from the target signal, we can see that the predicted relationship is also true for these five waves. That is, the larger the amplitude, the lower the frequency. For the delta wave, which has the largest amplitude, we see that its Frequency range is from 0.5 to 4Hz, which is in the low frequency section. For the theta wave, which has a smaller amplitude than delta, but its amplitude is larger than the other 3 waves, we can also see that its frequency range is after the delta frequency range and is from 4 to 8Hz. The same is true for subsequent signals. For the gamma wave, which has the lowest amplitude, we see a frequency range that is in the high frequency part. </p>

* <p align="justify"> To determine a person's activity, it should be checked based on two parameters: signal amplitude and frequency. To check based on the frequency, because the main signal contains all 5 waves and has the frequency of all of them, for this reason, it is not possible to clearly state which of these 5 waves has more expression in the main signal, and it is difficult to compare, so compare and determine the activity. We do it based on the domain. In fact, the signal amplitude also has a combination of the amplitude of 5 waveforms. As we can see, the range of our chosen signal, i.e. signal 1, has a larger range than the other two signals. According to the analysis done in the previous sections, the delta wave has a larger amplitude than the other waves, so it can be assumed that the activity that a person does in that 10 seconds was deep sleep, because the activity related to this wave is deep sleep. Another possibility is that the person was meditating and being creative because this activity is related to theta wave and the large amplitude of the main signal can be considered related to the appearance of more delta or theta waves. But in general, it is better to say that it is not possible to determine a person's activity accurately, because again, similar to the analysis we said for frequency, here we can also say that the range of the main signal is a combination of the range of the mentioned 5 waves and contains all of them. It is not clear exactly what the person was doing. </p>
