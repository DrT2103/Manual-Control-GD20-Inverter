# Manual Control GD20 Inverter
**Control *invt* Inverter GD20 Series manually by programming groups**  
<img src="https://i.imgur.com/3k4Hsev.jpg" width="150" height="250">
<img src="https://i.imgur.com/robAkFR.png" width="200" height="250">  
***invt** inverter  model **GD20-0R7G-S2** and **SPG 60W 3-phase motor** are used for examples in this reference.*

## Product Overview
### Name plate
<img src="https://i.imgur.com/VqdgyqS.png" width="400" height="215">

### Specifications
<img src="https://i.imgur.com/Sxol4Uo.png" width="200" height="45">  
<img src="https://i.imgur.com/ZLw7K5P.png" width="800" height="245">

## Keypad Operation
<img src="https://i.imgur.com/7zYExoP.png" width="700" height="700">

## Start/Stop and Rotation Control
### Parameter adjustment
For example, set parameter `P00.01 = 1`  
<img src="https://i.imgur.com/KAG9amf.png" width="790" height="240">

### Getting started
To start manually programming inverter with keypad mode, you have to make sure that all settings are set to default. To do this, follow these steps below:
- Step 1: Make connection for inverter and motor by wiring 3 lines U-V-W from motor to inverter
- Step 2: Connect L-N terminals to power supply (220Vac) and start the inverter
- Step 3: Set parameter `P00.18 = 1` to restore default settings
- Step 4: Set motor parameter (60W 3Ph SPG motor)
	- Motor power (kW) <kbd>→</kbd> `P02.01 = 0.06`
	- Frequency (Hz) <kbd>→</kbd> `P02.01 = 50`
	- Speed (RPM) <kbd>→</kbd> `P02. 03 = 1350`
	- Voltage (V) <kbd>→</kbd> `P02.04 = 220`
	- Current (A) <kbd>→</kbd> `P02.05 = 0.8`
- Step 5: Set `P00.01 = 0` to run command from keypad
- Step 6: Set `P00.06 = 1` to adjust motor speed by potentiometer on keypad

Now you can control some simple tasks of motor using keypad: *start/stop motor*, *control speed manually*, *jogging to test*.

### Control rotation direction


## Acceleration and Deceleration
## Start with Profile and DC Braking
## Register
## Modbus Overview
