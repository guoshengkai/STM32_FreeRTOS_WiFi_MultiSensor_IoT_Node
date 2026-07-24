# STM32_FreeRTOS_WiFi_MultiSensor_IoT_Node
Real-time edge sensing node developed on STM32 B-L475E-IOT01A integrating DMA-based multi-channel ADC acquisition, FreeRTOS task scheduling, inter-task communication and WiFi data transmission.
        Sensors
           |
           |
      ADC1 + DMA
           |
           |
   Acquisition Task
   (FreeRTOS Thread 1)
           |
           |
   Message Queue
           |
           |
 Communication Task
 (FreeRTOS Thread 2)
           |
           |
      WiFi Module
           |
           |
    Remote Server (raspberry Pi 5/ PC)

Task 1: ADC Acquisition Thread
Function:
- Continuous ADC sampling
- DMA circular buffer handling
- Sensor data preprocessing


Task 2: Communication Thread
Function:
- Receive data from message queue
- Package sensor information
- Transmit data through WiFi


Inter-task communication: 
FreeRTOS Message Queue

    
