# Alignment of temporal series

### **Background**

A research lab is performing an experiment where human participants are sitted in front of a computer screen and are asked to breath in from a tube when they are "triggered" to do so with a visual cue in the screen. The experiment consist of a tutorial phase with a flexible number of trials followed by 120 "good" trials. A trial is considered good if the participant responds to a question after the trial within a period of time. In each trial, the participant is presented with a visual cue to start breathing in, stop, exhale and repeat, so in each trial, a participant has to breath in two times. The experiment is setup to increase the resistance of the air flow that the participants are breathing for every trigger. After the two breathing in attempts, the participants need to answer which inhalation felt more resistive.

The experiment instruments are:

- Behavioural task programmed in Matlab to cue the participants when to inhale or to respond to the question.
- The Matlab program also changes the colour of a small square in the screen to encode information about when there is a trigger, which trigger was more resistive, as well as when there is a question prompted and what the participant responded.
- Photodiode is attached to the screen to record the color of the square in the screen.
- Breathing belt that measures chest expansion.
- Flow sensor in the tube.
- Pressure sensor in the tube.

### **Data**

- .tsv file containing behavioural data:
  - time stamps of screen cues,
  - which screen cue was related with the more resistive air flow and
  - response of participant.
- .tsv.gz file:
  - time stamps,
  - respiration belt resistance values and
  - photodiode intensity values.
- .json file describing the columns of the previous file.
- .edf file:
  - time stamps,
  - values of the pressure sensor.
- .csv file:
  - time stamps,
  - values of the flow sensor.

### **Problem**

Alignment of sensor data coming from the triggers of the experiment, a respiration belt, flow and pressure sensors. Each data stream comes from a different device with unsynchronized time stamps, they have different data formats resolutions and qualities.
