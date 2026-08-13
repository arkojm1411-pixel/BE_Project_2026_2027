````markdown
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

| Sr. No. | Component | Specification | Quantity | Purpose |
| ------- | --------- | ------------- | -------- | ------- |
| 1       |           |               |          |         |
| 2       |           |               |          |         |
| 3       |           |               |          |         |
| 4       |           |               |          |         |

---

## Software Requirements

| Sr. No. | Software / Tool | Version | Purpose |
| ------- | --------------- | ------- | ------- |
| 1       |                 |         |         |
| 2       |                 |         |         |
| 3       |                 |         |         |

---

## Technologies Used

Mention technologies used in the project.

Example:

* Embedded C / Python / JavaScript
* Arduino / STM32 / ESP32 / Raspberry Pi
* ROS / MATLAB / Simulink
* Machine Learning / Computer Vision
* IoT / Cloud / Mobile App
* PCB Design / CAD Design

---

## Methodology

Explain the step-by-step approach.

1. Literature survey
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
| Week 1       | Problem finalization  | Pending / In Progress / Completed |
| Week 2       | Literature survey     |                                   |
| Week 3       | Requirement analysis  |                                   |
| Week 4       | System design         |                                   |
| Week 5       | Prototype development |                                   |
| Week 6       | Testing               |                                   |
| Week 7       | Documentation         |                                   |
| Week 8       | Paper writing         |                                   |

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

---

## Design Files

Upload and link all design files here.

| File Type       | File Name / Link | Description |
| --------------- | ---------------- | ----------- |
| CAD Model       |                  |             |
| Circuit Diagram |                  |             |
| PCB Design      |                  |             |
| Flowchart       |                  |             |
| Simulation File |                  |             |

---

## Circuit Diagram

Add circuit diagram image here.

```markdown
![Circuit Diagram](images/circuit_diagram.png)
```

---

## Flowchart / Algorithm

Add flowchart image here.

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

Explain the actual implementation of the project.

### Hardware Implementation

Write details about connections, components, power supply, sensors, actuators, PCB, enclosure, etc.

### Software Implementation

Write details about code structure, libraries used, algorithms, communication protocols, database, app, cloud, etc.

---

## Code Structure

```text
BE-Capstone-Project/
│
├── README.md
├── docs/
│   ├── literature_survey.md
│   ├── project_report.pdf
│   └── presentation.pptx
│
├── hardware/
│   ├── circuit_diagram.png
│   ├── pcb_design/
│   └── cad_model/
│
├── software/
│   ├── src/
│   ├── include/
│   └── tests/
│
├── images/
│   ├── system_architecture.png
│   ├── prototype_photo.jpg
│   └── results.png
│
└── references/
    └── papers/
```

---

## How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/username/project-name.git
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

or mention specific software/library installation steps.

### Step 3: Upload / Run the Code

```bash
python main.py
```

or

```bash
arduino-cli upload -p COMx --fqbn board_name
```

### Step 4: Observe the Output

Mention the expected output of the project.

---

## Testing and Results

| Test No. | Test Description | Expected Result | Actual Result | Status      |
| -------- | ---------------- | --------------- | ------------- | ----------- |
| 1        |                  |                 |               | Pass / Fail |
| 2        |                  |                 |               | Pass / Fail |
| 3        |                  |                 |               | Pass / Fail |

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
