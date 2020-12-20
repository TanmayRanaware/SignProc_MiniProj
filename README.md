
# VOICE RECOGNITION TO IDENTIFY SPEAKER

## Team Members
<ul>
 <li>Tanmay Ranaware</li>
 </ul>

## Mentors
<ul>
 <li>Harish Bachu</li>
<li>Pravan Omprakash</li>
 <li>Sujith Bhat</li>
</ul>

### Objectives
<p>
The project aims at building a voice recognition program to identify speaker in the audio file.The project makes use of signal processing for feature extraction.Recognition is done using ML algorithms.The work was then divided into major two parts.
 </p>
<ul>
 <li>Extraction of Mel Frequency Cepstral Spectogram Coefficients</li>
<li>Create a CNN model, train the model with the given data.</li>
 </ul>
 
### Methodology
#### Extraction of Mel Frequency Cepstral Spectogram Coefficients
The audio is loaded and made available for feature extraction using Signal Processing.Amplitude envelope of a waveforms is then  captured to  give an idea about the loudness of the audio.
![Screenshot 2020-12-20 122504](https://user-images.githubusercontent.com/56064349/102708405-ee124800-42c8-11eb-83df-46e08f0d9c75.png)
![A2](https://user-images.githubusercontent.com/56064349/102708429-14d07e80-42c9-11eb-971b-d0222dd2a5df.png)
![A3](https://user-images.githubusercontent.com/56064349/102708466-56612980-42c9-11eb-9fb4-fcb266b7c27a.png)
![A4](https://user-images.githubusercontent.com/56064349/102708480-7f81ba00-42c9-11eb-8dda-1ad23fffaaa6.png)

To move wave from a time domain to frequency domain we need to perform Fast Fourier Transform.Fourier transform decomposes a periodic sound into a sum of sine waves which all vibrate oscillate at different frequencies. It is quite incredible so we can describe a very complex sound as long as it’s periodic as a sum as the superimposition of a bunch of different sine waves at different frequencies.
<p>By applying the Fourier transform we move in the frequency domain.The magnitude is a function of the frequency itself but by this information about time is lost.But audio data alike is a time series,so how things change in time should be known and with the Fourier transform it can’t be achived, so lot of information is missing.
</p>
<p>
 The solution to this is short time Fourier transform(stft).What the short time Fourier transform does it computes several Fourier transforms at different intervals and in doing so it preserves information about time and the way sound evolved it's over time ,so  fix the number of samples  and do the Fourier transform there and then  move on to to the rest lack of the waveform and what happens here is that we get a spectogram which gives us information of (time + frequency + magnitude)
 <\p>
  
 ### Spectograms
 #### Audio1
 
 ![a1](https://user-images.githubusercontent.com/56064349/102709568-181c3800-42d2-11eb-8356-483c949b4c09.png)
 
 #### Audio2
 
 ![A2](https://user-images.githubusercontent.com/56064349/102709621-3d10ab00-42d2-11eb-8ed8-a4f2e209a279.png)

 #### Audio3

![A3](https://user-images.githubusercontent.com/56064349/102709678-852fcd80-42d2-11eb-92eb-87142e16f83c.png)
 
 #### Audio4
 
  ![A4](https://user-images.githubusercontent.com/56064349/102709686-8fea6280-42d2-11eb-9ec7-39de7e6abe34.png)
  
 Time is on the x-axis,frequency on the y-axis and a third axis which is given by the colour and the colour is tells how much a given frequency is present in the sound at a given time.So here low-frequency sound is more in all audios.
 
 The human perception of sound levels is not linear, but better approximated by a logarithm.By converting to decibels (dB) the scale becomes logarithmic. This limits the numerical range, to something like 0-120 dB.The intensity of colors when this is plotted corresponds more closely to what humans hear than if  used a linear scale.
 
 ### Spectograms
 
 #### Audio1
 
 ![a1](https://user-images.githubusercontent.com/56064349/102709881-7813de00-42d4-11eb-9f7f-e67f7eff82d5.png)
  
 #### Audio2
 
 ![A2](https://user-images.githubusercontent.com/56064349/102709883-7a763800-42d4-11eb-9065-3122de17df23.png)

 #### Audio3
 
 ![A3](https://user-images.githubusercontent.com/56064349/102709886-7cd89200-42d4-11eb-8766-24e9e414ac18.png)

 
 #### Audio4
 
 ![A4](https://user-images.githubusercontent.com/56064349/102709887-7ea25580-42d4-11eb-9849-f128fb54f556.png)
 
 
 Mel Frequency Cepstral Coefficents (MFCCs) is a way of extracting features from an audio. The MFCC uses the MEL scale to divide the frequency band to sub-bands and then extracts the Cepstral Coefficents using Discrete Cosine Transform (DCT). MEL scale is based on the way humans distinguish between frequencies which makes it very convenient to process sounds.
 
 #### Audio1
![a1](https://user-images.githubusercontent.com/56064349/102711109-48b59f00-42dd-11eb-9b3e-5a96280e6bc8.png)
 
 #### Audio2
![A2](https://user-images.githubusercontent.com/56064349/102711110-494e3580-42dd-11eb-82ab-5a190d115ed1.png)
 #### Audio3
![A3](https://user-images.githubusercontent.com/56064349/102711105-46ebdb80-42dd-11eb-8f5e-926f942e025f.png)
 #### Audio4
![A4](https://user-images.githubusercontent.com/56064349/102711106-481d0880-42dd-11eb-9cc7-ce489b03c545.png)
 
 
Here we had 15 MFCC’s coefficient represented in the y-axis, time in the x-axis and more the yellow, more is the value of that coefficient in that time frame.

#### Create a CNN model, train the model with the given data

The MFCC's now, have to be classified into their classes of person. Identifying this classification problem, a deep learning model was proposed for efficient training and to get accurate results. A Convolutional Neural Network (CNN) model was designed and used as the model.

![model](https://user-images.githubusercontent.com/56064349/102711322-b7472c80-42de-11eb-9640-57078fab696b.png)


 
 
 
 
   
    
    


