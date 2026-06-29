# ChiShiri AI: Smart Mining Safety & Environmental Compliance Guardian

[cite_start]Ziso reGondo AI (derived from the Shona word *ziso*, meaning 'eagle eye') is an offline-capable, low-cost AI and IoT ecosystem designed to address critical safety, environmental management, and regulatory compliance challenges within the mining sector[cite: 28, 29, 32, 51]. [cite_start]Built specifically for resource-constrained environments with intermittent power and internet connectivity, the system empowers both artisanal small-scale miners (ASM) and large-scale industrial operations to safeguard worker dignity and preserve environmental health[cite: 33, 36, 37, 239].

---

## 📖 What the Mine IoT System Does

[cite_start]ChiShiri AI operates on a distributed, edge-first architecture that allows full site autonomy during internet outages[cite: 166, 167]. The primary functions of the ecosystem include:

* [cite_start]**Real-Time Hazard Detection:** Utilizes edge-based computer vision to identify structural instability (such as tunnel cracks and subsidence), unsafe worker practices (missing PPE like helmets, vests, or boots), and heavy equipment malfunctions[cite: 70].
* [cite_start]**Environmental Sensor Tracking:** Monitors continuous environmental vectors via a local mesh network, including air quality, water quality, ground vibrations, and tailings dam integrity[cite: 33, 70].
* [cite_start]**Multilingual Audio Alert System:** Dispatches immediate audio warnings on-site in Shona, Ndebele, and English to accommodate low-literacy workers, alongside SMS and USSD alerts to remote supervisors[cite: 42, 70, 116].
* [cite_start]**Automated Compliance Reporting:** Auto-generates formal Environmental Management Agency (EMA) compliance data reports and logs information securely[cite: 48, 70].
* [cite_start]**Tamper-Evident Auditing:** Records safety and compliance milestones on a permissioned ledger to create immutable audit trails for regulators and international buyers verifying responsible sourcing[cite: 43, 67, 111].

---

## 💻 How to Use the HTML Interface

The repository features a single-page, lightweight HTML5 dashboard (`index.html`) optimized for low-bandwidth and offline environments. It can run directly out of a browser or local storage medium without any active server side modules.

### 1. Global System Configuration Panel
* [cite_start]**System Status Indicator:** Toggles dynamically between **Online** (cloud synced), **Edge Mode** (fully autonomous local network tracking during outages), and **Simulation Mode**[cite: 72, 167].
* [cite_start]**Power Supply Monitor:** Displays live statuses for the **Electrical Grid** or the **Solar + Battery Backup System** to monitor load-shedding survival.
* [cite_start]**Language Selector:** Shifts the interface language across **English, Shona, and Ndebele** to adjust voice alert outputs and critical warning logs dynamically[cite: 42, 118].

### 2. Live Telemetry Layout
* [cite_start]**Computer Vision Incident Feed:** A scrolling, real-time logging terminal that populates hazard alerts immediately when edge cameras detect structural faults or safety violations[cite: 70, 169].
* [cite_start]**Sensor Visualization Cards:** Modular widgets presenting real-time data metrics including Air Quality (PM2.5, CO), Water Quality (pH levels), and Structural Stability (Vibrations)[cite: 70, 81, 83, 85].

### 3. Verification & Ingestion Controls
* **Simulation Mode Toggle:** A built-in feature designed for demonstration and testing purposes. Activating this toggle automatically pushes randomized mock industrial sensor anomalies and computer vision faults through the interface every 3 seconds.
* **Telemetry Data Integration:** The client interface processes live network inputs through a native JavaScript entry function: `updateDashboard(telemetryData)`. It parses real-time payloads structured as follows:
  ```json
  {
    "air_pm25": 42.5,
    "air_co": 10.2,
    "water_ph": 7.1,
    "vibration": 12.4,
    "hazard_event": "Missing Helmet Detected"
  }
