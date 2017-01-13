# Climate Control Guru Overview
This app implements night and day venting using whole house fans and/or other ventilation equipment by strategically introducing outside air. It can supplement or in some climates take the place of conventional air-conditioners or heaters. It makes use of inside sensors along with current and forecast conditions from Weather Underground to accurately predict and fully automate when and how much to ventilate. Additionally, window coverings can be automatically manipulated to save energy.

Configurations typically include an indoor temperature sensor, a whole house fan, and motorized windows/skylights (though manually controlled windows with contact sensors are also an option). This app also automatically sets your thermostat to heating or cooling and turns it off during venting. A simple learning algorithm allows the app to better regulate inside temperatures over time. Learn more at LawsonAutomation.com.

# Required Devices
- SmartThings-supported temperature sensor (can be a thermostat)

# Optional Devices
- Whole house fans
- Attic fans
- Garage fans
- Basement or crawlspace fans
- Motorized windows and/or skylights
- Motorized window coverings
- Window contact sensors
- Humidity sensor
- Smoke detectors
- Thermostat
- Garage temperature sensor

# Installation
To run this app you must cut and paste it into the SmartThings IDE as a new project and then publish it to your SmartThings hub from there.

# Screenshots
![screenshots](https://cloud.githubusercontent.com/assets/22286765/21754222/15828604-d5b1-11e6-9887-5d0330e0fbd9.png)
# App State
## Mode
This value indicates whether the App is attempting to heat or cool through ventilation. This value is primarily based on forecast conditions.
# Settings in Detail
## Daytime Comfort Zone Minimum and Maximum
The comfort zone boundaries should be the same as the daytime settings for your thermostat, the minimum being the heating set point and the maximum being the cooling set point.
## Temperature Sensor
The temperature sensor should be placed in a central part of the house away from windows, doors, vents, or any other sources of heat or cold. 
When in doubt, place it near your thermostat.  Best case is for your temperature sensor to also be your thermostat.
## Humidity Sensor
This sensor allows inside and outside air to be compared when outside air has moderate to high levels of humidity. 
In drier climates such as California this sensor is not necessary. 
## Smoke Detectors
If any of these sensors detect smoke, whole house fans are turned off and will remain off until no smoke is detected. 
Windows are not shut when smoke is present for egress purposes. This is an important, recommended safety feature.
## Thermostats
These thermostats will be turned off when windows are open or whole house fans are on. 
Additionally, thermostats will be set to cooling or heating mode automatically when not venting.
## Whole House Fans
Whole house fans ventilate inside air into the attic, drawing air from windows or skylights.  
These fans will be utilized at appropriate times during the day to raise or lower inside temperatures. 
When and for how long they run is calculated using forecast and current temperatures for your area.

WARNING: Whole house fans, automated or not, create a strong negative pressure inside the home. 
There should be no circumstances in which flame, ash, or smoke can be drawn into the home from a fireplace. 
A glass insert or other like measure should always be installed along with a whole house fan to prevent 
fire hazard or smoke/ash related damage.
## Attic Fans
When the house is in cooling mode, attic fans will run continually to lower attic temperatures. 
Attic fans are turned off during whole house fan operation to save wear and tear on attic fans. 
No attic temperature sensor is required.
## Garage Fans
When in cooling mode, the garage fan will turn on in the late afternoon and off in the late morning. These are the times when outside temperatures are lower than garage temperatures.  No garage temperature sensor is required.
## Basement/Crawlspace Fans
When heating is needed, the basement/crawlspace fans will run when outside temperatures exceed temperatures inside the house. No basement/crawlspace temperature sensor is required.
## Motorized Windows/Skylights
Windows/skylights are automatically opened to accommodate heating or cooling when conditions are right.
## Contact Sensors
Contact sensors can be used either as an extra check that a motorized window is open or to indicate that a manual window has been opened.
## Window Coverings
These coverings will be opened along with windows when ventilating. 
Otherwise, window coverings are opened at sunrise and closed at sunset.
## Whole House Fan/Window Operating Modes
By default, whole house fans and windows/skylights will operate in all modes. 
However, you can specify with this option under which modes you want windows and whole house fans to automatically open/turn on.
## Number of Open Windows Needed
Whole house fans will not turn on automatically until the total number of window/skylights and contact sensors equals or exceeds this number. 
Note:  If an open window is automated and has a contact sensor installed, this will count as two open windows.
## Suspend Operation
The automated operation of Whole House Fans and windows/skylights can be suspended temporarily by clicking the checkbox. 
To resume operation, deselect the checkbox.
# Tips and Tricks
- Look in 'Notifications' of the SmartThings app to see what Climate Control Guru is doing.
- Whole house fan automation can be achieved (for cooling) without motorized windows by using contact sensors and manually opening the windows in the evening. 
- It is not recommended that whole house fans be automated without motorized windows, contact sensors, or some other means of obtaining outside air, such as louvers.
- The rule of thumb regarding the open window area required for a whole house fan is to take the square of the diameter of the fan and then double it.
- If your thermostat is not also controlled by this app, the comfort zone minimum and maximum might need to be within rather than equal to the daytime thermostat setting.
- WARNING: Without proper ventilation, whole-house fans can create a backdraft in your furnace or water heater, potentially causing carbon monoxide to be pulled into your home. 
- Operating the fan without open windows may also cause the fan to overheat.
- WARNING: Whole house fans, automated or not, create a strong negative pressure inside the home. 
- There should be no circumstances in which flame, ash, or smoke can be drawn into the home from a fireplace. 
- A glass insert or other like measure should always be installed along with a whole house fan to prevent fire hazard or smoke/ash related damage.
