# BCI-Competition-III-Data-set-I-‹motor imagery in ECoG recordings, session-to-session transfer›

### Experiment
During the BCI experiment, a subject had to perform imagined movements of either the left small finger or the tongue. The time series of the electrical brain activity was picked up during these trials using a 8x8 ECoG platinum electrode grid which was placed on the contralateral (right) motor cortex. The grid was assumed to cover the right motor cortex completely, but due to its size (approx. 8x8cm) it partly covered also surrounding cortex areas. All recordings were performed with a sampling rate of 1000Hz. After amplification the recorded potentials were stored as microvolt values. Every trial consisted of either an imagined tongue or an imagined finger movement and was recorded for 3 seconds duration. To avoid visually evoked potentials being reflected by the data, the recording intervals started 0.5 seconds after the visual cue had ended.

### Format of the Data
The labeled training data (from the first session) is stored as a zipped matlab file called Competition_train.mat.gz. Use this data to train your classification algorithms. It consists of two parts:
* Part 1: the brain activity during 278 trials. This part is stored in a 3D matrix named X using the following format: [trials x electrode channels x samples of time series].
* Part 2: the labels of the 278 trials. This part is stored as a vector of -1 / 1 values named Y.
The unlabeled test data is also stored as a zipped matlab file called Competition_test.mat.gz. It contains 100 trials of brain activity in matrix X (3D format is the same as described above) but it contains no labels Y.

### Task
Please try to correctly classify the test data set. Provide a list of the labels (-1/1) of these trials in either ascii or matlab format. 

### Performance criterion
How many of the labels you provided match the true labels of the test set?
