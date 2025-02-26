# Cross-Flow Heat Exchanger Fouling Detection Simulator

An interactive web-based tool for simulating and detecting fouling phenomena in cross-flow heat exchangers based on physical modeling and parameter estimation.

![Simulator Interface](https://via.placeholder.com/800x400?text=Fouling+Detector+Interface)

## Overview

This simulator provides an interactive visualization of fouling detection in cross-flow heat exchangers. It implements a physical model-based detection approach using parameter estimation and CuSum statistical methods to identify when fouling occurs.

The model divides the heat exchanger into a 4×4 grid of sections on both the hot and cold sides, solving for temperature states in each section and monitoring the evolution of key parameters over time.

## Features

- **Interactive Visualization**: Real-time visualization of a cross-flow heat exchanger with hot and cold fluid flows
- **Parameter Control**: Comprehensive settings panel with sliders for all key parameters
- **Fouling Simulation**: Ability to simulate fouling with adjustable onset time, rate, and maximum value
- **Detection Algorithm**: Implementation of the CuSum algorithm for fouling detection
- **Multiple Visualizations**:
  - Heat exchanger diagram showing fluid flows
  - Fouling factor evolution chart
  - Parameter evolution charts for alpha and beta
  - CuSum detection visualization

## How to Use

1. Open `fouling-detection-visualization_2.html` in any modern web browser
2. Adjust simulation parameters using the settings panel on the left
3. Click "Start Simulation" to begin
4. Observe how parameters change as fouling develops
5. The system will automatically detect fouling when it exceeds the set threshold
6. Use "Reset" to restart the simulation with current parameters

### Key Parameters

The simulator allows adjustment of multiple parameter groups:

#### Model Parameters
- α (Alpha) and β (Beta): Heat transfer parameters
- τ<sub>h</sub> and τ<sub>c</sub>: Time constants for hot and cold sides
- γ (Gamma): Reynolds number exponent
- F: Correction factor

#### Fouling Parameters
- Fouling rate: Controls how quickly fouling accumulates
- Fouling start time: When fouling begins to develop
- Maximum fouling factor: Upper limit for fouling development

#### Heat Exchanger Parameters
- Heat transfer coefficients
- Reference mass flows
- Heat transfer areas
- Specific heat capacities

#### Detection Parameters
- Noise level: Measurement noise percentage
- CuSum K value: Reference value for detection algorithm
- CuSum H value: Detection threshold
- Window size: For moving average calculations

## Technical Details

This simulator is implemented entirely in HTML, CSS, and JavaScript, making it accessible without any server-side requirements. Key technical aspects include:

- **State-Space Model**: Implementation of a state-space representation of heat exchanger dynamics
- **Parameter Estimation**: Real-time estimation of model parameters
- **CuSum Detection**: Statistical method for detecting gradual parameter changes
- **Chart.js Visualization**: Dynamic charts for parameter evolution and fouling detection
- **Responsive Design**: Works on various screen sizes

## Mathematical Model

The simulator uses the following key model components:

1. **Heat Transfer Model**: Based on dividing the heat exchanger into a grid of sections
2. **Parameter Normalization**: Adjusts for variations in mass flow and operating conditions
3. **Fouling Factor Representation**: Models fouling as thermal resistance
4. **CuSum Detection Algorithm**: Monitors parameter shifts to detect fouling

## References

Based on the research paper:
- O. Gudmundsson, O.P. Palsson, H. Palsson, and S. Lalot, "Fouling detection in a cross-flow heat exchanger based on physical modeling," Heat Transfer Engineering, vol. 30, no. 8, pp. 682-699, 2009.

## License

This simulator is provided for educational and research purposes.

## Author

Developed by Ed Cherednik, 2025
