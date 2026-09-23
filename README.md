
# BE Capstone Project

SMART ELECTROPLATING SYSTEM

SMART ELECTROPLATING SYSTEM 

YT LINK- https://youtu.be/6FQ77SdycFc?feature=shared


## Team Details

| Sr. No. | Name of Student | Roll No. | Branch | Email ID |
|---|---|---|---|---|
| 1 | Arko Mukherjee | 14 | AUTOMATION AND ROBOTICS | 2023.arko.mukherjee@ves.ac.in |
| 2 | Sanika Puranik | 23 | AUTOMATION AND ROBOTICS | 2023.sanika.puranik@ves.ac.in |
| 3 | Archit Kothavade | 8 |  AUTOMATION AND ROBOTICS| 2023.archit.kothavade@ves.ac.in |
| 4 | Athang Bhandarkar| 38 | AUTOMATION AND ROBOTICS | 2023.athang.bhandarkar@ves.ac.in |

---

## Guide Details

Project Guide: Prasad Godse sir
Department:Automation and Robotics  
Institute:VESIT, Mumbai  

---

## Problem Statement

Conventional electroplating requires frequent manual monitoring of pH, temperature, electrolyte purity, plating current, and bath level, which can lead to inconsistent coating quality.
Changes in pH and accumulation of impurities can affect coating thickness, adhesion, and surface finish.
The proposed system uses an ESP32-based control system for real-time monitoring of critical process parameters.
It automatically controls boric-acid dosing .
The system also provides safety monitoring, alarms, HMI/IoT data logging, and process tracking.
This aims to reduce manual intervention and improve the consistency, reliability, and quality of electroplating.
---

## Abstract

Conventional electroplating processes require continuous manual monitoring and adjustment of critical parameters such as pH, temperature, electrolyte purity, plating current, and bath level. Variations in these parameters and the accumulation of impurities can result in inconsistent coating thickness, poor surface finish, and reduced coating quality. This project proposes a Smart Electroplating System that automates process monitoring and selected corrective actions to improve plating consistency and reliability.

The proposed system uses an ESP32 microcontroller as the central control unit, integrated with sensors for monitoring pH, temperature, liquid level, flow, and electrical parameters. Based on the monitored conditions, the system controls boric-acid dosing for pH correction and an automated pump-based filtration system for electrolyte maintenance. Safety interlocks and alarms are incorporated to detect abnormal conditions, while an HMI/IoT interface enables real-time visualization and data logging.

The expected outcome is a reduction in manual intervention, improved process stability, and more consistent electroplating quality. The system can be applied in industrial metal finishing, automotive components, electronics, manufacturing, and other electroplating industries where reliable and automated process control is required.

---

## Objectives

Objectives
1.To study the existing electroplating process, its limitations, and available automation solutions.
2.To design an ESP32-based hardware and software architecture for real-time monitoring and control of the electroplating process.
3.To implement pH monitoring and automated dosing, electrolyte filtration, temperature/level monitoring, and process safety controls.
4.To test and validate the system for process stability, reduced manual intervention, and improved coating consistency.
5.To develop HMI/IoT-based monitoring and data logging and document the complete project for future industrial applications.
---

## Scope of the Project

The project will cover:

1.Design and development of a smart electroplating prototype using ESP32 as the main controller.
2.Hardware implementation of pH, temperature, level, flow, and electrical parameter monitoring.
3.pH correction through pump and dosing control.
4.HMI/IoT interface for real-time monitoring, alarms, and data logging.
5.System testing and data collection under controlled operating conditions.
6.Performance analysis based on process stability, filtration effectiveness, manual intervention, and coating consistency.

## Existing System

Conventional electroplating systems generally rely on manual monitoring and periodic adjustment of parameters such as pH, temperature, electrolyte condition, plating current, and bath level. Chemical dosing are often performed manually or at fixed intervals, depending on operator experience.

Limitations
High manual intervention for monitoring and maintaining bath conditions.
Limited real-time monitoring of critical parameters.
Inconsistent coating quality due to variations in pH, temperature, impurities, and current.
Delayed detection of abnormal conditions, which can affect the plating process.
Chemical dosing can result in over- or under-treatment.
Limited data logging and process traceability for analyzing coating performance.
Difficulty in scaling and integrating automation into smaller conventional plating setups.

---

## Proposed System

Proposed System

The proposed system is a Smart Electroplating System designed to automate the monitoring and maintenance of critical electroplating parameters. An ESP32 microcontroller continuously collects data from sensors and controls the required process operations based on predefined conditions.

Main Idea

To develop an automated electroplating system that provides real-time monitoring, automatic electrolyte filtration, pH correction, and safety monitoring to improve coating consistency and reduce manual intervention.

How It Works
Sensors continuously monitor pH, temperature, liquid level, flow, and electrical parameters.
The ESP32 processes the sensor data and compares it with the required operating conditions.
Based on the pH condition, the system controls boric-acid dosing.
Safety interlocks detect conditions such as low level, abnormal temperature, excessive current, or loss of flow and generate alarms or stop the relevant actuator.
An HMI/IoT interface displays and records process parameters and system status.

Major Components
ESP32 microcontroller
pH, temperature and turbidity sensors
Level and flow sensors
DC plating power supply/rectifier
Circulation pump and filtration unit
Boric-acid dosing pump
Current/voltage monitoring
HMI/display and IoT data logging
Alarm and safety-interlock system

Expected Benefits
Reduced manual monitoring and intervention
Improved electrolyte condition and process stability
More consistent coating quality
Early detection of process abnormalities
Automated filtration and pH correction
Real-time monitoring and data logging
Better scope for industrial automation and scalability
---

## System Architecture

                  ┌──────────────────────┐
                  │   AC Supply / DC     │
                  │   Plating Rectifier  │
                  └──────────┬───────────┘
                             │
                       DC Plating Power
                             │
                    ┌────────┴────────┐
                    │ Electroplating  │
                    │      Bath       │
                    │ Anode + Cathode │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
        ┌───────────┐  ┌────────────┐  ┌────────────┐
        │ pH Sensor │  │Temperature │  │ Level/Flow │
        │           │  │   Sensor   │  │   Sensor   │
        └─────┬─────┘  └──────┬─────┘  └──────┬─────┘
              │               │               │
              └───────────────┼───────────────┘
                              ▼
                       ┌──────────────┐
                       │    ESP32     │
                       │  Controller  │
                       └──────┬───────┘
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
      ┌────────────┐   ┌────────────┐   ┌──────────────┐
      │  Dosing    │   │  Current/  │   │ HMI / IoT    │
      │   Pump     │   │  Voltage   │   │ Monitoring   │
      └─────┬──────┘   │ Monitoring │   └──────────────┘
            │          └────────────┘
            ▼
      ┌────────────┐
      │ Boric Acid │
      │   Dosing   │
      └─────┬──────┘
            │
            ▼
     ┌──────────────┐
     │ Electroplating│
     │     Bath      │
     └──────────────┘

        Safety Monitoring & Alarm
                 ▲
                 │
              ESP32
Briefly explain the architecture.

1.Power Supply: The AC supply is converted into controlled DC power using a rectifier for the electroplating process.
2.Electroplating Bath: The DC supply is connected to the nickel anode and workpiece (cathode) to perform electroplating.
3.Sensor Monitoring: pH, temperature, level, flow, current, and voltage are continuously monitored to track the condition of the process.
4.ESP32 Controller: The ESP32 receives sensor data, processes it, and compares the values with the predefined operating conditions.
pH Control: If the pH deviates from the required range, the ESP32 controls the boric-acid dosing pump to correct the electrolyte condition.
5.Safety Control: Level, flow, temperature, and electrical parameters are monitored to detect abnormal conditions and activate alarms or protective actions.
6.HMI/IoT Monitoring: The process parameters, actuator status, and alarms are displayed on the HMI/IoT interface and can be recorded for further analysis.
7.Continuous Operation: The system continuously repeats the monitor → analyze → control → monitor cycle to maintain stable electroplating conditions.

## Hardware Requirements

| Sr. No. | Component                 | Specification            | Quantity | Purpose                     |
| ------- | ---------                 | -------------            | -------- | -------                     |
| 1       | Temperature sensor        | PT 100 RTD               | 1        | Sensing temperature         |
| 2       | Temperature Controller    | Range -50 to 110 degree  | 1        | on off controller for heater|
| 3       | Relay                     | 5A relay                 | 1        | on off action               |
| 4       | pH probe                  | hydrogen bulb            | 1        | pH sensing                  |
| 5       | Current sensor            | ACS 712                  | 1        | sensing current             |
| 6       | Current sensor Module     | ACS 712 Current module   | 1        | Measuring currrent          |
| 7       | voltage sensor module     |                          | 1        | Measuring voltage           |
| 8       | ESP 32                    |                          | 1        | Microcontroller            
## Software Requirements

| Sr. No. | Software / Tool | Version | Purpose         |
| ------- | --------------- | ------- | -------         |
| 1       | Aurdino IDE     | 1.8.9   | Calculating AHI |


---

## Technologies Used

Mention technologies used in the project.

Example:

* Arduino C / C++
* Arduino IDE / ESP32 
* Machine Learning / Computer Vision
* 
* 

---

## Methodology

Explain the step-by-step approach.

1. industrial visit
2. Problem identification
3. Requirement analysis
4. System design
5. Hardware/software development
6. Integration
7. Testing and validation
8. Documentation and publication

---

## Project Timeline

| Week / Month | Task Planned          | Status                            |
| ------------ | --------------------- | --------------------------------- |
| Week 1       | Problem finalization  | Completed                         |
| Week 2       | Requirement analysis  | Completed                         |
| Week 3       | System design         | Completed                         |
| Week 4       | Prototype development | In progess                        |
| Week 5       | Testing               | In progess                        |
| Week 6       | Documentation         | pending                           |
| Week 7       | Paper writing         | pending                           |

---

## Weekly Progress Updates

Students must update this section every week.

| Week   | Date | Work Completed | Work Planned for Next Week | Issues / Challenges | GitHub Commit Link |
| ------ | ---- | -------------- | -------------------------- | ------------------- | ------------------ |
| Week 1 |      |                |                            |                     |                    |
| Week 2 |      |                |                            |                     |                    |
| Week 3 |      |                |                            |                     |                    |
| Week 4 |      |                |                            |                     |                    |
| Week 5 |      |                |                            |                     |                    |
| Week 6 |      |                |                            |                     |                    |
| Week 7 |      |                |                            |                     |                    |
| Week 8 |      |                |                            |                     |                    |



## Circuit Diagram

Add circuit diagram image here.

```markdown
![Circuit Diagram](images/circuit_diagram.png)
```

---

## Flowchart / Algorithm

                  ┌──────────────────────┐
                  │   AC Supply / DC     │
                  │   Plating Rectifier  │
                  └──────────┬───────────┘
                             │
                       DC Plating Power
                             │
                    ┌────────┴────────┐
                    │ Electroplating  │
                    │      Bath       │
                    │ Anode + Cathode │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
              ▼              ▼              ▼
        ┌───────────┐  ┌────────────┐  ┌────────────┐
        │ pH Sensor │  │Temperature │  │ Level/Flow │
        │           │  │   Sensor   │  │   Sensor   │
        └─────┬─────┘  └──────┬─────┘  └──────┬─────┘
              │               │               │
              └───────────────┼───────────────┘
                              ▼
                       ┌──────────────┐
                       │    ESP32     │
                       │  Controller  │
                       └──────┬───────┘
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
      ┌────────────┐   ┌────────────┐   ┌──────────────┐
      │  Dosing    │   │  Current/  │   │ HMI / IoT    │
      │   Pump     │   │  Voltage   │   │ Monitoring   │
      └─────┬──────┘   │ Monitoring │   └──────────────┘
            │          └────────────┘
            ▼
      ┌────────────┐
      │ Boric Acid │
      │   Dosing   │
      └─────┬──────┘
            │
            ▼
     ┌──────────────┐
     │Electroplating│
     │    Bath      │
     └──────────────┘

        Safety Monitoring & Alarm
                 ▲
                 │
               ESP32

```markdown
![Flowchart](images/flowchart.png)
```

### Algorithm

1. Start
2. Initialize the system
3. Read input from sensors/user
4. Process the data
5. Generate output/control action
6. Display/store/transmit result
7. Stop

---

## Implementation Details


### Hardware Implementation

1. Hardware Implementation
A. Electroplating Tank
Tank size: 400 × 300 × 200 mm
Working electrolyte: Nickel plating solution
Nickel anode connected to the positive terminal of the DC supply
Cathode/workpiece connected to the negative terminal
Sensors are mounted around the tank for process monitoring.
B. Temperature Control

Hardware:

Temperature sensor — PT100/thermocouple depending on your selected controller
Digital temperature controller
Heating element
SSR/relay
Electrolyte tank

Working:

Temperature Sensor → Temperature Controller → SSR/Relay → Heater

The sensor continuously measures bath temperature. When the temperature falls below the setpoint, the controller activates the heater. Once the setpoint is reached, heating is reduced/switched off.

C. Voltage & Current Monitoring

Hardware:

DC power supply
Voltage sensor/module
Current sensor/module
ESP32
Display

Basic arrangement:

DC Supply → Voltage/Current Measurement → Electroplating Cell

The ESP32 acquires the voltage and current values and displays/records them.

These values can also be used to identify abnormal operating conditions such as excessive current or voltage fluctuations.

D. pH Monitoring

Hardware:

pH electrode/probe
pH sensor/transmitter/interface module
ESP32
Electrolyte tank
Display

Connection:

pH Probe → pH Interface Module → ESP32 → Display

The pH probe measures the electrolyte condition. The signal-conditioning/interface module converts the probe signal into a form that the ESP32 can read.

For your project, the actual pH values obtained during calibration/testing should be recorded experimentally rather than assumed.

E. Solenoid Valve System

You have two solenoid valves:

Solenoid Valve 1 – Boric Acid Dosing

Connected between the boric-acid reservoir and electrolyte tank.
Used to introduce boric acid when required.

Solenoid Valve 2 – Electrolyte Outlet

Connected to the electrolyte discharge line.
Used to outlet/discharge electrolyte. F. ESP32 Control Unit

The ESP32 acts as the main controller.

It receives:

Temperature information
pH measurement
Voltage measurement
Current measurement
Level/status signals
Potential coating-quality measurement

And controls:

Solenoid Valve 1
Solenoid Valve 2
Heater/control output
Display/monitoring interface
Alarm indicators

### Software Implementation

2. Software Implementation
A. ESP32 Programming

The main software can be developed using:

Arduino IDE + Embedded C/C++

The program will:

Initialize all sensors and outputs.
Read sensor values.
Convert raw sensor signals into engineering values.
Compare measurements with setpoints/limits.
Operate actuators accordingly.
Display the current process status.
Repeat the monitoring cycle continuously.

Basic software flow:

START
  ↓
Initialize ESP32
  ↓
Initialize Sensors
  ↓
Read Temperature
  ↓
Read pH
  ↓
Read Voltage & Current
  ↓
Check Process Conditions
  ↓
Control Heater / Solenoid Valves
  ↓
Display Parameters
  ↓
Check Alarm Conditions
  ↓
Repeat
3. Temperature Control Software

You can implement a simple control algorithm:

Read Temperature
       ↓
Temperature < Setpoint?
    ↙          ↘
  YES           NO
   ↓             ↓
Heater ON     Heater OFF

If you are using a commercial temperature controller, the temperature-control algorithm itself can remain inside that controller, while the ESP32 only monitors the temperature.

4. pH Control Software

Your system can use threshold-based control:

Read pH
   ↓
Compare with allowable range
   ↓
Abnormal?
 ↙       ↘
YES       NO
 ↓         ↓
Control   Keep valves
valves    in normal state

For your boric-acid-only system, the software should not be written as a conventional acid/base dosing system. It should specifically account for:

pH measurement → control decision → boric acid dosing / electrolyte outlet → re-measurement

The exact pH limits should come from the nickel-plating chemistry you're using and your experimentally established operating range.

5. Voltage & Current Software

The ESP32 periodically reads the measurement modules:

ADC Reading
     ↓
Calibration/Conversion
     ↓
Voltage / Current Value
     ↓
Display
     ↓
Data Logging / Alarm

You can also calculate electrical power:

P = V × I

where:

P = electrical power
V = voltage
I = current

This gives you another useful parameter for your project analysis.

6. Coating Quality Software

For the eddy-current-based coating measurement, the software architecture can be:

Eddy Current Sensor
        ↓
Signal Conditioning
        ↓
ADC
        ↓
ESP32
        ↓
Calibration Curve
        ↓
Estimated Coating Thickness
        ↓
Quality Status

You would first need experimental calibration using samples with known coating thicknesses. The ESP32 can then use the resulting calibration relationship to estimate coating thickness.

7. Data Display / Monitoring

For the final system, you can have a simple display showing:

Parameter	Display
Temperature	°C
pH	pH value
Voltage	V
Current	A
Coating thickness	µm
Anode health	% / status
Valve status	ON/OFF

You could use either an OLED/LCD connected to the ESP32 or a computer/mobile dashboard if you want remote monitoring.

8. Hardware vs Software — PPT-Friendly Summary
Hardware	Software
Electroplating tank	Arduino IDE
Nickel anode & cathode	Embedded C/C++
Temperature sensor	Sensor-reading programs
Temperature controller	Temperature control logic
Heater	pH monitoring algorithm
pH sensor	Voltage/current conversion
Voltage sensor	Current monitoring
Current sensor	Solenoid control logic
Eddy-current sensor	Coating-thickness calculation
ESP32	Alarm/threshold logic
Solenoid valves	Data display
Relay/MOSFET drivers	Data logging
Display	Calibration algorithms
DC power supply	System integration
Overall implementation

Hardware layer:

Sensors + Electroplating Cell + ESP32 + Drivers + Valves + Heater + Display

Software layer:

Sensor acquisition + Calibration + Monitoring + Decision Logic + Actuator Control + Display/Data Logging

---



## Testing and Results

| Test No. | Test Description       | Expected Result                           | Actual Result | Status      |
| -------- | ----------------       | ---------------                           | ------------- | ----------- |
| 1        | Temperature loop check | Relay response according to set point     | Working       | PASS        |
| 2        | Current loop check     | Current module working according to input | Working       | PASS        |               
| 3        | pH Loop check          | Solenoid valve on/off - acid dosing       | Working       | PASS        |

---

## Result Images / Videos

Add images or videos of the working prototype.

```markdown
![Prototype](images/prototype_photo.jpg)
```

Video Link: https://youtu.be/6FQ77SdycFc?feature=shared

```markdown
[Project Demo Video](https://drive.google.com/your-video-link)
```

---

## Applications

Mention real-world applications of the project.

1.
2.
3.
4.

---

## Advantages

1.
2.
3.
4.

---

## Limitations

1.
2.
3.
4.

---

## Future Scope

Mention possible improvements.

1.
2.
3.
4.

---

## Research Paper / Publication

| Item                      | Details                                                   |
| ------------------------- | --------------------------------------------------------- |
| Paper Title               |                                                           |
| Conference / Journal Name |                                                           |
| Paper Status              | Not Started / Drafting / Submitted / Accepted / Published |
| Submission Date           |                                                           |
| Paper Link                |                                                           |

---

## References

Add references in IEEE format.

Example:

```text
[1] A. Author, B. Author, "Title of the Paper," Journal/Conference Name, vol. X, no. Y, pp. xx-yy, Year.
[2] Datasheet / Website / Book reference.
```

---

## Repository Update Guidelines

Each student team must update the GitHub repository regularly.

Minimum expected updates:

* Update README every week.
* Push code changes regularly.
* Upload circuit diagrams, CAD files, PCB files, reports and presentations.
* Add weekly progress in the progress table.
* Maintain proper folder structure.
* Do not upload unnecessary temporary files.
* Each major update should have a meaningful commit message.

Example commit messages:

```text
Added problem statement and objectives
Updated system architecture diagram
Added sensor interfacing code
Updated weekly progress for Week 3
Added testing results and prototype images
```

---

## Declaration

We declare that this project work is carried out by our team as part of the BE Capstone Project. The work will be regularly updated on GitHub and all references used will be properly cited.

---

## License

This project is for academic use only.

Optional:

```text
MIT License / Creative Commons / Institute Use Only
```

```
```
