The TiHAN-V2X Dataset was collected in Hyderabad, India, across various Vehicle-to-Everything (V2X) communication types, including Vehicle-to-Vehicle (V2V), Vehicle-to-Infrastructure (V2I), Infrastructure-to-Vehicle (I2V), and Vehicle-to-Cloud (V2C). The dataset offers comprehensive data for evaluating communication performance under different environmental and road conditions, including urban, rural, and highway scenarios. The dataset covers various communication parameters such as transmitted and received latitude, longitude, speed, altitude, heading, SNR, RSSI, path loss, effective radiated power (ERP), RX power, and noise power. This data is vital for studying the reliability and efficiency of V2X systems and optimizing protocols for connected vehicles.

The dataset is structured as follows:

V2V: 35 fields, 10,253 entries across 7 scenarios (S1-S7), covering both urban and rural areas, highways, and city streets.
V2I: 30 fields, 2,957 entries across 3 scenarios, focusing on optimizing V2I communication performance.
I2V: 38 fields, 2,106 entries collected in the TiHAN testbed at IIT Hyderabad, including weather data from RSUs and 5G sidelink interface.
V2C: 22 fields, 1,971 entries, focusing on cloud communication from vehicles using the User Datagram Protocol (UDP).
This dataset is critical for researchers and engineers focusing on V2X communication, enabling them to analyze communication parameters and performance under real-world conditions and apply AI/ML models to improve connected vehicle technologies.

Instructions: 
Documentation (Data Dictionaries and Structure Documentation):
V2V (Vehicle-to-Vehicle) Communication:

Entries: 10,253
Fields: 35
Scenarios: 7 (S1-S7) covering urban, rural, highways, and city streets.
Key Parameters:
Time_Epoch: Time of communication event (epoch format)
Transmitted Latitude, Longitude: Location of the transmitting vehicle (degrees)
Received Latitude, Longitude: Location of the receiving vehicle (degrees)
Speed (km/h): Speed of both transmitting and receiving vehicles
Altitude (m): Altitude of both vehicles
Heading (degrees): Heading direction of both vehicles
Distance (m): Distance between the transmitting and receiving vehicles
SNR (dB): Signal-to-noise ratio during communication
RSSI (dBm): Received Signal Strength Indicator for two antennas
Path Loss (dB): Signal attenuation
ERP (dBm): Effective Radiative Power
RX Power (dBm): Received power at the receiving vehicle
Noise Power (dBm): Power level of background noise
Packet Error Rate (PER): Rate of packet loss during transmission
V2I (Vehicle-to-Infrastructure) Communication:

Entries: 2,957
Fields: 30
Scenarios: 3 V2I scenarios
Key Parameters:
Latitude/Longitude (Tx & Rx): Location of the vehicle and RSU (degrees)
Heading (degrees): Heading direction of the vehicle
Speed (km/h): Speed of the vehicle
Altitude (m): Altitude of both the RSU and vehicle
Latency (ms): Communication delay between vehicle and RSU
Throughput (bits/sec): Data transfer rate
Distance (m): Distance between vehicle and RSU
Path Loss (dB): Signal path loss
ERP (dBm): Effective radiated power
RX Power (dBm): Received power at the vehicle
Noise Power (dBm): Background noise level
SNR (dB): Signal-to-noise ratio
Packet Error Rate (PER): Communication error rate
Receiver Gain (dB): Gain of the receiving antenna
I2V (Infrastructure-to-Vehicle) Communication:

Entries: 2,106
Fields: 38
Scenarios: 1 (conducted at TiHAN - IIT Hyderabad)
Key Parameters:
Similar to V2I but includes additional weather data (temperature, pressure, precipitation) as broadcasted by RSUs via the 5G sidelink interface.
This dataset supports the analysis of I2V communication performance and its reliability under different weather conditions.
V2C (Vehicle-to-Cloud) Communication:

Entries: 1,971
Fields: 22
Key Parameters:
Transmission/Reception Timestamp: Time of data transmission and reception
Latitude/Longitude (Tx): Location of the transmitting vehicle
Cloud Coordinates: Location of the receiving cloud server
Distance to Cloud (m): Distance between vehicle and cloud
Latency (ms): Delay in communication between vehicle and cloud
Packet Error Rate (PER): Communication error rate
Bandwidth (Mbits/sec): Data transmission capacity
Download/Upload Speed (Mbits/sec): Speed of data transfer
Total Data Transferred (MBytes): Cumulative amount of data transferred between vehicle and cloud
UDP: The dataset employs the User Datagram Protocol (UDP) for time-sensitive, efficient transmission between vehicle and cloud.
Instructions for Utilizing the Dataset:
Loading the Data:

Each CSV file (V2V, V2I, I2V, V2C) can be loaded into any data analysis platform, such as Python using pandas.
Example for loading the V2V data:pythonimport pandas as pd v2v_data = pd.read_csv('FinalV2V_Dataset.csv')
Preprocessing:

Unit normalization: Convert latencies, throughput, and power levels to consistent units across datasets if needed.
Filtering: Filter by scenarios or specific locations to focus on particular communication patterns.
Handling missing data: Check for missing or erroneous values and apply appropriate imputation techniques.
AI/ML Applications:

Predictive Models: Use regression models to predict latency or throughput based on distance, SNR, or other parameters.
Classification Models: Build classifiers to detect conditions that lead to high packet error rates or communication failures.
Optimization: Machine learning can be used to optimize transmission settings (e.g., frequency, power) for improved V2X performance.
Autonomous Driving Simulations: Use this data to model real-world V2X communications in smart city or highway driving scenarios, enhancing decision-making for autonomous vehicles.
Analyzing Performance:

Latency and Throughput: Use descriptive statistics to evaluate latency and throughput for different communication types.
Path Loss and SNR Analysis: Investigate how varying distances, locations, and scenarios impact path loss and SNR.
Scenario-based Analysis: Compare V2X performance across the seven V2V scenarios, or evaluate performance under specific urban, rural, and highway conditions.
Size of the Dataset:
V2V Dataset: 10,253 entries, 35 fields
V2I Dataset: 2,957 entries, 30 fields
I2V Dataset: 2,106 entries, 38 fields
V2C Dataset: 1,971 entries, 22 fields
This large dataset provides sufficient data for in-depth machine learning analysis, simulation studies, and real-world evaluation of V2X systems.
