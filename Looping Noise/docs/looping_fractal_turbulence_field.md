### ***looping_fractal_turbulence_field***
A vector field whose value at any position is given by the sum of one or more layers of curl noise that loops after the amount of frames specified.<br />

***
## Input
<span style="color:#82D99F">***position***</span>
<br />The input position to sample the noise at.

***
## Loop Settings
<span style="color:#82D99F">***loop_frames***</span>
<br />Amount of frames to loop.

<span style="color:#82D99F">***time_scale***</span>
<br />Multiplies time by this value to control the speed of the noise.

<span style="color:#82D99F">***smooth_loop***</span>
<br />Can help smooth the blending between current noise and past noise.

***
## Curl Noise Settings
<span style="color:#82D99F">***magnitude***</span>
<br />This scales the output field. Before being multiplied by magnitude the range of the noise is normally between -1.0 and 1.0, but may be greater if the ratio value is larger. 

<span style="color:#82D99F">***num_frequencies***</span>
<br />This is the total number of noise frequencies to sum. Generally as this number increases there will be more detail or small scale noise. The value does not need to be an integer. If one slowly animates num_frequencies the finest scale noise will gradually fade in, rather than popping on at integer values. 

<span style="color:#82D99F">***frequency***</span>
<br />This is the base frequency of the fractal noise. Higher values have finer detail. 

<span style="color:#82D99F">***ratio***</span>
<br />This is the ratio of magnitude of each noise frequency to the previous. If it is the same as frequency_ratio then the magnitude of each noise will be the same relative to its scale. When this value is higher the small details are stronger.

<span style="color:#82D99F">***frequency_ratio***</span>
<br />This is the ratio of each noise frequency to the previous. At a value of 0.5 each additional frequency is double the previous (twice the detail). Lower values can provide a greater range of noise frequencies while needing a lower num_frequencies. 

<span style="color:#82D99F">***time_ratio***</span>
<br />This is the ratio of how fast the different noise frequencies animate. If the value is 1.0 then the frequencies all animate the same relative to their scale. A value around 1.5 (when the frequency_ratio is 0.5) may look better for natural effects, like a turbulent fluid surface. 

<span style="color:#82D99F">***seed***</span>
<br />The seed to use for randomization.

***
## Output
<span style="color:#82D99F">***noise_field***</span>
<br />The output turbulence vector field. The general range is around -1.0 to 1.0 but may differ based on magnitude, ratio, and num_frequencies settings. 

