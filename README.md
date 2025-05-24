
# Umit-interactive-mouthguard
Okay, this is an impressive and well-documented project! Based on your detailed report, here's a README.md for your GitHub repository. I've tried to capture the essence and key details.

# Úmit: AI-Powered Interactive Mouthguard for Assistive Control

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Project Status: Active Development](https://img.shields.io/badge/status-active-success.svg)](https://github.com/your-username/umit-project) <!-- Replace with your actual repo link -->

**Úmit** (Kazakh for "Hope") is an innovative assistive technology project developed by students from the Nazarbayev Intellectual School of Physics and Mathematics in Taraz. It's an AI-integrated interactive mouthguard system designed to empower individuals with severe motor disabilities by enabling them to control digital devices (smartphones, computers, IoT) and electric wheelchairs using head and tongue movements.

---

**Authors:** Tazhikhan Kanat, Zhazykbay Ali, Kaldybay Baryskhan 
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
    *   Firmware: Embedded C/C++ for the nRF52840( Mu editor)
    *   AI Model: Tensorboard ( Moving to Edge Impulse platfortm)
    *   3D Modeling: Blender 
    *   Wheelchair Interface: Arduino/ESP8266 programming(STM 32 ST-LINK)

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

![изображение](https://github.com/user-attachments/assets/ea7b7dc1-f58e-47f0-b328-788e76cfd369)


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
*   Device 3D Models:
![изображение](https://github.com/user-attachments/assets/ee50f711-d557-40c4-a397-582f48cc73ff)
![изображение](https://github.com/user-attachments/assets/744a2474-abfd-4317-b6a2-ec6b5a675dd9)
![изображение](https://github.com/user-attachments/assets/b1dc088b-c116-46b1-b196-b161f3976e02)

*   Prototyping Process: 
![изображение](https://github.com/user-attachments/assets/bf737225-bd58-4618-99ae-28fbee6f15c9)
![изображение](https://github.com/user-attachments/assets/a6dd416c-175e-4fc0-bfd8-b542788f13a9)
![изображение](https://github.com/user-attachments/assets/1c4cf5c7-7ec3-4af8-923c-c29a95b3f1e8)
![изображение](https://github.com/user-attachments/assets/6ae48a25-a045-4b2e-9bde-3e1fb0d8cd25)
![изображение](https://github.com/user-attachments/assets/a2e9ff62-2616-4163-9cdc-49202c8816ae)
![изображение](https://github.com/user-attachments/assets/13b43c87-6a20-4ad3-ac3c-bc96e88851d0)
![изображение](https://github.com/user-attachments/assets/4752781f-8f1d-4af6-8639-78b429970b1f)


*   Completed Device: 
   ![изображение](https://github.com/user-attachments/assets/dfbd5d0e-3043-41f5-88e5-81dc84d6bd24)

*   Wheelchair Integration:
 ![изображение](https://github.com/user-attachments/assets/295f7058-67f4-4db1-8f23-a57037d7c9b7)

*   Principle of Operation: 
![изображение](https://github.com/user-attachments/assets/93de70ca-7d6a-4e94-85a3-a88bc3c4f142)
![изображение](https://github.com/user-attachments/assets/455f7ac8-568f-4193-b2d1-9bdc4f72cb8e)
![изображение](https://github.com/user-attachments/assets/f23ca8b0-9f9e-4ffe-82f7-8fc4e555bfab)
![изображение](https://github.com/user-attachments/assets/ca0dba31-bfdc-47df-a3b4-291e1d4d7b20)
![изображение](https://github.com/user-attachments/assets/788e878a-9deb-4393-9f9c-e04e85dd5ddc)
![изображение](https://github.com/user-attachments/assets/b8f889dd-7a5e-4d82-8378-25dce8384f3f)



*   User Testing:
*   ![изображение](https://github.com/user-attachments/assets/b29b6a21-8d73-48d2-9d72-c3bf6c13fddf)


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
![изображение](https://github.com/user-attachments/assets/9be6f3cf-8841-4347-82b5-a8640406116b)
![Uploading изображение.png…]()





Or open an issue in this repository.

---

We believe Úmit holds the potential to significantly improve the lives of many individuals, fostering independence and inclusion in the digital world.



