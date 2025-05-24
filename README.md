
# Umit-interactive-mouthguard
Okay, this is an impressive and well-documented project! Based on your detailed report, here's a README.md for your GitHub repository. I've tried to capture the essence and key details.

# Úmit: AI-Powered Interactive Mouthguard for Assistive Control

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Project Status: Active Development](https://img.shields.io/badge/status-active-success.svg)](https://github.com/your-username/umit-project) <!-- Replace with your actual repo link -->

**Úmit** (Kazakh for "Hope") is an innovative assistive technology project developed by students from the Nazarbayev Intellectual School of Physics and Mathematics in Taraz. It's an AI-integrated interactive mouthguard system designed to empower individuals with severe motor disabilities by enabling them to control digital devices (smartphones, computers, IoT) and electric wheelchairs using head and tongue movements.

---

**Authors:** Tazhikhan Kanat, Zhazykbay Ali, Kaldybay Baryskhan (12 "D")
**Mentor:** David Tuganov
**Scientific Supervisor:** Daulet Magzymov, Ph.D., University of Houston
**Institution:** "Nazarbayev Intellectual Schools" AEO, Nazarbayev Intellectual School of Physics and Mathematics in Taraz


---

## Table of Contents

1.  [Abstract](#abstract)
2.  [The Problem](#the-problem)
3.  [Our Solution: Úmit](#our-solution-úmit)
4.  [Key Features](#key-features)
5.  [How It Works](#how-it-works)
    *   [Hardware Components](#hardware-components)
    *   [Control Mechanism](#control-mechanism)
    *   [AI Integration](#ai-integration)
    *   [Wheelchair Interface](#wheelchair-interface)
6.  [Technology Stack](#technology-stack)
7.  [Project Journey & Methodology Highlights](#project-journey--methodology-highlights)
8.  [Results & Impact](#results--impact)
9.  [Practical Applications](#practical-applications)
10. [Demonstration & Visuals](#demonstration--visuals)
11. [Future Development](#future-development)
12. [Acknowledgments](#acknowledgments)
13. [License](#license)
14. [Contact](#contact)

## Abstract

Limited employment, educational opportunities, and digital access are significant challenges for people with disabilities, often leading to reliance on others. The Úmit project addresses this by developing an interactive mouthguard system that allows users to control digital devices and wheelchairs through preserved head and tongue movements, enhanced by Artificial Intelligence. Our research confirmed that 90% of individuals with conditions like paralysis, stroke, and cerebral palsy retain tongue movement, and 78% retain head mobility. The Úmit device leverages these capabilities, offering an intuitive, wireless, biocompatible, and cross-platform solution. Experimental testing showed a 46% increase in users' digital potential within one week, significantly enhancing independence and quality of life.

## The Problem

In Kazakhstan, and globally, individuals with disabilities face significant barriers:
*   **Limited Access to Technology:** Only a small percentage (e.g., 5% in Kazakhstan) have access to adapted digital devices.
*   **Employment & Education Gaps:** High unemployment rates (e.g., 83% in Kazakhstan) and low higher education enrollment among people with disabilities.
*   **Mobility Challenges:** Dependence on external assistance for mobility and daily tasks.
*   **Existing Assistive Tech Limitations:** Current solutions can be invasive (e.g., Neuralink), limited in functionality (e.g., specific to gaming like QuadStick), expensive, require specific conditions (e.g., eye-tracking), or have usability issues.

Our research in Taraz rehabilitation centers confirmed these challenges, with many individuals unable to use standard input devices due to motor impairments, despite retaining head and tongue control.

## Our Solution: Úmit

Úmit is an interactive mouthguard that translates head tilts and tongue pressure into control signals for digital devices and electric wheelchairs. It acts like a wireless, hands-free mouse, augmented with AI to learn user behavior and improve efficiency.

## Key Features

*   **Hands-Free Control:** Utilizes head and tongue movements, bypassing the need for hand dexterity.
*   **AI-Powered:** Integrated neural network learns user patterns, predicts movements, and adapts for smoother, more intuitive control.
*   **Universal Compatibility:** Designed to control any digital device (smartphones, computers, IoT) and electric wheelchairs via Bluetooth (HID profile).
*   **Non-Invasive & Biocompatible:** Made from hypoallergenic, biocompatible plastic, ensuring safety and comfort for long-term use.
*   **Wireless & Portable:** Compact design with Bluetooth connectivity and a rechargeable battery (Type-C).
*   **Intuitive Operation:** Gyroscope for head tracking (cursor movement) and force sensors for tongue pressure (clicks, directional commands).
*   **Customizable:** Sensitivity and button functions can be adjusted to individual user needs.

## How It Works

### Hardware Components
The Úmit mouthguard houses:
1.  **Custom Umit Microchip:** Based on Nordic nRF52840 (ARM® Cortex®-M4 with FPU), featuring a built-in 6 DOF IMU (LSM6DS3TR-C).
2.  **6 DOF IMU (LSM6DS3TR-C):** Tracks head orientation (pitch, yaw) for cursor or wheelchair movement.
3.  **Force Sensors (Strain Gauges & Tactile Switches):**
    *   Four strain gauges detect tongue pressure in different directions (up, down, left, right) for navigation or custom commands.
    *   Two force buttons at occlusion zones act as left/right mouse clicks.
4.  **Rechargeable Battery:** Powers the device.
5.  **Type-C Port:** For charging and reprogramming.
6.  **Bluetooth Antenna:** For wireless communication.
7.  **Biocompatible Plastic Casing:** Securely encloses all components.

*(Refer to Figure 9-18 in the project report for 3D models and device assembly visuals)*

### Control Mechanism
1.  **Head Movement:**
    *   Tilting the head forward/backward moves the cursor up/down or the wheelchair forward/backward.
    *   Tilting the head left/right moves the cursor or steers the wheelchair left/right.
    *   Initial calibration sets the neutral head position.
2.  **Tongue Movement:**
    *   Pressing the tongue against strategically placed force sensors can trigger clicks, scroll, navigate menus, or issue specific commands.
3.  **Tactile Buttons:**
    *   Gentle biting on force buttons simulates left/right mouse clicks.
    *   Long presses can switch modes or power off the device.

*(Refer to Figure 24-27 in the project report for diagrams of the principle of operation)*

### AI Integration
A lightweight neural network runs on the Umit microchip:
*   **Processes Sensor Data:** Analyzes real-time data from the gyroscope and force sensors.
*   **Pattern Recognition:** Learns individual user's movement patterns and common actions.
*   **Predictive Assistance:** Can predict intended cursor movements or commands, reducing physical effort.
*   **Noise Filtering:** Differentiates intentional movements from involuntary twitches or tremors.
*   **Adaptive Learning:** Continuously improves accuracy and responsiveness based on user interaction.

*(Refer to Figure 22-23 in the project report for AI training insights)*

### Wheelchair Interface
The Úmit mouthguard connects via Bluetooth (BLE) to a controller (e.g., ESP8266 or Arduino) integrated with an electric wheelchair (prototype used a modified hoverboard platform).
*   **Mode Switching:** Users can switch between digital device control and wheelchair control mode.
*   **Commands:** Head tilts and tongue presses are translated into 'Forward', 'Backward', 'Left', 'Right' commands for the wheelchair.

*(Refer to Figure 19-21 in the project report for wheelchair control details)*

## Technology Stack

*   **Hardware:**
    *   Microcontroller: Custom Umit microchip (Nordic nRF52840 SoC with ARM Cortex-M4)
    *   Sensors: 6 DOF IMU (LSM6DS3TR-C), Force-Sensitive Resistors (FSRs)/Strain Gauges, Tactile Switches
    *   Connectivity: Bluetooth Low Energy (BLE)
    *   Power: Rechargeable Li-ion battery, Type-C charging
    *   Casing: Hypoallergenic, biocompatible plastic
*   **Software & AI:**
    *   Firmware: Embedded C/C++ for the nRF52840
    *   AI Model: Lightweight feed-forward neural network (trained possibly with TensorFlow/PyTorch, deployed on-device)
    *   3D Modeling: Blender (for device casing design)
    *   Wheelchair Interface: Arduino/ESP8266 programming

## Project Journey & Methodology Highlights

1.  **Problem Identification:** Analytical review of existing tech and expeditions to Taraz rehabilitation centers to understand user needs.
2.  **Physiological Research:** Determined that head and tongue movements are largely preserved in individuals with severe motor disabilities.
3.  **Design & Prototyping:**
    *   Dental cast acquisition for anatomical accuracy.
    *   3D modeling in Blender for component placement.
    *   Fabrication of a two-layer biocompatible casing using vacuum forming.
    *   Circuit design and soldering of the Umit microchip and sensors.
4.  **AI Development:** Data collection, preprocessing, and training of a custom neural network for intuitive control.
5.  **Wheelchair Integration:** Developed an interface to control an electric wheelchair platform.
6.  **Testing & Validation:** Conducted experiments with users (e.g., Danial at "Bөbekzhai" rehabilitation center) to evaluate effectiveness and gather feedback.

## Results & Impact

*   **Preserved Mobility:** Confirmed that ~90% of individuals with disabilities retain tongue movement and ~78-85% retain head mobility.
*   **Improved Digital Access:** Experimental testing showed a **46% increase in digital potential** (confidence and ability) within one week of use.
*   **User Empowerment:** Positive feedback from test users like Danyal, who stated, "With this device, I can easily interact with digital technologies... I believe I can use these skills to earn money."
*   **Enhanced Independence:** Reduces reliance on caregivers for digital tasks and mobility.
*   **Potential for Socio-Economic Inclusion:** Facilitates access to education, remote work (e.g., programming, design), and communication.

*(Refer to Diagram 2 and Figure 28 in the project report for results and user feedback)*

## Practical Applications

The Úmit system has wide-ranging applications:
*   **Assistive Technology:** For individuals with cerebral palsy, paralysis, stroke, spinal muscular atrophy, etc.
*   **Education & Employment:** Enabling access to learning platforms and digital job opportunities.
*   **Specialized Professions:** Potential use in environments requiring hands-free control (e.g., medicine, engineering, diving, space missions).
*   **Gaming & Esports:** Offering an alternative control method for accessible gaming.
*   **Rehabilitation Centers & Special Education:** A tool for therapy and skill development.

## Demonstration & Visuals

*(This section is a placeholder. We encourage you to add GIFs, images, or a link to a demo video showcasing Úmit in action.)*

For detailed diagrams, 3D models, and photos from the project development, please refer to the figures and appendices in our full project report.
*   Device 3D Models: Figure 9, 10, 11
*   Prototyping Process: Figure 12-17
*   Completed Device: Figure 18
*   Wheelchair Integration: Figure 19-21
*   Principle of Operation: Figure 24-27
*   User Testing: Figure 28, Appendices

## Future Development

Based on our findings and recommendations:
*   **Multi-Platform Compatibility:** Develop robust firmware and companion apps for iOS, Windows, Linux, and Android.
*   **Adaptive User Interfaces:** Customizable control schemes for various software and personalized sensitivity settings.
*   **Enhanced Connectivity:** Advanced Bluetooth/Wi-Fi for smart home integration.
*   **Sensory Feedback:** Incorporate voice or haptic feedback for guidance.
*   **Advanced Bio-Sensing & AI:** Explore additional biometric sensors and further refine AI for even more precise user-specific behavior learning.
*   **Miniaturization & Aesthetics:** Continue to refine the design for comfort and discretion.

## Acknowledgments

We extend our sincere gratitude to:
*   Our mentor, **David Tuganov**, and scientific supervisor, **Daulet Magzymov, Ph.D.**
*   **Nazarbayev Intellectual School of Physics and Mathematics in Taraz** for their support.
*   The rehabilitation centers in Taraz, especially **"Bөbekzhai"**, and participants like **Danial** for their invaluable feedback and involvement.
*   Organizations that have recognized and supported our project, including **Microsoft, AMD, Samsung, and Red Bull**.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
*(You'll need to create a LICENSE.md file with the MIT license text if you choose this license.)*

## Contact

For any inquiries, please reach out to:
*   Tazhikhan Kanat: `[your_email_or_github_profile_kanat]`
*   Zhazykbay Ali: `[your_email_or_github_profile_ali]`
*   Kaldybay Baryskhan: `[your_email_or_github_profile_baryskhan]`

Or open an issue in this repository.

---

We believe Úmit holds the potential to significantly improve the lives of many individuals, fostering independence and inclusion in the digital world.


Next Steps for You:

Create the Repository: On GitHub, create a new repository for "Úmit".

Add README.md: Copy the text above into a file named README.md in your repository.

Replace Placeholders:

Update the repository link: [![Project Status: Active Development](https://img.shields.io/badge/status-active-success.svg)](https://github.com/your-username/umit-project)

Add your contact emails or GitHub profile links.

Add a LICENSE.md file: If you choose MIT, you can easily find the standard MIT license text online and paste it into a LICENSE.md file.

Upload Project Files: Add your code, design files (if you plan to share them like 3D models, schematics), and the full project report PDF to the repository. You might want to organize these into folders (e.g., /firmware, /hardware_design, /documentation).

Add Visuals:

Consider creating a short GIF or video demonstrating the device and embedding it or linking to it.

You can embed images directly in the README if they are in your repository. For example: ![Umit Device Prototype](path/to/your/image_in_repo.jpg)

Commit and Push: Save your changes and push them to GitHub.

This README provides a solid foundation. You can always update and expand it as your project evolves! Good luck!
