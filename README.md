# Power-Performance

Matlab compatible Octave script tempcycle_100W_v2.m was developed to study the 
effect of semiconductor (FPGA) power and ambient temperature on it's junction temperature. 
Nominally the junction temperature is to be maintained below 100 degree C for a reliable operation.

Code uses hard-coded nominal values for package temperature-coefficient 
 heat-sink and air-flow values while the accelerator is drawing abut 90 W of power. 
 These values can be changed in the code for studying about any particular case.  

This is a matlab script, when executed three plots are produced:

The plot-1 corresponds to the heatsink variant-a, where the FPGA is fitted with a
10-pin heatsink and is under 200 LFM of airflow. In this configuration, when the ambient is 32.5
oC a power dissipation of up to P = 38 W in the FPGA is fine because the junction temperature
TJ is still below 100 oC, ie., TJ ≤ TJMAX, where TJMAX = 100 oC. It can also be observed from
plot-1 that TJ ≤ TJMAX can be maintained at ambient of TA = 27 oC, for P ≤ 41 W. This means, for
this configuration of heatsink (a), an ambient of 27 oC instead of 32.5 oC allows an additional
power dissipation of 3 W in the FPGA. In other words, in this configuration, moving the ambient
from TA = 27 oC to 32 oC, limits the processing power by about 3 W.

Plot-2 is a result from using heatsink variant-b across the same range
of ambient TA and power P. The only change in this configuration is that the air-flow rate used
now is higher, i.e., 300 LFM instead of 200 LFM. In can be observed that significant
performance is achieved by just using higher airflow rate and TJ ≤ TJMAX condition is well met
even at the ambient TA = 32.5 oC, for P ≤ 41 W. The FPGA has higher headroom for power
dissipation.

In plot-3 shows results correspond to the third variant (c) of the heatsink
arrangements where we use 12 mm height instead of 10 mm height, 13-pins per row and 13
rows of pins for the heatsink instead of 10-pins per row and 10 row of pins, and we also use
only a lower airflow rate of 100 LFM. It can be observed that a significant performance is
achieved just by changing total number of pins even at a lower airflow rate and TJ ≤ TJMAX
condition is more than adequately met at the ambient TA = 32.5 oC, for P ≤ 41 W. In other
words, the FPGA has much higher headroom now for power dissipation.

In summary, moving the higher end of the operating ambient TA from 27 oC to 35 oC marginally
affects the FPGA hardware by limiting the maximum usable computational power. The low-end
for the ambient at TA = 15 oC seems to be fine and has no significant effect on the hardware as
seen from this analysis

References:
References

1. https://www.altera.com/support/literature/lit-index/lit-pkg/thermal.html?type=thermal&family=Arria_10
2. Thermal Resistance Calculator
http://www.myheatsinks.com/calculate/thermal-resistance-round-pin/# .
3. AN-368-4.0 Thermal management for FPGAs, March 2012, Altera
4. http://www.zseries.in/electronics%20lab/heat%20sinks/#.WaWPdfMjF0s
5. Thermal resistivity of copper is only marginally lower than aluminum
https://heatsinks.files.wordpress.com/2010/10/heat_sink_thermal_resistance_as_a_function_of_velocity.png
6. https://www.qats.com/cms/2010/10/04/copper-heat-sinks-aluminum-heat-sinks-does-it-matter-what-you-m
ake-a-heat-sink-from/
7. https://www.altera.com/content/dam/altera-www/global/en_US/pdfs/literature/packaging/04r00461-04.pdf
8. https://www.altera.com/support/literature/lit-index/lit-pkg/thermal.html?type=thermal&family=Arria_10

