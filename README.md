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

##### Descripción de Archivos
- **sujetoX_PPG.csv**: Cada archivo contiene las siguientes variables:
  - `fs`: Frecuencia de muestreo (en Hz)
  - `t`: Vector de tiempo (en segundos)
  - `y`: Datos de la señal PPG (valores de amplitud)

### Cómo Usar el Conjunto de Datos:

###### In MATLAB
1. Carga el archivo de datos:
   ```matlab
   data = load('sujeto1_PPG.mat');
   ppg_signal = data.y;  % Acceder a la señal PPG
   
##### In python
2. import scipy.io
 data = scipy.io.loadmat('tu_archivo.mat')
 ppg_signal = data['y'].flatten()  # Acceder a la señal PPG


###Annotations
Each subject's PPG signal is accompanied by its corresponding cholesterol concentration data, which can be integrated into your analysis for further research.

###Contributors
For any inquiries or issues regarding the dataset, please contact mateo.riascos00@usc.edu.co, sthefanny.salas00@usc.edu.co.

