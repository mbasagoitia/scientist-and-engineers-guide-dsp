# Mean, Standard Deviation, and RMS

The **mean** is the average value of a signal and is found by adding all samples together and dividing by N. Also known as DC (direct current) value.

The **alternating current (AC)** refers to how the signal fluctuates around the mean value. A generalized way of measuring this value is with the **standard deviation.**

**Average deviation** is found by summing the absolute value of the deviations of each individual sample from the mean and dividing by N. However, this value isn't typically relevant in statistics.

The **standard deviation** represents how far the signal fluctuates from the mean (noise and interference). Only measures the AC portion of a signal. It is calculated by squaring each of the deviations of each sample from the mean before taking the average, then taking the square root of that.

**Variance** is standard deviation squared and represents the power of this fluctuation.

**RMS (root-mean-square)** measures both AC and DC components of a signal. If a signal has no DC value, its rms is the same as it standard deviation. 

**Signal-to-noise ratio (SNR)** = mean/standard deviation

**Coefficient of variation (CV)** = (standard deviation/mean) * 100%

Better data means a higher SNR value and lower CV value.