# PLC and Driver EVER Titanio Connection and BLDC Motor Axis Configuration with TwinCAT

This repository provides a step-by-step guide to establish the communication between a PLC and the EVER Titanio driver using the TwinCAT software. It also covers the initial configuration and testing of an axis driven by a BLDC motor.

### Features:
- Setting up the TwinCAT environment
- Configuring the communication between TwinCAT 3 Bechoff PLC and EVER Titanio Driver
- Initial axis setup and parameter tuning for the BLDC motor
- Mapping the PLC variables for motor control
- Running basic tests to validate the setup

### Getting Started:
1. **Install TwinCAT**: Ensure that TwinCAT 3 is installed and properly licensed.
2. **Connect EVER Titanio Driver**: Follow the wiring diagram to connect the PLC, motor and sensors with the EVER Titanio driver.
3. **Configure Ethernet Interface**: Set the IPv4 to static if there is not a DHCP serverand make sure that the Ip set correspond to the sub net of the PLC network
 [add image]
    Test the conection excecuting in the CMD arp -a and then do a ping to the PLC to check everething is correct
[add image]
5.**Set the Route**:in the Twincat XAE or un the twincat router click on edit routes (before that disconect other ether cat devices conected to the PLC)
   [image]
   then put the Ip addres of LAN interface of the PLC and search for it
   [image]
   click on it set the adress info to IP Address traget route static and remote Route Static
   [image]
   Add the route of (defalutl user: Administrator psw: 1)
   [image]
   if it shows a swoosh is correct and if it shows a lock it is set a secure ADS connection
   [image]
6. **Configure TwinCAT Project**:
   - Set up a new project in TwinCAT and establish a connection with the PLC.
     (To solve the problem Platform target selected is not supported first slect the target device an then select that the build is the same as the target)
   - Add the EVER Titanio driver in the hardware configuration (scan devices it should be added an axis).
7. **BLDC Motor Setup**: 
   - Define the motor parameters, such as pole pairs and rated current with the EverStudio App and save the xml with the configuration data.
   - Map the control and feedback signals between the PLC and the driver.
8. **Testing and Tuning**:
   - Execute the first axis movements and perform basic tests.
   - Fine-tune parameters such as speed, acceleration, and current limits.
   
---
