The purpose of this lab was to understand the useage of timers, interrupts, and the DAC. 

We were given a script to generate audio data from MATLAB, and generated an array of audio data from that and imported it into Keil. We generated the C code by using STMCube.

In order to play audio, both DAC channels were used to play back the output via headphones. Interrupts were used based on one of the timers in order to play back the audio at the desired frequency (8kHz, the same rate as the sampled data). 
