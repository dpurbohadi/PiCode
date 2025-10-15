# picode-lms
AI-supported live coding and IoT learning module integrated with Moodle LMS

**archiceture**

<img src="Documentation/Architecture.png" alt="Ilustrasi Irigasi" width="600"/>

**System Architecture**

The system integrates an LMS (Moodle), IoT devices, and an AI feedback module through a secure VPN connection.
The diagram below illustrates the architecture of the AI-supported live coding and IoT learning environment.

**Description**

Greenhouse IoT Devices
The system includes IoT sensors (e.g., temperature, humidity, and light sensors) and actuators (e.g., servo-based irrigation systems) installed in a greenhouse. These devices collect environmental data and execute commands received from the LMS.

**TailScale VPN**
Provides a secure, encrypted network that connects all IoT devices with the LMS and servers through the internet. This ensures real-time communication and remote access while maintaining data privacy.

**Internet Layer**
Acts as the communication backbone, linking the LMS, IoT network, and AI feedback module. It enables data flow between students’ activities in the LMS and physical IoT responses in the greenhouse.

**Moodle (LMS)**
Hosts the PiCode Lab live coding environment, where students can write and execute code directly from the browser. The LMS manages user sessions, logs, and integration with SCORM packages.

**Programming Tools**
Embedded within the LMS, these tools allow students to develop control scripts, run code, and observe feedback in real time. The module logs each interaction for later analysis.

**Data Logger Server**
Receives and stores sensor readings from IoT devices. It also forwards relevant data to the LMS and supports synchronization for monitoring and evaluation.

**OpenAI API (Feedback Module)**
Processes student-submitted code and provides automated feedback through GPT-based analysis. It acts as a virtual instructor that evaluates logic, syntax, and coding efficiency.

System Flow :

  - The student writes and runs code in the LMS-based editor.
  - The LMS sends the command to IoT devices via the VPN network.
  - Sensors collect data and actuators respond accordingly.
  - The data logger records all activity and sends updates to the LMS.
  - The OpenAI API provides AI-generated feedback to guide student learning.

