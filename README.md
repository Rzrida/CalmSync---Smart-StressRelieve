# CalmSync - Smart-StressRelieve


StressRelievee is a semi-automated wearable device designed to help users manage stress through heart rate monitoring and vibrotactile feedback. Developed using the ESP32 microcontroller, this prototype provides real-time calming vibrations in response to elevated heart rates, promoting a relaxed state. The system features Bluetooth Low Energy (BLE) communication with a mobile app for manual or automatic operation.

<img width="367" alt="Screenshot 2025-06-04 at 10 41 23 PM" src="https://github.com/user-attachments/assets/75b6cb82-58b0-4320-9af6-6afbfa3d4783" />


## Features
- **Heart Rate Monitoring:** Detects elevated heart rates using a MAX30100 sensor.
- **Vibrotactile Feedback:** Activates a vibration motor to guide breathing into a calmer rhythm.
- **Bluetooth Communication:** BLE connectivity for real-time data transfer and device control.
- **Mobile App Integration:** Provides manual mode, intensity adjustments, and heart rate tracking.
 <img width="476" alt="Screenshot 2025-06-04 at 10 38 30 PM" src="https://github.com/user-attachments/assets/f1b015fc-d95f-4461-8a6f-1685f09359de" />

- **Semi-Automated System:** Offers both manual and automatic intervention modes.
- **Machine Learning:** Implements predictive stress detection using trained models.

## Components Used
### Hardware
- **ESP32 WROOM-32**: WiFi + Bluetooth microcontroller
- **MAX30100 Sensor**: Heart rate and pulse oximeter sensor
- **Vibration Motor**: Coin motor for tactile feedback
- **300mAh 3.7V 1S LiPo Battery**: Power source
- **Veroboard**: For circuit assembly

### Software
- **Arduino IDE**: For microcontroller programming
- **Wokwi Simulator**: For hardware simulation
- **nRF Connect**: BLE mobile app for control and testing
- **Flask**: Backend for data processing
- **TinyML (planned)**: For on-device ML inference

## System Overview
The device continuously monitors heart rate and compares it against predefined thresholds. Upon detecting elevated levels, it triggers the vibrotactile feedback mechanism to guide the user into a calmer state. The mobile app enhances user experience by offering customization and real-time feedback.

### Workflow
1. **Heart Rate Detection**: Sensor data is processed by the ESP32.
2. **Feedback Activation**: Vibrotactile motor is triggered based on stress levels.
3. **User Interaction**: BLE-enabled mobile app allows real-time control and monitoring.
4. **ML Integration**: Predictive models classify stress levels (future implementation).

<img width="453" alt="image" src="https://github.com/user-attachments/assets/1890c588-5dcc-4913-8e38-71e557f84456" />

<img width="503" alt="image" src="https://github.com/user-attachments/assets/8d61d658-68ed-4dec-a670-ac94555dc03b" />

## Installation
### Prerequisites
1. Arduino IDE installed.
2. ESP32 board configuration in Arduino IDE.
3. Required libraries:
   - MAX30100_PulseOximeter
   - BLEDevice
   - BLEServer


## Testing
1. Simulate heart rate using Wokwi.
2. Validate BLE communication by observing real-time data in the app.
3. Test vibrotactile feedback by manually triggering stress conditions.

## Challenges and Solutions
- **BLE Instability:** Optimized BLE intervals for stable communication.
- **Testing Constraints:** Used simulated sensor data for initial testing.
- **Simultaneous BLE and WiFi Issues:** Planned TinyML deployment to avoid WiFi dependency.

## Future Enhancements
1. Deploy ML models on ESP32 using TinyML.
2. Integrate Inertial Measurement Unit (IMU) sensors for better stress detection.
3. Improve the app with advanced features like historical data visualization.
4. Develop a compact and ergonomic hardware casing.


