# PPG Signals and Cholesterol Concentration Dataset

This dataset contains PPG (Photoplethysmography) signals from 46 patients who were admitted to medical and surgical intensive care units at the Beth Israel Deaconess center, along with their associated cholesterol concentrations. It works as a validation tool for research aimed at using PPG signals to estimate total cholesterol levels in blood.

## Dataset Overview

- **Number of Subjects**: 46
- **File Format**: The dataset includes `.csv` files which are compatible with:
  - **MATLAB**
  - **Python** (using the `scipy.io` library)
  - **R** (using the `R.matlab` package)

#### Data Collection
he data were obtained on an outpatient basis, i.e., none of the individuals were hospitalized, and data collection was performed in a laboratory. Each of the 46 recordings contained a 8-min (480 s) PPGsignal. These were sampled at 125 Hz.

#### File Descriptions:
46 (32 womens and 14 mens)To estimate blood pressure, we analyzed Photoplethysmography (PPG) signals, which contain information about the variation in blood volume within blood vessels. The process consisted of the following steps:
  - Acquisition of the PPG Signal: The PPG signals of 46 patients were obtained and stored in .mat files. Each file contained the PPG signal, the sampling time, and the sampling frequency.
  - Feature Extraction: Characteristics such as rise time, fall time, time between pulses, and peak amplitude were extracted from the PPG signal. These features are crucial as they correlate with blood pressure.
  - Blood Pressure Classification: Thresholds based on medical literature were used to classify each patient into normotensive, prehypertensive, or hypertensive categories. For instance, longer rise times and reduced amplitudes can indicate increased arterial stiffness, typical in hypertensive individuals.
  - Validation: The results were compared with expected blood pressure values to validate the accuracy of the model.
 
- **sujetoX_PPG.mat**: Each file contains the following variables:
  - `fs`: Sampling frequency (in Hz)
  - `t`: Time vector (in seconds)
  - `y`: PPG signal data (amplitude values)

#### Blood Pressure Clasification:

Hypertension is a disease characterized by a constant elevation of blood pressure. It is measured with two numbers: systolic pressure, which reflects the pressure during heartbeats, and diastolic pressure, which indicates the pressure at rest between heartbeats. Although both values ​​are important, systolic pressure is especially relevant in people over 50 years of age, since its increase can indicate a higher risk of cardiovascular diseases due to hardening of the arteries and plaque buildup.

| **Blood Pressure Category** | **Systolic BP (mm Hg)** |   | **Diastolic BP (mm Hg)** |
| :---------------: | :----------------: | :-: | :---------: |
| Normal | <120 | and | < 80 |
| Elevated | 120 - 129 | and | < 80 |
| Hypertension (stage 1)| 130 -139  | or | 80 - 89|
| Hypertension (stage 2) | >=140 | or | >= 90 |
| Hypertensive crisis | >180 | and / or | >120 |

#### Recomendations for BP

| **Age** | **Blood Pressure Level (mm Hg)** |   
| :---------------: | :----------------: | 
| Youths | SBP 105 - 120 Y DBP 80 -73| 
| Adults | SBP 110 - 134 Y DBP 85 -77 |
| Advanced ages | SBP 121 - 147 Y DBP 83 - 91 |

### How to Use the Dataset

##### In MATLAB
1. Carga el archivo de datos:
   ```matlab
   data = load('sujeto1_PPG.mat');
   ppg_signal = data.y;  % Acceder a la señal PPG
   
##### In python
2.
   ```Python:
   import scipy.io:
   data = scipy.io.loadmat('tu_archivo.mat')
   ppg_signal = data['y'].flatten()  # Acceder a la señal PPG

##### In R
3.
   ```R:
   library(R.matlab)
   data <- readMat('sujeto1_PPG.mat')
   ppg_signal <- data$y  # Access PPG signal


###Annotations
Each subject's PPG signal is accompanied by its corresponding cholesterol concentration data, which can be integrated into your analysis for further research.

###Contributors
For any inquiries or issues regarding the dataset, please contact mateo.riascos00@usc.edu.co, sthefanny.salas00@usc.edu.co

####Referencias
1. (S/f-b). Heart.org. Recuperado el 29 de septiembre de 2024, de https://www.heart.org/en/health-topics/high-blood-pressure
2. (Valores normales de la presión arterial, 2022)
Valores normales de la presión arterial. (2022, agosto 4). Viamed Salud |; Viamed Salud. https://www.viamedsalud.com/patologias/cardiologia/valores-normales-presion-arterial/




