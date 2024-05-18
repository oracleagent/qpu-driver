
# QPU Driver

## Overview

This repository contains the low-level driver and firmware code for a custom-designed PCIe card, engineered to interface with an advanced setup incorporating lasers, a microwave generator, a diamond with nitrogen-vacancy (NV) centers, photoreceptors, vibration sensitivity sensors, and temperature sensors. The driver facilitates precise control and data acquisition from these components, enabling the exploitation of the unique quantum properties of NV centers for pioneering applications in quantum computing, magnetic field sensing, and other quantum technologies.

## Features and Capabilities

- **Laser Control**: Provides precise control over high-precision lasers used for optical excitation of NV centers.
- **Microwave Frequency Management**: Manages the microwave generator for accurate manipulation of NV center spin states.
- **NV Center Interaction**: Facilitates interaction with the diamond NV centers, essential for quantum state initialization, manipulation, and readout.
- **Photoreceptor Data Acquisition**: Enables high-sensitivity data acquisition from photodetectors capturing NV center fluorescence signals.
- **Vibration Monitoring**: Integrates with advanced vibration sensitivity sensors to monitor and compensate for mechanical vibrations, ensuring experimental stability.
- **Temperature Monitoring**: Interfaces with temperature sensors to maintain optimal operating conditions, enhancing reliability and performance.

## Applications

The driver is critical for applications that leverage the quantum characteristics of NV centers, including but not limited to:

- **Quantum Computing**: Supports scalable quantum information processing by facilitating high-fidelity manipulation of NV center spin states.
- **Magnetic Field Sensing**: Enables ultra-sensitive magnetic field detection through coherent control of NV center spins, applicable in medical imaging, materials science, and fundamental research.
- **Quantum Metrology**: Employs NV centers for high-precision measurement of physical quantities, leveraging their sensitivity to external fields and environmental conditions.

## Installation

To install the driver, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/oracleagent/qpu-driver.git
   cd qpu-driver
   ```

2. Build the driver:
   ```bash
   make
   ```

3. Flash the driver onto the PCIe card (if applicable):
   Follow the specific instructions for your PCIe card to load the driver/firmware.

## Usage

### Initial Setup

1. **Initialize the PCIe Card**: Load the driver and initialize the card.
   ```bash
   sudo ./qpu_init
   ```

2. **Verify Hardware Initialization**: Ensure all components (lasers, microwave generator, sensors) are correctly initialized.

### Performing Operations

1. **Control the Laser**:
   ```bash
   sudo ./qpu_control --laser on
   ```

2. **Set Microwave Frequency**:
   ```bash
   sudo ./qpu_control --mw 2.87GHz
   ```

3. **Read Data from Photoreceptors**:
   ```bash
   sudo ./qpu_read --sensor photoreceptor
   ```

4. **Monitor Vibration**:
   ```bash
   sudo ./qpu_read --sensor vibration
   ```

5. **Monitor Temperature**:
   ```bash
   sudo ./qpu_read --sensor temperature
   ```

### Next Steps

After installing and initializing the driver, you can:

1. **Develop Higher-Level Control Scripts**: Create scripts to automate and extend the control over the QPU setup, leveraging the driver functionalities.

2. **Integrate with Data Management Systems**: Use the data acquired from the QPU setup for further processing, analysis, and storage.

3. **Conduct Experiments**: Perform experiments leveraging the NV centers for quantum computing, magnetic field sensing, or quantum metrology.

4. **Contribute Enhancements**: Contribute to the development and enhancement of the driver by adding new features, improving existing functionalities, or fixing bugs.


## Contact

For further inquiries, technical support, or collaboration opportunities, please open an issue on the GitHub repository.
