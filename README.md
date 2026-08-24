# Sigma Controls | IntelliConnect

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-ESP32-red.svg)
![Framework](https://img.shields.io/badge/framework-Arduino-00979D.svg)
![Communication](https://img.shields.io/badge/communication-RS485%20%7C%20Modbus-orange.svg)
![Connectivity](https://img.shields.io/badge/connectivity-Wi--Fi-2196F3.svg)
![Storage](https://img.shields.io/badge/storage-SD%20Card-green.svg)
![License](https://img.shields.io/badge/license-Proprietary-red.svg)

**IntelliConnect** is an industrial wireless data acquisition and connectivity device engineered by **Sigma Controls**. Built around the ESP32 platform, it interfaces with industrial instruments through RS485/Modbus communication, records acquired data locally, and provides wireless access through both existing Wi-Fi networks and a dedicated local Access Point.

Designed as a flexible field-side device, IntelliConnect can be deployed with **Temperature Scanners, PID Controllers, and other industrial process instruments** without being restricted to a single measurement type.

---

### ✨ Key Features & Capabilities

*   **Universal Industrial Interface:** Designed to communicate with multiple industrial instruments including Temperature Scanners, PID Controllers, and process-monitoring equipment through RS485/Modbus communication.

*   **RS485 / Modbus RTU Communication:** Provides reliable serial communication with industrial controllers and scanners using the widely adopted Modbus RTU protocol.

*   **Dual Wi-Fi Operating Modes:** Supports connection to an existing Wi-Fi network as well as standalone **Access Point mode**, allowing direct communication with the device without requiring an external router or Internet connection.

*   **Standalone Data Acquisition:** Performs field-side acquisition independently of the desktop monitoring applications. Data collection can continue locally even when an external network or Internet connection is unavailable.

*   **Local SD-Card Storage:** Acquired process data can be stored directly on an SD card, providing persistent local recording for offline operation and later analysis.

*   **Wireless Device Access:** Provides a wireless interface for accessing and configuring the device from a connected PC, laptop, or other Wi-Fi-enabled device.

*   **Industrial Field Deployment:** Designed for continuous operation alongside industrial instrumentation where reliable acquisition, local storage, and wireless accessibility are required.

*   **Flexible Instrument Support:** The device architecture is not limited to temperature measurement and can be adapted for different industrial process parameters and controller interfaces.

*   **Embedded Processing:** ESP32-based processing handles communication, data acquisition, local storage, and wireless networking directly at the field device.

*   **Sigma Controls Software Integration:** Designed to operate as the field-side acquisition component of the Sigma Controls industrial monitoring ecosystem and work with dedicated desktop applications for Temperature Scanner and PID Controller systems.

---

### 📡 Connectivity & Operating Modes

IntelliConnect provides two primary wireless operating modes:

| Operating Mode | Description | Typical Application |
| :--- | :--- | :--- |
| **Wi-Fi Station Mode** | Connects IntelliConnect to an existing wireless network. | Plant networks, local monitoring, networked installations |
| **Access Point Mode** | IntelliConnect creates its own local Wi-Fi network. | Field configuration, commissioning, diagnostics, direct device access |

The local Access Point capability allows IntelliConnect to remain usable in environments where there is **no existing Wi-Fi infrastructure or Internet connection**.

---

### 🔌 Industrial Communication

IntelliConnect communicates with supported industrial equipment through **RS485-based Modbus RTU communication**.

| Interface | Function |
| :--- | :--- |
| **RS485** | Industrial physical communication interface |
| **Modbus RTU** | Industrial communication protocol |
| **Wi-Fi** | Wireless device connectivity |
| **Local AP** | Direct local wireless access |
| **SD Card** | Local data storage |

The RS485 interface provides the physical connection to the industrial instrument while the ESP32 manages communication, data acquisition, storage, and wireless accessibility.

---

### 🏭 Supported Application Types

IntelliConnect is designed as a general-purpose industrial acquisition platform rather than a temperature-only recorder.

| Application | Example Data |
| :--- | :--- |
| **Temperature Scanner** | Multi-channel temperature measurements |
| **PID Controller** | Process temperature and controller parameters |
| **Pressure Controller** | Pressure measurements |
| **Speed Controller** | Speed / RPM measurements |
| **Humidity System** | Humidity measurements |
| **Process Instrumentation** | Application-specific process parameters |

Additional industrial instruments can be supported by adapting the communication and data-acquisition layer.

---

### 💾 Local Data Recording

IntelliConnect provides local data recording through an SD-card storage interface.

The local recording architecture allows the device to:

*   Acquire data directly from industrial instruments.
*   Store acquired measurements locally.
*   Continue recording without Internet access.
*   Provide recorded data for subsequent analysis.
*   Operate independently from the desktop monitoring applications.

This makes the device suitable for installations where **continuous data acquisition must not depend on Internet availability**.

---

### 🧠 Embedded Processing

The ESP32 acts as the central processing unit for IntelliConnect.

Core responsibilities include:

*   Industrial communication management
*   Modbus RTU data acquisition
*   Process data handling
*   Local data recording
*   SD-card management
*   Wi-Fi communication
*   Access Point management
*   Device-side configuration
*   Wireless data accessibility

The architecture allows field-side acquisition and communication to be performed directly on the embedded device.

---

### 🖥️ Sigma Controls Software Ecosystem

IntelliConnect is designed as the **field-side hardware component** of the Sigma Controls industrial data acquisition ecosystem.

The acquired data can be used with dedicated offline desktop applications depending on the connected industrial equipment.

| Component | Type | Primary Application | Responsibility |
| :--- | :--- | :--- | :--- |
| **IntelliConnect** | Embedded Hardware | Industrial Field Devices | RS485/Modbus acquisition, Wi-Fi connectivity, local AP, and SD-card recording |
| **IntelliScan** | Offline Desktop Software | Temperature Scanners | Temperature data monitoring, visualization, historical analysis, and reporting |
| **IntelliControl** | Offline Desktop Software | PID Controllers | PID/process data monitoring, visualization, configuration, historical analysis, and reporting |

---

### 🌡️ Temperature Scanner Integration

For temperature scanning systems, IntelliConnect works with **Sigma Controls IntelliScan**.

**Temperature Scanner → IntelliConnect → IntelliScan**

IntelliConnect acquires temperature data from the scanner through RS485/Modbus communication and provides the recorded data to IntelliScan for monitoring, visualization, historical analysis, and reporting.

**IntelliScan** is designed as an offline desktop application, allowing temperature data to be analyzed and reported without requiring continuous Internet connectivity.

---

### 🎛️ PID Controller Integration

For PID-based process control systems, IntelliConnect works with **Sigma Controls IntelliControl**.

**PID Controller → IntelliConnect → IntelliControl**

IntelliConnect acquires controller/process data through RS485/Modbus communication and provides the data to IntelliControl for monitoring, configuration, historical analysis, and reporting.

**IntelliControl** is a separate offline desktop application specifically designed for PID controller and process-control applications.

---

### 📊 Application & Product Matrix

| Product | Platform | Primary Function | Connectivity |
| :--- | :--- | :--- | :--- |
| **IntelliConnect** | ESP32 | Field-side acquisition & wireless connectivity | RS485, Modbus, Wi-Fi |
| **IntelliScan** | Windows | Temperature Scanner monitoring & analysis | Local / Offline |
| **IntelliControl** | Windows | PID Controller monitoring & control | Local / Offline |

The three components provide a complete field-to-desktop workflow while keeping the acquisition hardware independent from the desktop applications.

---

### ⚙️ Hardware Platform

*   **Microcontroller:** ESP32
*   **Industrial Interface:** RS485
*   **Communication Protocol:** Modbus RTU
*   **Wireless Connectivity:** Wi-Fi
*   **Network Modes:** Station / Access Point
*   **Local Storage:** SD Card
*   **Firmware Environment:** Arduino / PlatformIO

---

### 🛠 Technology Stack

*   **Microcontroller:** ESP32
*   **Firmware Framework:** Arduino
*   **Development Environment:** PlatformIO
*   **Industrial Communication:** RS485
*   **Protocol:** Modbus RTU
*   **Wireless Communication:** Wi-Fi
*   **Local Networking:** ESP32 Access Point
*   **Storage:** SD Card

---

### 🔄 Data Acquisition Workflow

The general acquisition workflow is:

1. Industrial equipment provides measurement or process data through RS485.
2. IntelliConnect communicates with the equipment using Modbus RTU.
3. The ESP32 processes the acquired data.
4. Data is recorded locally on the SD card.
5. IntelliConnect provides wireless access through Station or Access Point mode.
6. Recorded/acquired data can be consumed by the appropriate Sigma Controls desktop application.
7. Temperature Scanner systems use **IntelliScan**.
8. PID Controller systems use **IntelliControl**.

---
