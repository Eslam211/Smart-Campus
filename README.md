# Smart_Campus

The Smart Campus dataset summarizes the measurements of the smart campus IoT sensor network that decomposes of hundreds of low-power sensors scattered across the university of Oulu campus (indoor) and the botanical garden (outdoor). The smart campus IoT sensor network consists of 462 devices scattered across 135,000 m^2 area. It consists of two datasets, namely, (a) LoRa parameters dataset that presents the physical layer characteristics of the LoRa network, and (b) Sensors readings dataset that presents the measurements of the sensors. The former consists of the time stamp of transmission, the channel used in transmission (there are 7 available channels), the device extended unique identifier DevEUI), the LoRa signal-to- noise ratio (LSNR) of the transmission, the port that is used to distinguish between messages, the binary RF chain value (RFCH), the received signal strength indicator (RSSI), and the frame counter (FCNT). The latter has the physical measured quantities besides the time stamp and the DevEUI. The sensors are divided into three types: i) CO2 devices measure CO2 levels, motion and light, ii) sound devices measure sound average, sound peak, motion and light, and iii) moisture devices measure pressure and moisture. In addition, all devices measure temperature and humidity and monitor their own battery levels. The physical quantities that are monitored by a device has a nan reading. Among the 462 devices, there are 326 CO2 devices, 119 sound devices and 17 moisture devices. The LoRa devices transmit their packets to a gateway, which relays the collected data to the server as shown in Fig. 1.


![LoRa System Model](https://user-images.githubusercontent.com/45125543/228687821-c9808ae1-6b4d-4fc0-b2dd-89b2a236eddd.jpg)
Fig. 1: The presented system model.

This repository consists of 7 files as follow that describe the work done on the propsed people counter model based on LoRaWAN as shown in Fig. 2:


![Proposed Model](https://user-images.githubusercontent.com/45125543/228688438-d9aaa51f-88cd-42d8-9e0b-a5681861080e.jpg)
Fig. 2: The proposed people counter model. First, the data imputation and pre-processing phase consists of failures identification and failures handling. Then, the data analysis phase consists of data predictor and people counter.



# 0. Documentation.ipynb
This file presents the documentation of the devices. For example: their type, location, data of installement, and other important parameters.


# 1. Preliminary_Analysis.ipynb
This file introduces a simple analysis of the readings of the sensor for the second dataset (the Sensors readings dataset). It introduces the basic analysis of each reading for all the devices over the whole datatset.


# 2. Advanced_Analysis.ipynb
This file presents a detailed analysis for the dataset. The minimum, maximum, and mean analysis are shown for the devices for each parameter. An analysis for individual devices is shown as well.


# 3. Detect_Missing_Transmissions.ipynb
This file detects and identifies the failures in the transmission of the devices in LoRa network between the devices and the gateway, or between the gateway and the server.


# 4. Test_Interpolation.ipynb
This file exploits different techniques to handle the missing values in the dataset reslting from the failures. In addition, it compares between these techniques and claims the best among them.


# 5. Fill_Missing_Transmissions.ipynb
This file fills the missing values for all the devices using the best approach presented in the previous file.


# 6. Predict_Number_of_People.ipynb
This file proposes a neural network scheme that uses the resulting parameters from the aforementioned files to predict the number of people inside a room.


# Dataset and Citation
To access the dataset: http://ieee-dataport.org/documents/smart-campus-dataset

We kindly ask you to cite our published paper: whenever you use the dataset or the uploaded notebooks.
