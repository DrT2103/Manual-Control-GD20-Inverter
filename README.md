# Manual Control GD20 invt Inverter
**Control *invt* Inverter GD20 Series manually by programming groups**  
<img src="https://i.imgur.com/3k4Hsev.jpg" width="210" height="350">
<img src="https://i.imgur.com/robAkFR.png" width="280" height="350">  
***invt** inverter  model **GD20-0R7G-S2** and **SPG 60W 3-phase motor** are used for examples in this reference.*

## Product Overview
### Name plate
<img src="https://i.imgur.com/VqdgyqS.png" width="400" height="215">

### Specifications
<img src="https://i.imgur.com/Sxol4Uo.png" width="200" height="45">  
<img src="https://i.imgur.com/ZLw7K5P.png" width="600" height="185">

## Keypad Operation
<img src="https://i.imgur.com/7zYExoP.png" width="550" height="550">

## Start/Stop and Rotation Control
### Parameter adjustment
For example, set parameter `P00.01 = 1`  
<img src="https://i.imgur.com/O6DTtqs.png" width="690" height="285">  
**Note:** *Normally, SHIFT key is used to change the display of setting frequency, motor speed, output
ampere, ... (pay attention to the status lights corresponding to the data displayed)*.

### Getting started
To start manually programming inverter with keypad mode, you have to make sure that all settings are set to default. To do this, these following steps are applied:
- Step 1: Make connection for inverter and motor by wiring 3 lines U-V-W from motor to inverter
- Step 2: Connect L-N terminals to power supply (220Vac) and start the inverter
- Step 3: Set parameter `P00.18 = 1` to restore default settings
- Step 4: Set Maximum output frequency `P00.03` and Upper limit of the running frequency `P00.04` must greater than rated frequency of the motor
	- `P00.03 >= 50`
	- `P00.04 = 50 ~ P00.03`
- Step 5: Set motor parameter (60W 3Ph SPG motor)
	- Motor power (kW) <kbd>→</kbd> `P02.01 = 0.06`
	- Frequency (Hz) <kbd>→</kbd> `P02.01 = 50`
	- Speed (RPM) <kbd>→</kbd> `P02. 03 = 1350`
	- Voltage (V) <kbd>→</kbd> `P02.04 = 220`
	- Current (A) <kbd>→</kbd> `P02.05 = 0.8`
- Step 6: Set `P00.01 = 0` to run command from keypad
- Step 7: Set `P00.06 = 1` to adjust motor speed by potentiometer on keypad

Now we can control some simple tasks of motor using keypad: *start/stop motor*, *control speed manually*, *jogging to test*.

### Control rotation direction
The procedure of switching FWD/REV rotation is described in the *figure* below.  
<img src="https://i.imgur.com/yiNVZDn.png" width="475" height="240">  
Before controlling the switching rotation process, first we have to resive some important control parameters of group `P01`.  
<img src="https://i.imgur.com/lDhEglS.png" width="685" height="350">  
For example, to have the motor switched its rotation direction at frequency 40Hz immediately, we can adjust the above parameters to control the process.  
- `P01.13 = 0` (can be ignored)
- `P01.14 = 2`
- `P01.15 = 40`
- `P01.24 = 0` (can be ignored)

## Start with Profile and DC Braking
### Acceleration and deceleration
#### Acceleration and deceleration time

#### ACC/DEC selection

### DC braking

## Register
## Modbus Overview