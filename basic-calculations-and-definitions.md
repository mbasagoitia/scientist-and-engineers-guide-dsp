# Mean, Standard Deviation, and RMS

The **mean** is the average value of a signal and is found by adding all samples together and dividing by N. Also known as DC (direct current) value.

The **alternating current (AC)** refers to how the signal fluctuates around the mean value. A generalized way of measuring this value is with the **standard deviation.**

**Average deviation** is found by summing the absolute value of the deviations of each individual sample from the mean and dividing by N. However, this value isn't typically relevant in statistics.

The **standard deviation** represents how far the signal fluctuates from the mean (noise and interference). Only measures the AC portion of a signal. It is calculated by squaring each of the deviations of each sample from the mean before taking the average, then taking the square root of that. See below on why we divide by N - 1 instead of N.

**Variance** is standard deviation squared and represents the power of this fluctuation.

**RMS (root-mean-square)** measures both AC and DC components of a signal. If a signal has no DC value, its rms is the same as it standard deviation. 

**Signal-to-noise ratio (SNR)** = mean/standard deviation

**Coefficient of variation (CV)** = (standard deviation/mean) * 100%

Better data means a higher SNR value and lower CV value.

## Probability and Statistics

Note there is a difference between statistics on an N point signal and the probability of the underlying process that generated the signal.

**Typical error** in calculating the mean of an underlying process by using a finite number of samples N is given by standard deviation/(N^1/2). The larger N is, the smaller the expected error will become.

Typically, we only know the mean of the N point signal, not the mean of the underlying process that created the signal. This value contains an error due to statistical noise, which reduces the calculated value of the standard deviation. To compensate for this, N is replaced by N - 1 in the calculation of the standard deviation. This provides an estimate of the standard deviation of the underlying process and is more accurate when N is smaller. If we divide by N, that is the standard deviation of the acquired signal.

A **histogram** is a measure of the frequency of each possible value in an acquired signal. The corresponding curve for the underlying process is the **probability mass function (pmf).** A histogram is calculated using a finite number of samples, and the pmf would be obtained with an infinite number of samples and can be inferred from the histogram or may be deduced by some mathematical technique. The pmf describes the probability that a certain value will be generated. 

Whereas the histogram and pmf can only be used with discrete data, the **probability density/distribution function (pdf)** is analogous to the pmf on continuous signals. 

The sum of all histogram values must equal N (the number of samples), whereas the sum of all pmf and pdf values must equal 1.

**Binning** is a technique that arbitrarily selects the length of the histogram to be some convenient number such as 1,000 points called bins. The value of each bin represents the total number of samples in the signal that have a value within a certain range. The number of bins controls a tradeoff between resolution along each axis.

Signals formed from random processes usually have a bell-shaped (Gaussian) curve given by e^-x^2, which can be expanded by adding an adjustable mean and standard deviation and normalized so that the total area under the curve equals 1.

The integral of the pdf is used to find the probability that a signal will be within a certain range of values. This integral is known as the **cumulative distribution function (cdf).**

**Accuracy** is defined as the difference between the true value and the mean of the underlying process that generates the data. **Precision** is the spread of values, specified by the standard deviation SNR, or CV. Poor accuracy results from systematic errors suhc as poor calibration that are repeated each time a measurement is conducted. Poor precision results from random errors--each individual measurement is a poor measurement of the true value, although all measurements perform well overall.

Precision can be improved by averaging successive readings; accuracy can be improved by better calibration.