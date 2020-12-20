
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
<p> The solution to this is short time Fourier transform(stft).What the short time Fourier transform does it computes several Fourier transforms at different intervals and in doing so it preserves information about time and the way sound evolved it's over time ,so  fix the number of samples  and do the Fourier transform there and then  move on to to the rest lack of the waveform and what happens here is that we get a spectogram which gives us information of (time + frequency + magnitude)
 <\p>
  
 ### Spectograms
 #### Audio1
 
 ![a1](https://user-images.githubusercontent.com/56064349/102709568-181c3800-42d2-11eb-8356-483c949b4c09.png)
 
 #### Audio2
 
 ![A2](https://user-images.githubusercontent.com/56064349/102709621-3d10ab00-42d2-11eb-8ed8-a4f2e209a279.png)

 #### Audio3
 
 
 #### Audio4
 
 


