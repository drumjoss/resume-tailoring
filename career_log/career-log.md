# EXP-007 — Kal Engineering Studio — Freelance Embedded Engineer
**2024 – Present**

## Context
Freelance activity focused on embedded systems development and system architecture for industrial and connected devices. My interventions cover both firmware development, high-level and hardware/software system design.

## Responsibilities
- Design and implementation of embedded software solutions in C/C++.
- Definition of hardware/software architectures for new systems, including components selection.
- Contribution across full development lifecycle, from specification to industrialization.

## Achievements / Work

### Embedded Development
- Ported a **C** embedded software application for a handheld radio-based indoor localisation system adding new features, for instance firmware update and robustified lone worker safety mechanism. Initial target was an AT32 (AVR32), and the new one a SAM4S (ARM Cortex-M4), causing endianess issues.
- Refactored a full project to streamline product line maintenance and update costs, including porting to a **CMake** compatible toolchain and **FreeRTOS**.
- Designed and implemented a portable lone worker alert mechanism based on accelerometer and gyroscope data.
  [tags: c, embedded-software, indoor-localization, firmware-update, cmake, sensors, imu]

### System Architecture
- Defined the hardware/software architecture for robust operation and product evolution future-proofing.
  [tags: system-architecture, embedded-system, real-time, safety-critical]

### Validation, Testing and Industrialization
- Created integration tests to simulate back-end operations in **node.js**, with the emulated back-end running on a **Raspberry Pi 3**/**Zero W**.
- Ubuntu 24 and Windows 11 VM Creation and management to configure and use the product.
- Created a hardware test device to simulate alert cases, driven by **node.js** tests sequencing and running on a **Arduino UNO R4 WiFi**, and on a **Raspberry Pi Zero W** with **Python** **Flask**.
- Proof of concept of a Yocto based autonomous robot for indoor localization algorithm validation.
  [tags: test-automation, hardware-test-bench, nodejs, raspberry-pi, arduino, yocto, backend-integration]


---

# EXP-006 — Netatmo — Embedded Engineer
**2018 – 2024**

## Context
I was part of the Embedded Software Engineer team, composed by 25 engineers, grouped by product lines and technological stacks.
On each project ie one product applicative, the embedded software team represented 1 to 3 people on average.

## Responsibilities
- Embedded software development from prototype to industrialization.
- End-to-end System design involving embedded, mobile, and backend components.
- Hardware characterization, validation, performance and endurance testing.
- Prepare and/or perform the required certifications depending on the target product: RED, CE, Apple-Homekit.
- Product specification discussion with Product Management team.

## Achievements / Work

### Embedded Development
- Developed firmware in **C** for a HomeKit-compatible smart door lock using **BLE** and **NFC** on an **nrf52** (ARM Cortex-M4) with **FreeRTOS**, taking the product from proof of concept to mass production. The build was handled by plain **Make**.
- Designed and implemented a low-power **NFC** tag detection algorithm.
- Designed and implemented a robust real-time DC motor calibration and control algorithm.
- Developed **C/C++** Software for an **Ambarella**/**Buildroot**-based indoor camera.
  [tags: c, embedded-software, ble, nfc, homekit, real-time, low-power]

### Cybersecurity
- Specified a bootloader with firmware integrity check with ciphered and authenticated application update mechanism based on **ED25519**, **Poly1305-Chacha20** and **HMAC-SHA256** algorithms. This bootloader also had a swap mechanism preventing the product to brick with a malicious firmware update.
- Designed and implemented cryptographic keys storage with a **SAM Av2**, which is a **Common Criteria** certified secure element, along with the factory key provisioning process.
- Designed and implemented a hardware based security to prevent an unauthenticated user to perform action on the product: actuation components are disabled until a succesful authentication is done, this prevent a malicious actor to unlock the smart door lock.
- Designed and implemented a physical authentication mechanism to lock certain product administration feature, for example to manage the smart door lock keys.
- Supervised penetration testing campaigns, including one performed by a third-party company.
  [tags: cybersecurity, secure-boot, firmware-update, secure-element]

### System Architecture
- Participated in the product system architecture covering embedded device, mobile apps (iOS/Android), and backend services to implement end-user scenarios such as temporary guest invitation for the smart door lock, along with maintenance features: secure firmware update with Azure and products fleet remote diagnosis with Kibana.
  [tags: system-architecture, embedded-system, iot, firmware-update, backend-integration]

### Validation, Testing and Industrialization
- Developped a test suite with **PyQt** to validate product reliability in the long term: endurance testing, mechanical aging and recalibration handling.
- Wrote factory scripts in **Python** to handle the smart door lock product initial configuration to be used by the factory in China, including the secure key provisioning.
- Carried multiple certification processes:
  - Ran all the tests required for the Apple-Homekit certification.
  - Developped specific firmwares for the CE certification concerning **BLE** and **NFC**.
  - Taken into account RED certification requirements for hardware validation.
- Conducted hardware validation on an **Ambarella**/**Buildroot**-based indoor camera: the goal was to validate the usage of a new higher resolution image sensor, and check if the current CPU would handle the extra computation needed.
- Tailored and fine-tuned an indoor camera Echo-cancellation algorithm to new mechanical constraints, with the support of the CODEC supplier AKM.
  [tags: test-automation, ci-cd, hardware-validation, endurance-testing, hardware-test-bench, python, certification, buildroot, linux]


---

# EXP-005 — Somfy — Software Engineer (Technical Department)
**2016 – 2018**

## Context
I was working in Somfy Technical Departement, a newly created entity whose goal was to enable new technologies, tools and processes for the different Somfy Buisiness Units.
The Technical Department Software team was initially constituted by 4 software engineers, but could reach up to 10 engineers for big architecture phase, spread over 3 R&D centers including 2 in France and 1 in Poland.

## Responsibilities
- Provide Somfy Buisiness Units with reusable software architecture and modules.
- Ensure the application of Software development processes and rules across all the Buisiness Units.
- Support software processes evolutions with new tools and test philosophy.
- Training and supporting of the newcomers.

## Achievements / Work

### Software Architecture
- Designed a generic UML-based software architecture for IoT actuators thanks to the **Rhapsody** tool, with a focus on protocol abstraction and interoperability while taking into account protocols such as Zigbee, Thread, and Somfy proprietary protocols io-homecontrol and RTS. Hiogh-level requirements were summarized in Reqtify.
- Handled specific code generation in **C/C++** and compiled with **IAR** to integrate this architecture into a solar-powered roller shutter system.
  [tags: system-architecture, uml, embedded-software, iot, low-power]

### IoT & Standards
- Contributed to interoperability efforts, including work with the Zigbee Alliance to contribute to the ZigBee Cluster Library specification.
  [tags: iot, zigbee, interoperability]

### Test Automation & CI-CD
- Implemented **Jenkins**-based automated unit and integration testing with strict coverage requirements using **Gcov**.
- Ran automated Static-Analysis (LDRA, CodeSonar) on different projects, adding new tools support including for example **CppCheck**.
- Developed automated physical test benches using **Gherkins** as high-level tests description and implemented in **Python**/**Lua**.
  [tags: jenkins, gcov, python, hardware-test-bench, test-automation, ci-cd, static-analysis]

### Process Application
- Participated in the transition from waterfall to **Agile** (**Scrum**/**Kanban**)
- Contributed to several newcomers groups training about Testing/Coding rules and good practices.
- Contributed to multiple Buisiness Units projects code and design formal reviews.
  [tags: agile, scrum, process, kanban]


---

# EXP-004 — Agixis (for Somfy) — Development Engineer
**2015 – 2016**

## Context
Consulting role within Somfy Technical Department, focused on low-level embedded development across a wide range of products (actuators, remotes, sensors), many with strong low-power constraints: up to 10-year battery life.

## Responsibilities
- Development of critical embedded software layers.
- Integration into multiple product lines simultaneously.
- Application of the software development process and rules.
- Coordination with internal client and offshore subcontractor teams.

## Achievements / Work

### Embedded Development
- Developed critical software components in **C** on **STM32** and **EFM32** platforms: RTOS abstraction layers, motor control, and flash memory management, with IAR IDE and Compiler.
- Created a benchmark software for new MCU qualification, using **µcos-II** as RTOS, which serves as a template for application development.
- Managed Software requirements with **Reqtify**, based on the different buisiness units needs, and proposed software design in **UML** under Rhapsody.
  [tags: c, embedded-software, stm32, efm32, rtos, motor-control]

### Product Integration
- Delivered technical support for the software components integration in more than 15 products including actuators, remote controls, and sensors. It was also integrated in the proprietary io-homecontrol stack, sold to Somfy buisiness partners for their own products.
  [tags: embedded-software, integration, iot, protocol-stack]

### Test Automation & CI-CD
- Performed 100% codeline coverage with automated Unitary tests, scheduled with Jenkins on **Code::Blocks** and using **Gcov** for code coverage measurments.
- Developped Hardware-in-the-loop integration and high-level functionnal tests.
- Ran Static-Analysis tool on every project: **LDRA**, **CodeSonar**.
  [tags: static-analysis, ci-cd, test-automation]

### Coordination
- Handled technical supervision of offshore development for a selection of software modules.
  [tags: outsourcing, coordination]


---

# EXP-003 — Adetel — Embedded Systems Intern
**2015 (5 months)**

## Context
5 months End-of-study internship within the FPGA team of Adetel focused on FPGA-based video systems and embedded Linux integration.

## Responsibilities
- Development of FPGA video interfaces and associated firmware.
- Integration into embedded Linux systems.

## Achievements / Work

### Embedded Development
- Developed **HDMI**/**SDI** interfaces on a **Xilinx Kintex-7** FPGA in **VHDL** and **Verilog**, using the least amount of resource. Few solutions were proposed, varying on specific resources: LUT, PLL, Transceiver, ... Two IDEs were used for synthesis: Vivado Design Suite and Xilinx Platform Studio.
- Wrote corresponding drivers in C on a Microblaze softcore processor.
- Integrated the solution into an embedded Linux **Zynq-7000** platform.
- Creation of an **I²C** EDID memory emulation as certain video sources require valid EDID to send a signal.
  [tags: fpga, xilinx, microblaze, zynq, embedded-system, embedded-software, embedded-linux, video, drivers]


---

# EXP-002 — Thales — Industrial Project
**2014 (7 months)**

## Context
Engineering project at Esisar in a team of 3 students,supervised by Thales Avionics, for signal processing acceleration in satellite positioning systems.

## Achievements / Work
- Studied and improved a complex mathematical algorithm on an System-On-Chip **Zynq-7000** platform. A Step of the GNSS positioning algorithm involves a matrix inversion which can lead to latency and high power-consumption when exclusively performed on a single core CPU.
- Benchmarked ARM Cortex-A9 NEON SIMD hardware acceleration component with CPU implementation **C**.
- Designed and implemented a FPGA based custom hardware computation acceleration component in **VHDL**. **Vivado Design Suite** IDE was used for synthesis.
  [tags: fpga, xilinx, zynq, embedded-system, embedded-software, signal-processing, hardware-acceleration]


---

# EXP-001 — Thales — Internship (Electronics)
**2012 (3 months)**

## Context
Pre-egineering school intership in a team of Electrical Technician on an avionic components production line.

## Achievements / Work
- Conducted Manual production line tests for three-phase power supply systems: Dielectric tests, Voltage Ramp & Stability Test.
- Performed troubleshooting on electronic boards which presented default during production tests or after deployment.
  [tags: electronics, embedded-system, production-testing, troubleshooting]

---


# Personnal Projects
### Google Calendar Powered Clock Alarm
- **Python** Google API and **Raspberry Pi Zero** based Alarm clock that syncs with an online schedule to wake the user.

### Electronic Drum Set
- Teensyduino based **USB MIDI** Device with capacitive and piezoelectric sensors.

### Real-time Audio Processing Platform
- Teensyduino with SGTL5000 CODEC to perform zero latency audio processing.

### Remote Controller Rover with real-time camera monitoring
- **Raspberry Pi Zero W** with Sphero RVR robot base and camera sensor.

### Audio Sanity Check Software
- **TensorFlow** **Python** based Software to detect abnormal noise in recordings.

### Timelapse Server
- **Python** **Flask** based Timelapse server for **Raspberry Pi Zero** with a camera.


---

# Education

## Grenoble INP – Esisar
**2010 – 2015**
Engineering degree in Embedded Systems (Hardware & Software)

## EPFL (Exchange Program)
**2014 – 2015**
Micro and Nanoelectronics


---

# Certifications and Training

## Agile SCRUM
**2016 – 2017**
Agile SCRUM coaching sessions and concrete application.

## Embedded C++
**2017**
Ac6 delivered certification.

## TOEIC®
**2014**
TOEIC® Program certification (940)
